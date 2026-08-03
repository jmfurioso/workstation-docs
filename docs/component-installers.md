# 🧰 Component Installers

These installers configure software that requires additional setup beyond package installation.

---

# ScreenConnect

```bash
./scripts/install-screenconnect.sh
```

Purpose

- Install the ScreenConnect client.
- Register this workstation with the ScreenConnect server.

---

# NoMachine

```bash
./scripts/install-nomachine.sh
```

Purpose

- Install NoMachine.
- Configure remote desktop access.

---

# LucidLink

```bash
./scripts/install-lucidlink.sh
```

Purpose

- Download the latest installer from Nextcloud.
- Convert the Debian package using debtap.
- Install using pacman.
- Restore required helper permissions.
- Verify installation.

Reference

- TCR-2026-004

---

# Ninja Remote Player

```bash
./scripts/install-ninjaone.sh
```

Purpose

- Download the latest installer from Nextcloud.
- Convert using debtap.
- Install using pacman.
- Register the ninjarmm URL handler.
- Verify installation.

---

# Framework Audio

Framework Laptop 13 only.

```bash
./scripts/install-framework-audio.sh
```

Purpose

- Select the correct internal microphone.
- Set microphone boost.
- Save ALSA state.
- Verify microphone operation.

Reference

- TCR-2026-006
