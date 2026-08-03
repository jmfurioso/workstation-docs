# 🎨 Desktop Customization

This document covers optional workstation personalization.

The workstation is fully functional without these steps.

---

# LibrePixels Catppuccin Theme

Reference:

https://www.librepixels.com/en/tutoriales/catppuccintheme/

Follow the guide exactly.

When complete, run:

```bash
cd ~/Projects/workstation

./scripts/bootstrap.sh
```

to restore:

- wallpaper
- Plasma configuration
- panel layout
- shortcuts
- workstation preferences

---

# Microsoft Edge PWAs

Create manually.

## Teams

- Inside
- SOS
- Tagwall

## Outlook

- Inside
- SOS
- Tagwall

These remain intentionally manual.

---

# Optional Applications

Install only if desired.

Examples:

- Google Earth Pro
- KTailctl
- Proton Mail
- Other personal desktop applications

---

# Wallpaper

The workstation wallpaper is restored automatically by bootstrap.

Changing wallpapers is considered personal customization.

Run:

```bash
./scripts/capture-workstation.sh
```

when promoting a new wallpaper to the workstation standard.

---

# Plasma Layout

The desktop workstation is the reference implementation.

When significant layout improvements are made:

```bash
./scripts/capture-workstation.sh
```

Commit the updated configuration.

Future workstation deployments inherit the new layout.

---

# Philosophy

Automate:

- repeatable configuration

Document:

- intentional manual customization

Avoid:

- automating highly personal desktop preferences unless they become part of the workstation standard.
