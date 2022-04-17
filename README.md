# Open source cybersecurity software

The following table lists open source software, which can be installed on Linux server to create an appliance and replace vendor's proprietary hardware.
<br>Hardware server + open source software = applicance.

|cybersecurity function                                          |open source software                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------|
|firewall                                                        |nftables, XDP, packet filter, npf, shorewall                          |
|web proxy<br>SSL offloader<br>reverse proxy                     |squid, HAproxy, traefik, nginx, varnish, apache traffic server, pound |
|unified access gateway<br>identity gateway<br>app gateway       |OpenIG, OWASP application gateway                                     |
|WAF                                                             |modsecurity, ironbee, NAXSI, shadow daemon, lua-resty-way, vulture    |
|NGFW                                                            |OPNSense, pfsense, ipfire                                             |
|url filtering<br>content filtering                              |squid guard, dans guarding                                            |
|DPI tools                                                       |nDPI                                                                  |
|VPN                                                             |open vpn, wireguard                                                   |
|IDS<br>IPS<br>threat detection                                  |snort, suricata, zeek                                                 | 
|antispam<br>mail gateway                                        |spam assasin, mail scanner, ASSP, proxmox, orange assasin             |
|sandbox                                                         |cuckoo                                                                |
|antiDDoS                                                        |gatekeeper, fastnetmon, crowdsec                                      |

Next-generation firewall characteristics:

|charactestic                          |Cisco      | Palo Alto | Fortinet  | Juniper   | Hillstone |Checkpoint |
|--------------------------------------|-----------|-----------|-----------|-----------|-----------|-----------|
|firewall throuput                     |650Mb-235Gb|535Mb-697Gb|800Mb-1,9Tb|1Gb-1Tb    |1Gb-1,2Tb  |3,3Gb-800Gb|
|NGFW throuput<br>App ID throuput      |650Mb-190Gb|500Mb-697Gb|800Mb-550Gb|100Mb-400Gb|400Mb-280Gb|1,5Gb-51Gb | 
|IPS throuput<br>theat protection      |650Mb-190Gb|150Mb-405Gb|600Mb-675Gb|200Mb-860Gb|610Mb-400Gb|2Gb-52Gb   |
|IPSec VPN throuput                    |150Mb-110Gb|100Mb-334Gb|950Mb-63Gb |300Mb-230Gb|620Mb-500Gb|3,3Gb-44Gb |
|VPN peers<br>VPN tunnels              |75-60k     |500-60k    |200k-26k   |250-40k    |512-20k    |200-20k    |
|concurrent session                    |3m-195m    |64k-416m   |700k-1000m |64k-338m   |300k-480m  |2m-49m     |
|sessions per second<br>Connetion rate |40k-1,1m   |4k-6m      |35k-9m     |5k-7,5m    |15k-10m    |32k-690k   |

Findings:
<li> All hardware firewall vendors have almost the same hardware.
<li> Firewall pps-capabilities do differ -  firewall with low pps could be taken out by pps-DDoS.
<li> Intelligent packet processing like App ID, NGFW, IPS, threat protection is a non-technical speculative term and it's performance depends on how many rules vendor integrated into IPS, threat protection etc. 
