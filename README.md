# Security as data analysis
Security can be thought of as data analysis. For example:
<li>An anti-virus sofrware analyzes data about memory and processes in the operating system and compares them with a database of known viruses (signatures).
<li>The network firewall parses the packet headers and compares them to a database called access-list or network policy.
<li>Transactional fraud monitoring systems analyze each transaction using a rule base, desicion tree or more sophisticated databasesd, which can be obtained using AI or mathematical statistics algorithms.
<li>Secure software development lifecycle <mark>SDLC</mark> systems scan source code and compare it with the database of known software vulnerabilities.
<li>Data leakage prevention systems ^^DLP^^ scan content of emails, files and etc and compare it with the database (rule-based systems) or compare with more sophisticated database, which is created using AI and mathemetical statistics algorithms.
<li>Web proxy systems also analyze packet content and search for known vulnerabilties and can block access from corporate network to Dropbox etc. Web prpxy can have 2nd function - analyze repuration of destination site, which is done by comparion of each session to repuration database.
<li>Antispam has a database, which is built using mathematical statistics algothims. Antispam can have also domain-reputaion database. Threrefore antispam system scans each email and it's header against these databases.
<li>App Control works by analyzing content of each packet aganinst a database of known application signatures.
<li>IDS works almost like app control only it analyzes each packet against a database of kbown vulnerabilities. This database is bigger than database of App control.

Threfore if you view security as data analysis (computational tricks, which manipulate data) you can start building your own security system.
Computational tricks, which manipulate data are implemented on hardware CPU, GPU, ASIC and FPGU and software which can work with these hardware.

Next generation firewall (NGFW) has anti-virus/spyware, web-filtering, IDS/IPS, app-control, DLP, anti-spam functions and ofcourse routing, access-lists, VPN and etc. Let's look deeper, which hardware is required to build a security system.

The following table shows which security functions can be implemented on which hardware.
Deep Packet Inspection (DPI), which is required for Next Generation Firewalls (NGFW) or any device, which looks into packet content (not packet header) is mostly implemented in CPU.
Cryptographic functions (SSL decription/encryption) which are requied for VPN gateway or mobile/unified access gateway (UAG) can be boosted via GPU.

|data proceesing device|device/function    |Open Souce Software              |
|:---------------------|:-----------------:|--------------------------------:|
|ASIC, SoC, DPU        |Firewall           |nftables, ebpf                   |
|GPU, CPU              |SSL offloder       |nginx, HAproxy, traefic          |
|GPU, CPU              |VPN                |open vpn, wireguard              |
|GPU, CPU              |UAG                |nginx, HAproxy, traefic          |
|CPU                   |NGFW               |squid+suricata                   |
|CPU                   |IDS                |snort, suricata, zeek            |
|CPU                   |WAF                |nginx, HAproxy, traefik+suricata |
|CPU                   |Web proxy          |squid                            |

Most intellectual security functions, which analyze unstructural and unpredictural data (content) use CPU. Security functions which analyze structural data like packet headers can be boosted via ASIC, SoC, DPU, GPU etc.

Firewall Hardware specification
-----

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