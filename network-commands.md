1. ping
ping google.com

Checks connectivity between your system and a remote server.

📊 2. netstat
netstat -tuln

Displays network connections, listening ports, and protocols.

🌍 3. ifconfig
ifconfig

Shows network interface details (IP address, MAC, etc).
⚠️ Deprecated in modern systems (use ip instead).

🧭 4. traceroute / tracepath
traceroute google.com
tracepath google.com

Shows the path packets take to reach a destination.

📈 5. mtr
mtr google.com

Combines ping + traceroute for real-time network diagnostics.

🔍 6. nslookup
nslookup google.com

Queries DNS to get IP address of a domain.

🔌 7. telnet
telnet google.com 80

Tests connectivity to a specific port.

🏷️ 8. hostname
hostname

Displays system hostname.

🌐 9. ip
ip a

Shows IP address and network interfaces (modern replacement for ifconfig).

📶 10. iwconfig
iwconfig

Displays wireless network configuration.

🔗 11. ss
ss -tuln

Modern alternative to netstat (faster and more detailed).

🧾 12. arp
arp -a

Displays ARP table (IP ↔ MAC mapping).

🌍 13. dig
dig google.com

Advanced DNS lookup tool.

🔧 14. nc (netcat)
nc -zv google.com 80

Tests port connectivity and transfers data.

🕵️ 15. whois
whois google.com

Displays domain registration details.

🔌 16. ifplugstatus
ifplugstatus

Checks if network cable is connected.

17. route
route -n

Displays routing table (how packets are routed in network).

🔍 18. nmap
nmap localhost

Network scanning tool used to discover:
Open ports
Services running

📥 19. wget
wget https://example.com/file.zip

Downloads files from the internet.

⏱️ 20. watch
watch -n 2 date

Runs a command repeatedly every few seconds.

🔐 21. iptables
sudo iptables -L

Manages firewall rules in Linux.

🧭 22. traceroute (Recap)
traceroute google.com

Tracks the path of packets to destination.

⚔️ 23. curl vs wget
curl
curl https://example.com
Fetches data from URL
Used in APIs
More flexible
wget
wget https://example.com/file.zip
Downloads files
Simple and direct
🔥 Difference
| Feature         | curl      | wget          |
| --------------- | --------- | ------------- |
| Use case        | API calls | File download |
| Output          | Terminal  | Saves file    |
| Resume download | ❌       | ✅             |
