# Network Mapper (NMAP) is a free and open-source network scanner. This is used for network discover purposes but its extremely powerful.

# Some of the things you can do in Nmap:

1. Host Discovery
2. Port Scanning
3. Version detection
4. OS Detection
5. Scriptable interaction with the target.


# This isn't meant to be a full list but a quick cheatsheet for running nmap:

-sV = Standard service detection
-sC = Default safe Scripts
-A = Detect OS and Services
-oN namp.txt = Save default output to a file
-sT = TCP Connect 
-sU = UDP Scan
-sF = TCP FIN Scan
-p- = Scan all ports

# Vulnerability Scan 

--script=vuln = Vulnerability NSE scan
--script=smb-enum-users,smb-enum-shares = Multiple scripts

# HTTP Information

--script=http-tittle = Page titles from HTTP Services
--script=http-headers = Get HTTP headers of web services 
--script=http-enum = Find web apps from paths
