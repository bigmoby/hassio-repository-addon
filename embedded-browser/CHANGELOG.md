# 🚀 Release 1.0.1 - Stable Release

We are excited to announce the first stable release of the **Epiphany Embedded Browser** add-on! This version focuses on security, improved logging, and a more robust container architecture.

## 🛡️ Security Improvements
- **Password Masking**: Updated the configuration schema to use the `password` type for `vnc_password`. This ensures your VNC password is encrypted at rest and automatically masked in the Home Assistant UI and Supervisor logs.
- **Safer Secret Handling**: Replaced insecure `echo` commands with `printf` and temporary file-based authentication for the VNC server, preventing secrets from leaking into process lists or shell history.

## 🐞 Bug Fixes & Stability
- **Fixed VNC Startup**: Resolved a critical issue where setting a VNC password would prevent the add-on from starting due to a missing password file reference.
- **Dependency Fix**: Added `tigervnc-tools` to the Docker image to ensure the `vncpasswd` utility is always available.
- **Improved Service Handling**: Enhanced the `s6-overlay` service scripts for better reliability during startup and restarts.

## 📊 Observability
- **Live VNC Logging**: Integrated VNC server logs directly into the Home Assistant Add-on log stream. You can now see authentication attempts (including failures) and display server events in real-time.

## 📖 Documentation
- **Technical Architecture**: Added a comprehensive "How it works" section to the README and DOCS. This explains the internal stack (Xvnc -> Openbox -> Epiphany -> Websockify -> noVNC) for advanced users and contributors.

## 🛠 Internal Changes
- **Version Bump**: Bumped to `1.0.1`.
- **Production Image**: Enabled the pre-built image path in `config.yaml` for faster deployments.

---

**Full Changelog**: https://github.com/bigmoby/addon-embedded-browser/compare/v0.0.2...v1.0.1
