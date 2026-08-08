# 🧰 Component Installers

Component installers handle applications that require additional setup beyond normal package installation.

During bootstrap, you may be offered these installers interactively.

Install only the components required on the workstation.

---

# LucidLink

```bash
./scripts/install-lucidlink.sh
```

## Purpose

Installs the LucidLink client on CachyOS/Arch.

The installer handles the additional work required for the Debian-distributed application, including:

- Downloading the installer from Nextcloud
- Converting the Debian package for Arch
- Installing the converted package with pacman
- Restoring required privileged-helper permissions
- Verifying installation

## After Installation

Launch LucidLink and:

1. Sign in.
2. Connect to the required filespace.
3. Verify that the filespace mounts correctly.

---

# ScreenConnect

```bash
./scripts/install-screenconnect.sh
```

## Purpose

Installs the ScreenConnect client used for remote support.

## After Installation

Verify:

- The client launches
- The workstation appears online
- A remote session can be established

---

# NoMachine

```bash
./scripts/install-nomachine.sh
```

## Purpose

Installs NoMachine for remote desktop access.

## After Installation

Verify:

- NoMachine services are running
- The workstation is reachable
- A remote session can be established

---

# Ninja Remote Player

```bash
./scripts/install-ninjaone.sh
```

## Purpose

Installs the NinjaOne Remote Player used to access remote workstations.

The installer handles the non-native package installation and registers the:

```text
ninjarmm:
```

URL handler.

## After Installation

Verify that a NinjaOne remote-session link launches the Remote Player.

!!! note

    This installs the **NinjaOne Remote Player**, not the NinjaOne RMM agent.

    Personal workstations do not require the RMM agent.

---

# Framework Audio

```bash
./scripts/install-framework-audio.sh
```

!!! warning

    **Do not run this automatically on a new Framework laptop.**

    This installer exists to remediate the known microphone problem encountered on the FW13.

    New Framework hardware may use a different audio implementation and may not require this workaround.

## First Test the Hardware

Before running the installer:

1. Test the internal microphone.
2. Test the speakers.
3. Confirm the correct audio devices appear.
4. Verify normal microphone input levels.

If everything works normally:

**Do not run the Framework Audio installer.**

## If the Microphone Has Problems

Investigate the detected hardware and audio profile first.

Run:

```bash
./scripts/install-framework-audio.sh
```

only if the symptoms match the known FW13 issue and the workaround is appropriate for that hardware.

After applying the workaround:

- Retest microphone input
- Reboot if necessary
- Confirm the fix persists

---

# Manual Installation

Component installers can be run at any time from:

```bash
cd ~/Projects/workstation
```

then:

```bash
./scripts/install-<component>.sh
```

They do not need to be run during the initial bootstrap.

---

# Rule of Thumb

**Normal application?**

Let the package lists and bootstrap handle it.

**Application requires special installation or configuration?**

Use a component installer.

**Hardware-specific workaround?**

Test the hardware first and apply the workaround only when required.
