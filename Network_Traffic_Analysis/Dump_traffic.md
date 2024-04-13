# TCP Dump

## install
```
sudo apt install tcpdump 
```
## Arguments
| Switch Command | Result                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------|
| D              | Will display any interfaces available to capture from.                                                      |
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

