# Lymow Toolkit — Home Assistant add-on image. Built ON the user's HA machine at install time
# (no prebuilt registry): it downloads the OFFICIAL versioned docker bundle from the public
# GitHub release — the exact obfuscated bits every other platform ships — and applies the same
# proven steps as the standalone Docker build. python:3.12-slim is multi-arch, so this builds
# natively on amd64 / aarch64 (Raspberry Pi 4-5, ODROID) / armv7 HA boxes.
ARG BUILD_FROM=ghcr.io/home-assistant/amd64-base:latest
FROM python:3.12-slim

ARG LYMOW_VERSION=1.38.2
WORKDIR /app

# app payload (official release bundle) + python deps + camera/tunnel helpers, one cached layer
# Google-sign-in browser = the Playwright chromium build (most compatible headless build; the Debian
# distro build silently crashed on some hosts). armv7 has no Playwright build -> Debian chromium.
ENV PLAYWRIGHT_BROWSERS_PATH=/opt/pw
RUN apt-get update && apt-get install -y --no-install-recommends ffmpeg fonts-liberation dbus curl ca-certificates \
    && dbus-uuidgen --ensure=/etc/machine-id \
    && arch="$(dpkg --print-architecture)" \
    && if [ "$arch" = "amd64" ] || [ "$arch" = "arm64" ]; then \
         pip install --no-cache-dir playwright \
         && (playwright install --with-deps --no-shell chromium \
             || playwright install --with-deps chromium); \
       else apt-get install -y --no-install-recommends chromium; fi \
    && curl -fsSL --retry 3 -o /tmp/lymow.tar.gz \
       "https://github.com/AppGuy77/lymow-toolkit-downloads/releases/download/v${LYMOW_VERSION}/lymow-docker-v${LYMOW_VERSION}.tar.gz" \
    && tar xzf /tmp/lymow.tar.gz -C /tmp \
    && cp -a /tmp/lymow-docker/. /app/ \
    && rm -rf /tmp/lymow.tar.gz /tmp/lymow-docker \
    && pip install --no-cache-dir -r requirements.txt \
    && case "$(dpkg --print-architecture)" in armhf|armel) cfarch=arm;; i386) cfarch=386;; *) cfarch="$(dpkg --print-architecture)";; esac \
    && (curl -fsSL --connect-timeout 10 --max-time 180 --retry 2 -o /usr/local/bin/cloudflared \
       "https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-${cfarch}" \
       && chmod +x /usr/local/bin/cloudflared \
       || echo "WARN: cloudflared fetch skipped (remote tunnel off; LAN/HA access still works)") \
    && apt-get purge -y curl && apt-get autoremove -y && rm -rf /var/lib/apt/lists/*

# /data is Home Assistant's persistent add-on volume: login/config/backups survive updates & rebuilds
ENV LYMOW_HOST=0.0.0.0 LYMOW_PORT=8787 LYMOW_RELOAD=0 PYTHONUNBUFFERED=1 LYMOW_DATA=/data
EXPOSE 8787
CMD ["python", "-m", "app.run"]
