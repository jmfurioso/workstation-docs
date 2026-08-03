# New Machine Checklist

This document is the companion to `bootstrap.sh`.

The goal is to turn a fresh CachyOS installation into my personal workstation as efficiently and consistently as possible.

**Automate the repeatable. Synchronize the personal. Document the intentional.**

## Initial Setup

- [ ] Install CachyOS with KDE Plasma
- [ ] Install Git
- [ ] Install `paru`
- [ ] Launch Shelly
- [ ] Enable AUR support in Shelly
- [ ] Enable Flatpak support in Shelly
- [ ] Generate a machine-specific SSH key
- [ ] Add the SSH public key to GitHub
- [ ] Clone the workstation repository into `~/Projects/workstation`
- [ ] Install `rclone`
- [ ] Configure the `monocloud` WebDAV remote using the `workstation-rclone` Nextcloud app password
- [ ] Verify access with `rclone lsd monocloud:`

## Restore Environment

- [ ] Run `bootstrap.sh`
- [ ] Log out and back in
- [ ] Verify the Plasma theme and panel appearance
- [ ] Install Kitty
- [ ] Make Kitty the default terminal
- [ ] Install LucidLink
- [ ] Install NinjaRMM
- [ ] Install GameVox
- [ ] Copy the Windows VM into `~/VirtualMachines/Windows11/`
- [ ] Import the Windows VM definition into Virt-Manager

## Accounts & Authentication

- [ ] Sign in to 1Password
- [ ] Sign in to Firefox and allow Sync
- [ ] Sign in to Google Chrome
- [ ] Install Joplin
- [ ] Sign in to Joplin Cloud and enable synchronization
- [ ] Configure Talanoa and add the Fastmail account (`jmarshall@marshallnetworks.com`)
- [ ] Sign in to Fastmail (Flatpak)
- [ ] Sign in to Discord
- [ ] Pair Signal with the phone
- [ ] Pair KDE Connect
- [ ] Sign in to Ente Auth
- [ ] Sign in to Nextcloud Desktop
