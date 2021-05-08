### The following are a few Directory Discovery tools

# GoBuster, is a toll used to brute-force URIs, DNS Subdomains and virtual host names.

Download by **sudo apt-get install gobuster**

Usage:

1. gobuster -u http://<INSERT IP>:<PORT> **-w** /usr/share/wordlists/dirb/common.txt = This will use the wordlist for finding web directories or files.
2. gobuster -e -u <INSERT IP>:<PORT> -w /usr/share/wordlists/dirb/common.txt = This will obtain the full path for a Directory/File. The **-e** option will print complete URLs.
3. gobuster -u http://<INSERT IP>:<PORT> -w /usr/share/wordlists/dirb/common.txt -o result.txt = This will save the output in a file.
4. gobuster -u http://<INSERT IP>:<PORT> -w /usr/share/wordlists/dirb/common.txt **-x .php** = This will enumerate directory with specific extensions. 
5. gobuster dir -u http://<INSERT IP> -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt = This will enumerate website directories. 

Extra wordlist to be familiar with:
1. /usr/share/wordlists/dirbuster/directory-list-2.3-*.txt
2. /usr/share/wordlists/dirbuster/directory-list-1.0.txt
3. /usr/share/wordlists/dirb/big.txt
4. /usr/share/wordlists/dirb/common.txt
5. /usr/share/wordlists/dirb/small.txt
6. /usr/share/wordlists/dirb/extensions_common.txt

# Dirb is a command line based tool to brute force Directory based on wordlists.

Usage:

1. dirb <INSERT URL> = Dirb will search the default word list file. 
