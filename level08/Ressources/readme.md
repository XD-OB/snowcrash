chmod 777 .

# We found:
- ./level08
- token

# It's obvious the file 'token' has the token XD
# But don't have permission to 'cat' it

# We tested with a simple file and got the content

# We try it with 'token' but we got the message:
'You may not access token'
# Even with the binary that have full permission can't access it, we doubt that the problem is the name of the file
# To prove it
echo 'test' > t
chmod -rwx t
./level08 t     ==> We got: Permission denied!

# So we changed the name of 'token'
mv token boken

./level08 boken     ==> password
# Connect to user 'flag08' using the 'password'
getflag

# TADAAAAAAA
