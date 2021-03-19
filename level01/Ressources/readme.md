# Find the password of Flag01

## First check :
Home directory : \[x\] empty.

## next ..

As we _catted_ the `/etc/passwd` file looking for a hint for **flag00**, we kept in mind that the user **flag01** has actually a hashed code `42jkfhgjkf` in the password placeholder.

## Google it.

Naively, we looked for a tool to crack a hashed password in `/etc/passwd`.

Turned out there is a famous password cracker called [John The Ripper](https://askubuntu.com/questions/427770/can-users-passwords-be-cracked-from-etc-shadow-file).

...
...
...

```
./john "42jkfhgjkf"
> abcdefg
```

## TADAAAAAAA, It's indeed the flag01 password !

_tobecontinued_

> getflag
> [next level flag](https://github.com/XD-OB/snowcrash/blob/master/level01/flag)
