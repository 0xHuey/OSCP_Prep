## Server Message Block

# SMB is a protocol for sharing resources like files, printers or retreivable or made available by the server.

# Runs on port 445 or port 139

# Common enumeration:
1. nmap -p445 --script smb-protocols <INSERT IP>
2. nmap -p139 --script smb-protocols <INSERT IP>

# SMBMap allows users to enumerate samba share drives across an entire domain. List share drives, drive permissions, share contents, upload/download functionality, file name auto-download pattern matching and even execute remote commands.

1. smbmap **-H** <INSERT IP> = Hostnames
2. smbmap -H <INSERT IP> **-R** = Recursive switch so it will go through each directory and list out the files.

# SMBClient will test the connectivity to a Windows share. This can also be used to transfer files or to look at share names. 
1. smbclient **-L** \\\\<INSERT IP> = Displays what services are available on a server.
2. smbclient **-N** -L \\\\<INSERT IP>
3. smbclient \\\\<INSERT IP>\\tmp = Insert a shell.
