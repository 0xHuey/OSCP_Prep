# Network Mapper (NMAP) is a free and open-source network scanner. This is used for network discover purposes but its extremely powerful.

# Some of the things you can do in Nmap:

1. Host Discovery
2. Port Scanning
3. Version detection
4. OS Detection
5. Scriptable interaction with the target.


# This isn't meant to be a full list but a quick cheatsheet for running nmap:

1. -sV = Standard service detection
2. -sC = Default safe Scripts
3. -A = Detect OS and Services
4. -oN namp.txt = Save default output to a file
5. -sT = TCP Connect 
6. -sU = UDP Scan
7. -sF = TCP FIN Scan
8. -p- = Scan all ports

# Vulnerability Scan 

1. --script=vuln = Vulnerability NSE scan
2. --script=smb-enum-users,smb-enum-shares = Multiple scripts

# HTTP Information

1. --script=http-tittle = Page titles from HTTP Services
2. --script=http-headers = Get HTTP headers of web services 
3. --script=http-enum = Find web apps from paths
