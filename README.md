# Hacking-Tool
https://www.whois.com/whois
https://wigle.net/
https://gchq.github.io/CyberChef/

exiftool <bild.png>

## Nmap
nmap -A -p 22,80,443 <ip>
nmap --script vuln -p 22,80,443 <ip>

### Sort file and remove duplication
sort "file" | uniq > sort_"file"
wc -l sort_"file"
