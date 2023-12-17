# Open source cybersecurity software

The following table lists open source software, which can be installed on Linux server to create an appliance and replace vendor's proprietary hardware.
<br> :white_check_mark: `Hardware server` + `linux` + `open source software` = `appliance`

|cybersecurity function                                          |open source software                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------|
|`firewall`                                                      |system tools: `nftables` `XDP` `packet filter` `npf` `shorewall` <br> firewall distros: `opnsense` `pfsense` `VyOS` `ClearOS` `ipfire` `zentyal` `webadmin` `cockpit` `xWRT`|
|`web proxy` `SSL offloader` `reverse proxy`                     |`squid` `HAproxy` `traefik` `nginx` `varnish` `apache traffic server` `pound`|
|`unified access gateway` `identity gateway` `app gateway`       |`OpenIG` `OWASP` `application gateway`                                       |
|`WAF`                                                           |`modsecurity` `ironbee` `NAXSI` `shadow daemon` `lua-resty-way` `vulture`    |
|`NGFW`                                                          |`OPNSense` `pfsense` `ipfire`                                                |
|`url filtering` `content filtering`                             |`squid guard` `dans guarding`                                                |
|`DPI tools`  `AppID` `Application visibility`                   |`nDPI` `nTop`                                                                |
|`VPN`                                                           |`open vpn` `wireguard`                                                       |
|`IDS` `IPS` `threat detection` `threat defence`                 |`snort` `suricata` `zeek` `sensei`                                           | 
|`antispam` `mail gateway`                                       |`spam assasin` `mail scanner` `ASSP` `proxmox` `orange assasin`              |
|`sandbox`                                                       |`cuckoo` `firejail`                                                                     |
|`antiDDoS`                                                      |`gatekeeper` `fastnetmon` `crowdsec`                                         |
|`antivirus`                                                     |`clamAV`                                                                     |

# Open Source firewall (and router+fw) operating system comparison
|firewall<br>distro |linux<br>distro        |packet manager|latest release|techological<br>stack                       |arch       |comments            |
|-------------------|-----------------------|--------------|--------------|--------------------------------------------|-----------|--------------------|
|opnsense<br>pfsense|xBSD                   |yes           |2023          |`JavaScript` `PHP` `Shell`                  |`x86`        |One of the most common products, a fairly simple and logical core. Firewall, QOS are implemented differently from linux. There are performance and hardware issues (NICs)|
|VyoS               |Debian 10              |monolthic+deb |2023          |`Python/Django` `Perl`                    |`x86` `ARM` |More router than a firewall. Has server control tools. Has CLI.| 
|ClearOS            |RHEL/CentOS            |rpm           |2020          |`JavaScript` `PHP` `Shell` `C++` `Python` |`x86`        |More of a server management tool than a firewall. Although they are affiliated with HP. Possible to use with Cockpit.|
|ipfire             |linux                  |no            |2023          |`Perl(Raku)` `C` `Shell`                   |`x86` `ARM`|Specialized distribution  for creating a firewall|
|zentyal            |ubuntu                 |dpkg          |2021          |`JavaScript` `Perl` `Shell`                  |`x86`        |More server management tool than a firewall|
|webadmin           |any, works on Debian 10|any           |2023          |`Perl`                                         |`many`       |More server management tool than a firewall. Firewall interface is limited.|
|cockpit            |any, works on Debian 10|any           |2023          |`JavaScript` `C` `Python`                    |`many`       |A more modern analogue of Webmin|
|xWRT               |linux                  |ipkg          |2023          |`JavaScript` `C` `Lua`                       |`ARM` `MIPS`|Solution for creating a firewall on low end hardware|

Findings: No open-source analogue for `Cisco Security Manager.`
