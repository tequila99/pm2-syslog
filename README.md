# pm2-syslog

Redirect all logs of PM2 + Apps managed into `/var/log/syslog`

## Configure OS

Edit `/etc/rsyslog.conf` and uncomment:

```
# provides UDP syslog reception
module(load="imudp")
input(type="imudp" port="514")
```

Restart rsyslog:

```
$ sudo service rsyslog restart
```

## Install module

```
# Install
$ pm2 install @tequila99/pm2-syslog

# Test
$ pm2 start "ls -la"

# Uninstall
$ pm2 uninstall @tequila99/pm2-syslog
```

# License

MIT
