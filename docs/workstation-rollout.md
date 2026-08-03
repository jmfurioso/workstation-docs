# 🚀 New Workstation Rollout

> Estimated time: **30–45 minutes**

This guide provisions a new CachyOS workstation from a fresh installation to a fully operational workstation.

---

## Overview

```text
Install CachyOS
      │
      ▼
Update System
      │
      ▼
Install 1Password
      │
      ▼
Run Commissioning
      │
      ▼
Bootstrap
      │
      ▼
Reboot
      │
      ▼
Install Components
      │
      ▼
Configure Microsoft PWAs
      │
      ▼
Acceptance Test
```

---

# Phase 1 — Base Operating System

## Install CachyOS

Complete a standard installation.

Recommended:

- KDE Plasma
- Wayland
- Internet connected

---

## Update

```bash
sudo pacman -Syu
```

Reboot if required.

---

# Phase 2 — Identity

## Install 1Password

Sign into your account.

Unlock your vault.

---

## Download Commissioning Script

Navigate to:

```
Nextcloud
└── IT Infrastructure
    └── Workstation
        └── Commissioning
```

Download:

```
commission-workstation.sh
```

---

# Phase 3 — Commission

```bash
cd ~/Downloads

chmod +x commission-workstation.sh

./commission-workstation.sh
```

Expected result:

- ✅ GitHub authenticated
- ✅ Git identity configured
- ✅ rclone configured
- ✅ Repository cloned
- ✅ Machine identity created
- ✅ bootstrap launched

---

# Phase 4 — Bootstrap

Allow bootstrap to finish.

Expected:

- Official packages
- AUR packages
- Flatpaks
- Wallpaper
- Plasma configuration
- Dotfiles

Reboot after completion.

---

# Phase 5 — Component Installers

Run only those required for this workstation.

| Component | Script |
|-----------|--------|
| ScreenConnect | `install-screenconnect.sh` |
| NoMachine | `install-nomachine.sh` |
| LucidLink | `install-lucidlink.sh` |
| Ninja Remote Player | `install-ninjaone.sh` |
| Framework Audio | `install-framework-audio.sh` |

---

# Phase 6 — Microsoft

Create Edge profiles manually.

Install:

- Teams (Inside)
- Teams (SOS)
- Teams (Tagwall)

Install:

- Outlook (Inside)
- Outlook (SOS)
- Outlook (Tagwall)

---

# Phase 7 — Acceptance

Proceed directly to:

➡️ **Acceptance Test**
