# 🎨 Desktop Personalization

Desktop appearance is intentionally **not automated**.

The workstation rollout creates a functional, consistent software environment. Plasma appearance remains a personal choice and is configured manually after the core workstation is working.

---

# Plasma Theme

## LibrePixels Catppuccin

The current preferred starting point:

[Open the LibrePixels Catppuccin tutorial](https://www.librepixels.com/en/tutoriales/catppuccintheme/){ target="_blank" rel="noopener" }

Follow the author's current instructions.

The tutorial may install or configure:

- Plasma theme
- Color scheme
- Window decorations
- Icons
- Fonts
- Plasmoids
- Panel layout

These assets are intentionally **not copied from another workstation**.

!!! important

    Do **not** run `bootstrap.sh` afterward to restore a desktop layout.

    Bootstrap deliberately leaves Plasma personalization untouched.

---

# Other Themes

This page can become a collection of themes worth revisiting.

## Current References

| Theme | Reference |
|---|---|
| LibrePixels Catppuccin | [Installation Guide](https://www.librepixels.com/en/tutoriales/catppuccintheme/){ target="_blank" rel="noopener" } |

Add additional themes here when you find ones worth keeping.

---

# Wallpaper

Choose the wallpaper manually.

Wallpaper is intentionally **not**:

- captured by `capture-workstation.sh`
- restored by `bootstrap.sh`
- standardized between workstations

Each workstation can have its own wallpaper.

---

# Plasma Layout

Configure the Plasma desktop manually.

This includes:

- Panels
- Panel size and position
- Application launcher
- Widgets
- Desktop layout
- Virtual desktops
- Window decorations
- Icons
- Global shortcuts

These settings are no longer promoted from one workstation to another through `capture-workstation.sh`.

---

# Microsoft Edge Profiles

Create the required Edge profiles manually.

Current profiles:

- Inside
- SOS
- Tagwall

Authenticate each profile as required.

---

# Teams PWAs

Create Teams PWAs in the appropriate Edge profiles.

Current organizations:

- Teams — Inside
- Teams — SOS
- Teams — Tagwall

---

# Outlook PWAs

Create Outlook PWAs in the appropriate Edge profiles.

Current organizations:

- Outlook — Inside
- Outlook — SOS
- Outlook — Tagwall

Authentication and MFA remain intentionally manual.

---

# Optional Applications

Install additional personal applications only when desired.

They do not need to become part of the workstation standard unless you decide they should be present on future machines.

---

# What Capture Does Now

`capture-workstation.sh` is intentionally narrow.

It captures:

- Installed official package inventory
- Installed foreign/AUR package inventory
- Installed Flatpak inventory

It does **not** capture desktop personalization.

This keeps application standardization separate from appearance.

---

# Philosophy

> **Automate functionality. Personalize appearance.**

The workstation project should reliably reproduce the tools required for daily work without trying to clone every visual preference from another machine.
