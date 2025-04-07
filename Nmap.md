### NMAP
## IDS/IPS Evation
sudo nmap <IP>  -p22 -sS -Pn -n --disable-arp-ping --packet-trace -O -sV

sudo nmap -sSU -p 53 --script dns-nsid <IP> -Pn -n --disable-arp-ping --packet-trace -D RND:50 --max-retries 50 --version-intensity 9 -sV

nmap <IP> -p50000 -sS -Pn -n --disable-arp-ping --packet-trace --source-port 53

nc -nv -p 53 <IP> <puerto_destino>

| Flag | Description |
| ------------- |:-------------:|
| --disable-arp-ping | --disable-arp-ping |
|--packet-trace| Shows all packets sent and received.|
|-sA|Performs ACK scan on specified ports|
|-n|Disables DNS resolution.|
|-Pn|Disables ICMP Echo requests.|
|-sA|Performs ACK scan on specified ports.|
|-D RND:5|Generates five random IP addresses that indicates the source IP the connection comes from.|
|--source-port 53|Performs the scans from specified source port.|

---
