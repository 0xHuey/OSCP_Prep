# Quick commands to run once you get access to a Linux Machine

1. sudo -l = Will show allowed commands for the invoking user on the current host. 
2. ps = Will show the current processes running on the system.
3. ps aux = Display current processes snapshot
4. find / -perm -4000 -type f -exec ls -la {} 2>/dev/null \; = Will print SUID binaries
5. find / -uid 0 -perm -4000 -type f 2>/dev/null = Will print SUID binaries
6. find / -perm -4000 2>/dev/null = Search for SetUID binaries
7. ps aux | grep tmux = will shouw you if tmux is running on the system. Tmux is a terminal multiplexer.

# Priv Esc Tools
1. wget https://github.com/ohpe/juciy-potato/release/download/v0.1/JuicyPotato.exe


