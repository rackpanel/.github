<p align="center">
  <img src="https://raw.githubusercontent.com/rackpanel/rack-panel/main/assets/banner.png" alt="RACK//PANEL" width="100%" />
</p>

<h2 align="center">Touchscreen-First Infrastructure &amp; Homelab Control Consoles</h2>

<p align="center">
  Building fast, high-contrast, self-hosted control panels engineered to run smoothly on dedicated rack touchscreens — from brand-new tablets down to repurposed <strong>Android 4.4 KitKat</strong> wall displays.
</p>

<p align="center">
  <a href="https://github.com/rackpanel/rack-panel"><img src="https://img.shields.io/badge/Repository-rackpanel%2Frack--panel-22d3ee?logo=github&logoColor=white" alt="rack-panel" /></a>
  <a href="https://github.com/rackpanel/rack-panel/pkgs/container/rack-panel"><img src="https://img.shields.io/badge/Docker-ghcr.io%2Frackpanel%2Frack--panel-3b82f6?logo=docker&logoColor=white" alt="GHCR" /></a>
  <img src="https://img.shields.io/badge/Multi--Arch-amd64%20%7C%20arm64-34d399" alt="Multi-arch" />
</p>

---

### Featured Project

| Project | Description | Container Image |
| --- | --- | --- |
| [**`rack-panel`**](https://github.com/rackpanel/rack-panel) | Unified real-time touchscreen command center for **SSH Servers (Linux & macOS)**, **Proxmox VE** (VMs, LXCs, Storage, Fullscreen Terminal & noVNC), **OPNsense** (23.x–25.x gateways, interfaces, PF states, services, logs), and **Tailscale** mesh discovery with automatic cross-source device deduplication, persistent user login, and 4-digit splash PIN lock. | `ghcr.io/rackpanel/rack-panel:latest` |

---

### Quick Deploy

```bash
docker run -d \
  --name rack-panel \
  --restart unless-stopped \
  -p 3840:3840 \
  -v rack_panel_data:/app/server/data \
  ghcr.io/rackpanel/rack-panel:latest
```

---

### Core Design Principles

- **Touchscreen & Kiosk First** — Oversized tactile controls, edge-to-edge fullscreen Terminal & VNC modes with floating touch exit bars, and burn-in-safe idle metrics splash screens.
- **Zero-Waste Telemetry** — Single-poll Union-Find device deduplication unifies overlapping SSH, Proxmox, Tailscale, and OPNsense nodes so hosts are never double-polled or double-counted.
- **Self-Hosted & Encrypted** — All credentials, API tokens, session keys, and PINs stay on your network, encrypted at rest with AES-256-GCM.
- **Runs Everywhere** — Multi-arch Docker images (`linux/amd64`, `linux/arm64`) and a legacy ES5 + Flexbox frontend bundle built for Android 4.4+ WebViews as well as modern desktop browsers.
