cat /etc/passwd

# We notice that there is a user with the name 'flag00' but no password

# We searched for the files owned by flag00:
find / -user flag00 2> /dev/null

# For the result:
/usr/sbin/john
/rofs/usr/sbin/john

# We Cat'ed both the files, we notice they contain the same string: cdiiddwpgswtgt
# We tested this string as a password to access the flag00 but didn't worked :(
# So we thinked that is a sort of a crypted password

# We used the famous Website 'www.decode.fr', we tried the Cesar Cipher Identifier (ROT15)
# We saw for the 15 param an understandable words: nottoohardhere

# We used this result and TADAAAAAAA
