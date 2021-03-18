# Find the password of Flag05

Once we logged in, we received a mail.


```
$ cat /var/mail/level05
$ */2 * * * * su -c "sh /usr/sbin/openarenaserver" - flag05
```

## Translation :
The mail means that crontab executed a script every 30s
On run, the script `/usr/sbin/openarenaserver` execute all the shell scripts in the directory `/opt/openarenaserver/` and remove them.

#### Could you run our getflag please ?
We create a file to log in the result of the script that will be run by the crontab `touch /tmp/flag` .

We create the following script in the `/opt/openarenaserver/` directory.

```
#!/bin/sh

echo getflag > /tmp/flag
```

Once it's run and deleted, we simply cat the `/tmp/flag`

## TADAAAAAAA, It's ... 
[The next level flag](https://github.com/XD-OB/snowcrash/blob/master/level05/flag)

_tobecontinued_