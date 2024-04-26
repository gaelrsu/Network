# Wireshark 

## Filters 

| Capture Filters      | Result                                                                                       |
|----------------------|----------------------------------------------------------------------------------------------|
| host x.x.x.x        | Capture only traffic pertaining to a certain host                                             |
| net x.x.x.x/24      | Capture traffic to or from a specific network (using slash notation to specify the mask)      |
| src/dst net x.x.x.x/24 | Using src or dst net will only capture traffic sourcing from the specified network or destined to the target network |
| port #               | Will filter out all traffic except the port you specify                                       |
| not port #          | Will capture everything except the port specified                                              |
| port # and #        | AND will concatenate your specified ports                                                      |
| portrange x-x       | Portrange will grab traffic from all ports within the range only                               |
| ip / ether / tcp    | These filters will only grab traffic from specified protocol headers                           |
| broadcast / multicast / unicast | Grabs a specific type of traffic: one to one, one to many, or one to all                   |
