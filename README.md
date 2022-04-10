# fwhw

Anti-Virus/spyware, web filtering, IDS/IPS, app control, DLP, anti-spam

NGFW = UTM = 

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| Cisco|Firepower 4100, 9300 | $1600 |
| Cisco|ASA 5500-X, ASA 5585-X | $1600 |
| Cisco|Firepower 4100, 9300 | $1600 |
| Juniper      | centered        |   $12 |
| Palo Alto |NP7, NP9. SoC4        |    $1 |

|                       |Firepower 4410-4150    |FortiGate 1800F-7121F|
|:----------------------|:---------------------:|--------------------:|
|Firewall               |20-60Gbps              |                     |
|IPSec VPN              |                       |                     |
|Threat Protection      |                       |                     |
|NGFW throuput          |                       |                     |
|SSL inspection         |                       |                     |
|Concurrent sessions    |                       |                     |
|Session per second     |                       |                     |
|Connection rate        |68K-350K/sec           |640K-9M/sec          |


|data proceesing device|device/function    |Open Souce Software              |
|:---------------------|:-----------------:|--------------------------------:|
|ASIC, SoC, DPU        |Firewall           |nftables, ebpf                   |
|GPU, CPU              |SSL offloder       |nginx, HAproxy, traefic          |
|GPU, CPU              |VPN                |open vpn, wireguard              |
|GPU, CPU              |UAG                |nginx, HAproxy, traefic          |
|CPU                   |NGFW               |squid+suricata                   |
|CPU                   |IDS                |snort, suricata, zeek            |
|CPU                   |WAF                |nginx, HAproxy, traefik+suricata |
|CPU                   |Web proxy          |68K-350K/sec                     |