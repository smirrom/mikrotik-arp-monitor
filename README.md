# mikrotik-arp-monitor
Mikrotik script for monitoring new MACs in /ip arp and sends notification to email and log.

## Installation
Before using script need to create empty knownmacs.txt file by using theese commands:                                         
> /file print file=knownmacs.txt
> /file set knownmacs.txt contents=""

For periodic check need to create scheduler task:

> /system scheduler add interval=1m name=macwatch on-event="/system script run mikrotik-arp-monitor"
