# KDE Plasma

## Plasma Login

### Multi-monitor login screen

On a dual-monitor system, Plasma Login initially displayed the login screen on the portrait monitor while the desktop correctly loaded on the landscape monitor.

The fix was to copy the desktop display configuration to the `plasmalogin` user's configuration.

```bash
sudo mkdir -p /var/lib/plasmalogin/.config
sudo cp ~/.config/kwinoutputconfig.json /var/lib/plasmalogin/.config/
sudo chown -R plasmalogin:plasmalogin /var/lib/plasmalogin/.config
```

After rebooting, the login screen appeared on the correct monitor with the proper rotation.
