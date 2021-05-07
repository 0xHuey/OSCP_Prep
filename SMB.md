## Server Message Block

# SMB is a protocol for sharing resources like files, printers or retreivable or made available by the server.

# Runs on port 445 or port 139

# Common enumeration:
1. nmap -p445 --script smb-protocols <INSERT IP>
2. nmap -p139 --script smb-protocols <INSERT IP>
3. nmap -T4 -v -oA shares --script smb-enum-shares --script-args smbuser=username,smbpass=password -p445 <INSERT IP>.0/24 = Find open SMB Shares
4. nmap -sU -sS --script=smb-enum-users -p U:137,T:139 <INSERT IP>.200-254 = Enumerate SMB Users   


# SMBMap allows users to enumerate samba share drives across an entire domain. List share drives, drive permissions, share contents, upload/download functionality, file name auto-download pattern matching and even execute remote commands.

1. smbmap **-H** <INSERT IP> = Hostnames
2. smbmap -H <INSERT IP> **-R** = Recursive switch so it will go through each directory and list out the files.

# SMBClient will test the connectivity to a Windows share. This can also be used to transfer files or to look at share names. 
1. smbclient **-L** \\\\<INSERT IP> = Displays what services are available on a server.
2. smbclient **-N** -L \\\\<INSERT IP>
3. smbclient \\\\<INSERT IP>\\tmp = Insert a shell.

# Enum4Linux is a Linux tool for enumerating from Windows and Samba systems.

1. enum4linux -a <INSERT IP> = Runs all options outside of dictionary based name guessing.
2. enum4linux -U <INSERT IP> = List usernames.
3. enum4linux -r <INSERT IP> = Pull usernames from the default RID range.
4. enum4linux -R <INSERT IP> = Pull usernames using a custom RID range.
5. enum4linux -S <INSERT IP> = List the shares.
6. enum4linux -s <INSERT IP> = Dictionary attack.
7. enum4linux -o <INSERT IP> = Pull OS information using smbclient.8. 
