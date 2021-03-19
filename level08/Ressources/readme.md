# Find the password of Flag08

## First check :
Home directory : \[✓\] not empty.
- ./level08
- token

## My home, my rules.

```
chmod 777 .
```

## Run it :
To run the `./level08` properly, it needs a file, which might be `token`, which also contains the token obviously, or maybe ... ?

We first tried it with a simple file we created, it returned our file's content.
So, let's try it with the token file.

```
./level08` token
> 'You may not access token'
```

Even with the binary that have full permission, it couldn't access it.
We doubted that the problem is in the name of the file, not the access rights.

```
echo 'filecontent' > filename
chmod -rwx filename
./level08 filename
> Permission denied
```

We'll definitely change the token file name and test.

```
mv token broken
./level08 broken
```

aand ... 
## TADAAAAAAA, It's indeed the flag08 password !

_tobecontinued_

> getflag
> [next level flag](https://github.com/XD-OB/snowcrash/blob/master/level08/flag)