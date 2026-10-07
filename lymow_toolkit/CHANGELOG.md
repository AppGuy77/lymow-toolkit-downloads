Lymow Toolkit v2.10.5

An update fix for Mac and Linux. It keeps your sign-in, settings, maps, layout and history — just update.


- **Mac and Linux: the update should install again.** v2.10.4 stopped with a Python version message on Macs and Linux machines running Python 3.10, and on Intel Macs.
- **Still on v2.10.3?** This update brings everything in v2.10.4 too — see the change log.


## Installs

- **Mac and Linux:** the in-app update and `install.sh` should install again on Python 3.10 and on Intel Macs. Your install was not changed by the failed attempt — it kept running the version you had.
- **Mac and Linux without Python 3.10 or newer:** `install.sh` now always downloads Python 3.12, the same Python the Windows and Docker versions use.
- If an update cannot install its Python packages, the message now names the Python version your install runs.
