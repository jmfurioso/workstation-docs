# 🚀 New Workstation Rollout

> Use this page from top to bottom. Don't rely on memory.

This guide takes a fresh CachyOS installation to a ready-to-use Mono workstation.

The rollout supports two paths:

| Rollout | Use when |
| --- | --- |
| **KDE Plasma** | CachyOS was installed with KDE Plasma |
| **Desktop-neutral** | CachyOS was installed with GNOME, COSMIC, XFCE, or another desktop |

Desktop appearance and personalization are intentionally manual. The automated rollout focuses on applications, services, configuration required for functionality, and specialized component installers.

---

## 🗺️ Rollout Overview

```text
Install CachyOS and choose a desktop
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
      Select Rollout Path
        ┌─────┴─────┐
        ▼           ▼
       KDE       Neutral
        └─────┬─────┘
              ▼
 Install Required Components
              │
              ▼
 Configure Microsoft Edge + PWAs
              │
              ▼
    Personalize the Desktop
              │
              ▼
       Acceptance Test
```

---

# Phase 1 — Install CachyOS

Perform a normal CachyOS installation.

Use:

- The desktop environment you intend to keep
- Wayland when supported and appropriate
- A normal user account
- A working Internet connection

Supported rollout examples include:

- KDE Plasma
- GNOME
- COSMIC
- XFCE
- Another CachyOS-supported desktop environment

Do not install KDE merely to obtain workstation applications. The desktop-neutral rollout uses the environment selected during the CachyOS installation.

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
- Clone the workstation repository
- Create the machine identity
- Offer to launch the rollout selector

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

For a new laptop, choose its permanent workstation name and use that consistently.

### Expected Result

Before rollout selection begins, commissioning should report successful:

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

# Phase 5 — Select the Rollout

Commissioning launches:

```text
Workstation Bootstrap Selection

1) KDE Plasma rollout
2) Desktop-neutral rollout
Q) Quit without running a bootstrap
```

Choose exactly one path.

## KDE Plasma Rollout

Choose **KDE Plasma** only when KDE Plasma is the installed desktop environment.

This runs:

```bash
./scripts/bootstrap.sh
```

It installs:

- The established official Arch/CachyOS package set
- KDE and Plasma applications included in that baseline
- Common AUR applications
- Common Flatpak applications
- Curated non-Plasma configuration and local files, when present

It intentionally leaves Plasma themes, panels, wallpaper, global shortcuts, and other personalization manual.

## Desktop-Neutral Rollout

Choose **Desktop-neutral** when using GNOME, COSMIC, XFCE, or another non-KDE desktop.

This runs:

```bash
./scripts/bootstrap-neutral.sh
```

It installs:

- Desktop-independent official Arch/CachyOS packages
- Desktop-independent AUR applications
- Desktop-independent Flatpak applications

It does **not**:

- Install KDE or Plasma
- Install GNOME or COSMIC components
- Install another desktop environment
- Restore desktop configuration
- Restore desktop themes, panels, wallpaper, layouts, or global shortcuts
- Install KDE applications such as Dolphin, Kate, Gwenview, Ark, or Spectacle

The selected desktop environment supplies its own file manager, image viewer, archive manager, screenshot tool, Bluetooth frontend, and other desktop utilities.

## Run the Selector Later

To reopen the selector manually:

```bash
cd ~/Projects/workstation
./scripts/select-bootstrap.sh
```

---

## Optional Component Installers

At the end of either bootstrap, you will be asked whether to install optional workstation components.

Choose **Yes** for the components required on this machine.

Normally offered installers include:

| Component | Purpose |
| --- | --- |
| LucidLink | LucidLink client installation and Arch-specific handling |
| NoMachine | Remote desktop |
| ScreenConnect | Remote support |
| Ninja Remote Player | NinjaOne remote workstation access |

Hardware-specific troubleshooting installers are intentionally not offered during normal provisioning.

For example, run the Framework audio installer manually only when required:

```bash
cd ~/Projects/workstation
./scripts/install-framework-audio.sh
```

The installer scripts handle software that needs more than ordinary package installation.

If uncertain about a component, see:

➡️ [Component Installers](component-installers.md)

---

# Phase 6 — Reboot and Verify the Core System

After bootstrap and the required component installers complete:

```bash
sudo reboot
```

Log back in.

Before spending time on appearance, verify the important functional pieces:

- The intended desktop environment launches
- No unintended second desktop environment was installed
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

## Teams PWAs

Create a Teams PWA for each required organization/profile:

- Teams — Inside
- Teams — SOS
- Teams — Tagwall

## Outlook PWAs

Create an Outlook PWA for each required organization/profile:

- Outlook — Inside
- Outlook — SOS
- Outlook — Tagwall

Authentication and MFA remain manual.

---

# Phase 8 — Personalize the Desktop

Now make the workstation yours.

Desktop personalization is deliberately outside both automated rollouts.

Configure the selected environment manually, including:

- Displays, orientation, scaling, and refresh rates
- Panels, docks, or workspaces
- Wallpaper
- Theme and icons
- Global shortcuts
- Default terminal
- Default file manager and desktop applications

➡️ [Open Desktop Personalization](desktop-customization.md)

## KDE Theme Reference

When using KDE Plasma, the current preferred starting point is:

[LibrePixels Catppuccin Theme](https://www.librepixels.com/en/tutoriales/catppuccintheme/){ target="_blank" rel="noopener" }

Follow the author's current instructions rather than trying to reproduce theme settings from another workstation.

This reference does not apply to GNOME, COSMIC, XFCE, or other desktop environments.

---

# Phase 9 — Acceptance Test

Do not consider the rollout finished until the acceptance checklist passes.

➡️ [Open Workstation Acceptance Test](acceptance-test.md)

The goal is not for every workstation to look identical.

The goal is:

> **A complete, functional Mono workstation that is ready for daily use.**
