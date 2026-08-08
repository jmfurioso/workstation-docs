# 🚀 New Workstation Rollout

> Use this page from top to bottom. Don't rely on memory.

This guide takes a fresh CachyOS installation to a ready-to-use Mono workstation.

Plasma appearance and desktop personalization are intentionally manual. The automated rollout focuses on applications, services, configuration required for functionality, and specialized component installers.

---

## 🗺️ Rollout Overview

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
Download Commissioning Script
      │
      ▼
Commission Workstation
      │
      ▼
Bootstrap
      │
      ▼
Install Required Components
      │
      ▼
Configure Microsoft Edge + PWAs
      │
      ▼
Personalize Plasma
      │
      ▼
Acceptance Test
```

---

# Phase 1 — Install CachyOS

Perform a normal CachyOS installation.

Use:

- KDE Plasma
- Wayland
- Normal user account
- Working Internet connection

After reaching the desktop, update the system:

```bash
sudo pacman -Syu
```

If the update installs a new kernel or other major system components, reboot before continuing.

---

# Phase 2 — Install 1Password

Install and launch 1Password.

Sign into the vault and verify that credentials are available before continuing.

You will need credentials during commissioning and application setup.

---

# Phase 3 — Get the Commissioning Script

Open Nextcloud and navigate to:

```text
IT Infrastructure
└── Workstation
    └── Commissioning
```

Download:

```text
commission-workstation.sh
```

to `~/Downloads`.

---

# Phase 4 — Commission the Workstation

Open a terminal:

```bash
cd ~/Downloads
chmod +x commission-workstation.sh
./commission-workstation.sh
```

The commissioning script will guide you through the process.

It will:

- Install commissioning prerequisites
- Configure Git identity
- Install `paru` if required
- Authenticate GitHub
- Configure the `monocloud:` rclone remote
- Clone the private workstation repository
- Create the machine identity
- Offer to launch bootstrap

### GitHub

Complete the browser authentication when prompted.

### Nextcloud

Use the requested Nextcloud username and app password from 1Password.

### Machine Name

Use a short lowercase identifier appropriate for the machine.

Examples:

```text
fw13
fw12
desktop
```

For the new laptop, choose its permanent workstation name and use that consistently.

### Expected Result

Before bootstrap begins, commissioning should report successful:

- Git identity configuration
- GitHub authentication
- Nextcloud access
- Repository preparation
- Machine identity creation

When asked:

```text
Run workstation bootstrap now? [Y/n]
```

choose **Yes**.

---

# Phase 5 — Bootstrap

Bootstrap builds the functional workstation.

It installs:

- Common official Arch/CachyOS packages
- Common AUR packages
- Flatpak applications
- Curated non-Plasma configuration
- Curated non-Plasma local files

Bootstrap intentionally leaves these alone:

- Plasma themes
- Look-and-Feel packages
- Panel layouts
- Window decorations
- Icon themes
- Wallpapers
- Global shortcuts
- Other desktop personalization

Those are handled later.

---

## Optional Component Installers

At the end of bootstrap you will be asked whether to install optional workstation components.

Choose **Yes** for the components required on this machine.

Current specialized installers include:

| Component | Purpose |
|---|---|
| LucidLink | LucidLink client installation and Arch-specific handling |
| NoMachine | Remote desktop |
| ScreenConnect | Remote support |
| Ninja Remote Player | NinjaOne remote workstation access |
| Framework Audio | Framework-specific microphone/audio configuration |

The installer scripts handle software that needs more than ordinary package installation.

If uncertain about a component, see:

➡️ [Component Installers](component-installers.md)

---

# Phase 6 — Reboot and Verify Core System

After bootstrap and the required component installers complete:

```bash
sudo reboot
```

Log back in.

Before spending time on appearance, verify the important functional pieces:

- Repository exists at `~/Projects/workstation`
- Internet works
- 1Password works
- Browser works
- LucidLink mounts correctly, if installed
- Remote-access tools launch, if installed

---

# Phase 7 — Microsoft Edge and PWAs

Microsoft Edge is installed as part of the workstation software baseline, but profiles and PWAs are intentionally configured manually.

## Create Edge Profiles

Create the required profiles:

- Inside
- SOS
- Tagwall

Authenticate each profile as required.

---

## Teams PWAs

Create a Teams PWA for each required organization/profile:

- Teams — Inside
- Teams — SOS
- Teams — Tagwall

---

## Outlook PWAs

Create an Outlook PWA for each required organization/profile:

- Outlook — Inside
- Outlook — SOS
- Outlook — Tagwall

Authentication and MFA remain manual.

---

# Phase 8 — Personalize Plasma

Now make the workstation yours.

Desktop personalization is deliberately outside the automated bootstrap.

➡️ [Open Desktop Personalization](desktop-customization.md)

## Current Theme Reference

The current preferred starting point is:

[LibrePixels Catppuccin Theme](https://www.librepixels.com/en/tutoriales/catppuccintheme/){ target="_blank" rel="noopener" }

Follow the author's current instructions rather than trying to reproduce theme settings from another workstation.

Additional theme references can be added to the Personalization page over time.

---

# Phase 9 — Acceptance Test

Do not consider the rollout finished until the acceptance checklist passes.

➡️ [Open Workstation Acceptance Test](acceptance-test.md)

The goal is not for every workstation to look identical.

The goal is:

> **A complete, functional Mono workstation that is ready for daily use.**
