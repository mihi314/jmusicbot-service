* copy `config-template.txt` to `config.txt` and fill out token etc
* download the latest [JMusicBot jar](https://github.com/jagrosh/MusicBot/releases) and update the filename in `jmusicbot.service`
* symlink `jmusicbot.service` to `~/.config/systemd/user/jmusicbot.service`
* enable and start the service as the current user via:
```
systemctl --user daemon-reload 
systemctl --user enable jmusicbot.service
systemctl --user restart jmusicbot.service
```
* check status and logs via `systemctl --user status jmusicbot.service`
* maybe [automatically start the systemd user instance on startup](https://wiki.archlinux.org/title/systemd/User#Automatic_start-up_of_systemd_user_instances) with `loginctl enable-linger <username>`
