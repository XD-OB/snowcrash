# Find the password of Flag00

## First check :
Home directory : \[x\] empty.

## Second check :
We checked the /etc/passwd with no results.
We thought about looking for files owned by flag00.

> find / -user flag00 2> /dev/null

## Results:

User flag00 has access to 2 similar files.

> /usr/sbin/john
> /rofs/usr/sbin/john

They both contain an str: `cdiiddwpgswtgt`

Unfortunaltely, it's not the password we're looking for.
Maybe it's encrypted.
Using [dcode](https://www.dcode.fr), we tried randomly the decryption tools.

The Cesar Cipher Identifier (ROT15) gave a readable string of the file: `nottoohardhere`

## TADAAAAAAA, It's indeed the flag00 password !

_tobecontinued_

> getflag
> [next level flag](https://github.com/XD-OB/snowcrash/blob/master/level00/flag)