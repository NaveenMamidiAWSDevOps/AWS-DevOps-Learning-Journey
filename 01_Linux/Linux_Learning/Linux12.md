

# Linux Commands Cheat Sheet (DevOps Friendly) #

## 1. clear

Purpose: Clears the terminal screen.
Example:
   bash Terminal 
       clear  "*(Same as pressing Ctrl + L in most terminals.)*"


## 2. cal

Purpose: Shows a calendar.
Example:
   bash Teerminal 
       cal 2025   "*(Shows calendar for the year 2025.)*"


## 3. wget

Purpose: Downloads files from the internet (non-interactive).
Example:
    bash Teerminal
         wget https://example.com/file.zip  "*(Downloads file.zip from the given URL.)*"


## 4. tee

Purpose: Shows output on the screen **and** saves it to a file at the same time.
Example:
  bash Teerminal
       ls -l | tee output.txt  "*(Lists files, displays output, and saves it to output.txt.)*"


## 5. script

Purpose: Records your terminal session into a file.
Example:
   bash Terminal 
       script session.log "*(Starts recording to session.log; stop with `exit`.)*"


## 6. ping

Purpose: Checks network connectivity to a host.
Example:
   bash Terminal 
       ping -c 4 google.com "*(Sends 4 ping requests to google.com.)*"


## 7. telnet

Purpose: Connects to a remote host on a specific port.
Example:
    bash Terminal 
        telnet example.com 80  "*(Opens connection to example.com on port 80.)*"


## 8. history

Purpose: Shows recently used commands.
Example
   bash Termianl 
        history  "*(Lists your command history; use `!5` to run command number 5.)*"


## 9. uname

Purpose: Displays system information.
Example:
   bash Terminal 
       uname -a "*(Shows OS type, kernel version, and architecture.)*"


## 10. cat /etc/*release

Purpose: Displays Linux distribution details.
Example:
   bash Terminal "*(Shows OS name, version, and release info.)*"


## 11. netstat

Purpose: Shows network connections and listening ports.
Example:
   bash Terminal 
       netstat -tulnp "*(Shows TCP/UDP ports in use with process IDs.)*"



## 12. watch

Purpose: Runs a command repeatedly at set intervals.
Example:
   bash Trmiank
        watch -n 5 df -h  "*(Runs `df -h` every 5 seconds to monitor disk usage.)*"



