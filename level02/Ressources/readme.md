# Find the password of Flag02

## First check :
Home directory : \[✓\] not empty.

Unlike the previous levels, we found a file with the `.pcap` extension.

## Google it.

[pcap](https://en.wikipedia.org/wiki/Pcap) files are data files where the packet data of a network is stored. To open it, we copied the file to our local machine `scp -P 4242 level02@localhost:/home/user/level02/level02.pcap .` and used [Wireshark].

We examined the data flowing between the client & the server i.e `Follow TCP Stream`, and found the characters typed during a login. After removing the deleted characters (*as backspace is represented by dots*) we got `ft_waNDReL0L` .

## TADAAAAAAA, It's indeed the flag02 password !

_tobecontinued_

> getflag
> [next level flag](https://github.com/XD-OB/snowcrash/blob/master/level02/flag)