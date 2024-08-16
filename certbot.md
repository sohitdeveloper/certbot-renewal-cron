# first go to the below directory

```
cd /etc/cron.d
```

# create & modify the certbot file

```
sudo vim certbot
```

# execute the below command
```
SHELL=/bin/sh
PATH=/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin
0 */12 * * * root test -x /usr/bin/certbot -a \! -d /run/systemd/system && perl -e 'sleep int(rand(43200))' && certbot -q renew
```
