# New Machine Checklist

This checklist accompanies the [New Workstation Rollout](workstation-rollout.md).

The goal is to turn a fresh CachyOS installation into a Mono workstation efficiently and consistently while leaving desktop personalization intentional and manual.

> **Automate the repeatable. Synchronize the personal. Document the intentional.**

## Base Installation

- [ ] Install CachyOS
- [ ] Select the desktop environment you intend to keep
- [ ] Connect to the internet
- [ ] Complete all system updates
- [ ] Reboot if required
- [ ] Install and unlock 1Password

## Commissioning

- [ ] Download `commission-workstation.sh` from the Nextcloud commissioning folder
- [ ] Make the script executable
- [ ] Run the commissioning script
- [ ] Confirm Git identity
- [ ] Authenticate GitHub
- [ ] Configure the `monocloud` rclone remote
- [ ] Confirm the workstation repository was cloned
- [ ] Create the machine identity

## Rollout Selection

Choose exactly one rollout:

- [ ] **KDE Plasma** — use the established KDE workstation package set
- [ ] **Desktop-neutral** — use with GNOME, COSMIC, XFCE, or another desktop

The desktop-neutral rollout does not install or configure a desktop environment.

To reopen the selector:

```bash
cd ~/Projects/workstation
./scripts/select-bootstrap.sh
```

## Optional Components

Install only those required on this machine:

- [ ] LucidLink
- [ ] Ninja Remote Player
- [ ] NoMachine
- [ ] ScreenConnect
- [ ] Framework audio troubleshooting, if required
- [ ] Copy the Windows VM into `~/VirtualMachines/Windows11/`
- [ ] Import the Windows VM into Virt-Manager

## Desktop Setup

Configure these manually for the selected desktop environment:

- [ ] Displays, orientation, scaling, and refresh rates
- [ ] Panels, docks, or workspaces
- [ ] Wallpaper
- [ ] Theme and icons
- [ ] Global shortcuts
- [ ] Default terminal
- [ ] Default file manager and desktop applications

## Accounts and Synchronization

- [ ] Sign in to 1Password
- [ ] Sign in to Firefox and allow Sync
- [ ] Sign in to Google Chrome
- [ ] Sign in to Joplin Cloud and enable synchronization
- [ ] Configure Talanoa and add the Fastmail account
- [ ] Sign in to Fastmail
- [ ] Sign in to Discord
- [ ] Pair Signal with the phone
- [ ] Pair KDE Connect only when using it
- [ ] Sign in to Ente Auth
- [ ] Sign in to Nextcloud Desktop

## Completion

- [ ] Configure Microsoft Edge profiles and PWAs
- [ ] Reboot
- [ ] Complete the workstation acceptance test
- [ ] Record any machine-specific exceptions in the documentation
