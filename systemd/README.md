Systemd Timers

Systemd timers can be used as an alternative to cron. To use these timers, simply
drop all 4 files into `/etc/systemd/system/` and then run:

```
systemctl enable burndownmonth.timer
systemctl enable burndowndaily.timer
systemctl start  burndownmonth.timer
systemctl start  burndowndaily.timer
```

You can check the status of systemd timer jobs with `systemctl list-timers --all`.

See the
[systemd.timer](http://www.freedesktop.org/software/systemd/man/systemd.timer.html)
manpage for more details.
