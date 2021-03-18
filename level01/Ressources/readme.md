# We Cat'ed the file: /etc/passwd
# We noticed that the user flag01 is the only one that has a weird password
# We did some research crack passwords and found that there is a tool named 'John The Ripper'
# https://askubuntu.com/questions/427770/can-users-passwords-be-cracked-from-etc-shadow-file
# We used the tool as follow
./john "42jkfhgjkf"
# We got the result: abcdefg
# We used this password and TADAAAAAAAA