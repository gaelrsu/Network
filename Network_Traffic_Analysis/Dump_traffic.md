# TCP Dump

## install
```
sudo apt install tcpdump 
```
## Arguments
| Switch Command | Result                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------|
| D              | Will display any interfaces available to capture from.                                                      |
| A              | Looking for something human readable                                                                       |
| i              | Selects an interface to capture from. ex. -i eth0                                                           |
| n              | Do not resolve hostnames.                                                                                  |
| nn             | Do not resolve hostnames or well-known ports.                                                               |
| e              | Will grab the ethernet header along with upper-layer data.                                                  |
| X              | Show Contents of packets in hex and ASCII.                                                                  |
| XX             | Same as X, but will also specify ethernet headers. (like using Xe)                                          |
| v, vv, vvv     | Increase the verbosity of output shown and saved.                                                           |
| c              | Grab a specific number of packets, then quit the program.                                                   |
| s              | Defines how much of a packet to grab.                                                                      |
| S              | Change relative sequence numbers in the capture display to absolute sequence numbers. (13248765839 instead of 101) |
| q              | Print less protocol information.                                                                            |
| r file.pcap    | Read from a file.                                                                                          |
| w file.pcap    | Write into a file.                                                                                         |

## Filters

| Filter      | Result                                                                                      |
|-------------|---------------------------------------------------------------------------------------------|
| host        | Filters traffic involving the designated host (bi-directional).                             |
| src / dest  | Modifiers to designate source or destination host or port.                                  |
| net         | Shows traffic from or destined to the designated network (uses / notation).                |
| proto       | Filters for a specific protocol type (e.g., ether, TCP, UDP, ICMP).                         |
| port        | Shows traffic with the specified port as the source or destination (bi-directional).        |
| portrange   | Specifies a range of ports (e.g., 0-1024).                                                   |
| less / greater "< >" | Looks for packets or protocol options of a specific size.                                |
| and / &&    | Concatenates two different filters together (e.g., src host AND port).                       |
| or          | Matches on either of two conditions (does not have to meet both; can be tricky).             |
| not         | Excludes traffic matching the specified condition (e.g., not UDP).                           |

### Exemple :
```
sudo tcpdump -i eth0 host 172.16.14.20
sudo tcpdump -i eth0 src host 172.16.14.20
sudo tcpdump -i eth0 tcp src port 53
sudo tcpdump -i eth0 proto 64003
sudo tcpdump -i eth0 tcp port 443
sudo tcpdump -i eth0 portrange 0-1024
sudo tcpdump -i eth0 host 192.168.0.1 and port 23 or port 2300
sudo tcpdump -r my.pcap not icmp
sudo tcpdump -Ar my2.cap -l | grep 'mailto:*'
sudo tcpdump -i eth0 'tcp[13] &2 != 0'     => looking for SYN
```







