# Find the password of Flag07

## First check :
Home directory : \[✓\] not empty.

We found 1 executable file `./level07`

## Run it :
It printed its name.
Maybe if we modify it we could inject a command ?
```
chmod 777 .
mv level07 executemepls
./executemepls
> level07
```
We expected the output to change but it was negative, so, let's do it as before.

## Binary ? hexdump !

In the hexdump we noticed that it `echo` the value of the `env variable 'LOGNAME'`

```
export LOGNAME=\`getflag\`
./level07
```

## TADAAAAAAA, It's ... 
[The next level flag](https://github.com/XD-OB/snowcrash/blob/master/level07/flag)

_tobecontinued_