* copy `config-template.txt` to `config.txt` and fill out token etc
* download the latest jar and update filename in `jmusicbot.service`
* symlink `jmusicbot.service` to `~/.config/systemd/user/jmusicbot.service`
* enable and start the service as the current user via:
```
systemctl --user daemon-reload 
systemctl --user enable jmusicbot.service
systemctl --user restart jmusicbot.service
```
* check status and logs via `systemctl --user status jmusicbot.service`

