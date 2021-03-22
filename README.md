# snowcrash
Snowcrash is an introductory Cyber Security project, consisting of a virtual machine, containing multiple levels and users.
You have to find a password (flag), for each level to advance to the next.
Some challenges.
#### Objectives:
- Learn to read and write `Perl/Python/Shell scripts`
- Deeply understand `Unix file permissions`, bad practices and how to exploit them.
- Vulnerabilities in `Standard C library` functions and `syscalls`
### Setup the VM:
Use the iso provided in the subject, set the network to bridged to make access to ssh and levels with web easier.
### SSH / SCP
```
ssh -p 4242 levelXX@<ip>
scp -P 4242 levelXX@<ip>:/path/on/the/vm ./path/on/your/machine
```