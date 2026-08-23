# Lymow Toolkit — Home Assistant add-on image.
#
# PULLS the official prebuilt multi-arch image instead of rebuilding it on the user's Home
# Assistant machine. This file used to start FROM python:3.12-slim and then, on the user's box,
# apt-install ffmpeg, pip-install Playwright, download Chromium, download the release bundle and
# fetch cloudflared — every install and every update. On a Raspberry Pi that took HOURS, and it
# ran again for every new version.
#
# ghcr.io/appguy77/lymow-toolkit already contains all of that, built once by CI for amd64, arm64
# and armv7 (.github/workflows/docker-ghcr.yml). Supervisor pulls the layer for the machine's own
# architecture, so an add-on install or update is now a download rather than a build — the same
# thing `docker compose pull` does for Docker users.
#
# The tag is pinned to the add-on's version, never :latest. Home Assistant decides when to update
# an add-on, and a floating tag would let the image change underneath a version the user has not
# chosen to move to.
ARG BUILD_FROM
FROM ghcr.io/appguy77/lymow-toolkit:1.51.0

# /data is Home Assistant's persistent add-on volume: login/config/backups survive updates and
# rebuilds. Everything else — host, port, no reload — matches the standalone Docker image.
# LYMOW_KEY_DIR is the add-on's OWN config volume (map: addon_config -> /config), never /data:
# 'Stay signed in' keeps its unlock key there and the encrypted record in /data, so a copied
# data folder or a partial backup carries one half and never both.
ENV LYMOW_HOST=0.0.0.0 LYMOW_PORT=8787 LYMOW_RELOAD=0 PYTHONUNBUFFERED=1 LYMOW_DATA=/data LYMOW_KEY_DIR=/config/.lymow-key
EXPOSE 8787
CMD ["python", "-m", "app.run"]
