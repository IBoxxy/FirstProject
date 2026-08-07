sudo nano /etc/systemd/logind.conf

#HandleLidSwitch=suspend
#HandleLidSwitchExternalPower=suspend
#HandleLidSwitchDocked=ignore

HandleLidSwitch=ignore
HandleLidSwitchExternalPower=ignore
HandleLidSwitchDocked=ignore

sudo systemctl restart systemd-logind

gsettings set org.gnome.settings-daemon.plugins.power sleep-inactive-ac-timeout 0

sudo systemctl status ssh
