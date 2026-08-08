# ✅ Workstation Acceptance Test

Complete this checklist before considering a workstation rollout finished.

Only check components that apply to this machine.

---

# Operating System

- [ ] CachyOS fully updated
- [ ] Reboot completed successfully
- [ ] Network connectivity working
- [ ] No unresolved package errors

---

# Commissioning

- [ ] Git identity configured
- [ ] GitHub authenticated
- [ ] `~/Projects/workstation` cloned
- [ ] `machine.conf` contains the correct workstation name
- [ ] `monocloud:` rclone remote configured
- [ ] Nextcloud access verified
- [ ] Bootstrap completed successfully

---

# Core Applications

- [ ] 1Password working
- [ ] Firefox launches and is synchronized
- [ ] Google Chrome launches
- [ ] Microsoft Edge launches
- [ ] Required standard applications are present

---

# Component Installers

Verify only the components required on this workstation.

## LucidLink

- [ ] LucidLink installed
- [ ] Login successful
- [ ] Required filespace mounts correctly

## ScreenConnect

- [ ] ScreenConnect installed
- [ ] Client online and usable

## NoMachine

- [ ] NoMachine installed
- [ ] Remote connection works

## Ninja Remote Player

- [ ] Ninja Remote Player installed
- [ ] NinjaOne remote-session links open correctly

## Framework Audio

Framework hardware only.

**Test the audio hardware before applying any workaround.**

- [ ] Internal microphone tested before making changes
- [ ] Internal microphone works normally

If the microphone does **not** work correctly:

- [ ] Investigate the detected audio hardware and profile
- [ ] Determine whether the problem matches the known FW13 microphone issue
- [ ] Run `install-framework-audio.sh` only if the known workaround is applicable
- [ ] Retest the internal microphone after remediation

The Framework audio installer is a troubleshooting tool, not a standard requirement for every Framework laptop.

---

# Microsoft Edge Profiles

- [ ] Inside profile configured
- [ ] SOS profile configured
- [ ] Tagwall profile configured

---

# Teams PWAs

- [ ] Teams — Inside launches
- [ ] Teams — SOS launches
- [ ] Teams — Tagwall launches

---

# Outlook PWAs

- [ ] Outlook — Inside launches
- [ ] Outlook — SOS launches
- [ ] Outlook — Tagwall launches

---

# Framework Hardware

Framework laptops only.

- [ ] Internal microphone verified
- [ ] Speakers verified
- [ ] Webcam verified
- [ ] Wi-Fi verified
- [ ] Bluetooth verified
- [ ] Suspend/resume works
- [ ] Function keys behave normally

Do not assume hardware-specific fixes from another Framework model are required.

Test the new machine first and remediate only demonstrated problems.

---

# Desktop Personalization

These items are manual and do **not** need to match another workstation.

- [ ] Preferred Plasma theme configured
- [ ] Window decorations usable
- [ ] Panel/layout usable
- [ ] Application launcher works
- [ ] Preferred wallpaper selected
- [ ] Required keyboard shortcuts configured

The goal is a comfortable, functional desktop—not an identical clone of another machine.

---

# Final Validation

- [ ] Normal reboot succeeds
- [ ] No unexpected startup errors
- [ ] Required applications launch
- [ ] Required remote-access tools work
- [ ] Required cloud storage is accessible
- [ ] Microsoft PWAs work
- [ ] Desktop is comfortable for daily use

---

# Complete

- [ ] **Mono's Workstation is ready for daily use**
