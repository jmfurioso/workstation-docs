# 🎨 Desktop Personalization

Desktop appearance is intentionally **not automated**.

The workstation rollout creates a functional, consistent software environment. Appearance remains a personal choice and is configured manually after the core workstation is working.

This policy applies to KDE Plasma, GNOME, COSMIC, XFCE, and other desktop environments.

---

# KDE Plasma Theme

## LibrePixels Catppuccin

When using KDE Plasma, the current preferred starting point is:

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

    Do **not** run bootstrap afterward expecting it to restore a desktop layout.

    Both rollout paths deliberately leave desktop personalization untouched.

---

# Other Desktop Environments

When using GNOME, COSMIC, XFCE, or another desktop:

1. Run the desktop-neutral workstation rollout.
2. Use that environment's own settings and applications.
3. Configure appearance, panels, shortcuts, and default applications manually.
4. Do not install the KDE rollout merely to obtain workstation applications.

Individual KDE or Qt applications can be installed later if specifically wanted, but they are intentionally absent from the neutral rollout.

---

# Other Themes

This page can become a collection of themes worth revisiting.

## Current References

| Desktop | Theme | Reference |
| --- | --- | --- |
| KDE Plasma | LibrePixels Catppuccin | [Installation Guide](https://www.librepixels.com/en/tutoriales/catppuccintheme/){ target="_blank" rel="noopener" } |

Add additional themes here when you find ones worth keeping.

---

# Wallpaper

Choose the wallpaper manually.

Wallpaper is intentionally **not**:

- Captured by `capture-workstation.sh`
- Restored by either bootstrap
- Standardized between workstations

Each workstation can have its own wallpaper.

---

# Desktop Layout

Configure the selected desktop environment manually.

This includes:

- Panels, docks, or workspaces
- Panel or dock size and position
- Application launcher
- Widgets or extensions
- Desktop layout
- Virtual desktops or workspaces
- Window decorations
- Icons
- Global shortcuts
- Default desktop applications

These settings are not promoted from one workstation to another through `capture-workstation.sh`.

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

The workstation project should reliably reproduce the tools required for daily work without trying to clone every visual preference from another machine or tying the workstation core to a particular desktop environment.
