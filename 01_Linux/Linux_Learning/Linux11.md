
# 🖥️ Linux Admin Cheatsheet

## 🔐 Remote Access Control

- `ssh` – Secure Shell  
  Use to log in to another machine securely.

  # bash
  ssh user@remote_host


* `scp` – Secure Copy
  Securely copy files between local and remote systems.

  #bash
  scp file.txt user@remote_host:/path/to/destination
  


## 🧠 Hardware Information Commands

* `free` – Show memory usage (RAM).

  # bash
  free -h
 

* `dmidecode -t 17` – Show RAM details: type (DDR2/DDR3/etc), speed, manufacturer, etc.
  ⚠️ Requires **root** privileges.

  # bash
  sudo dmidecode -t 17
  

* `vmstat` – Show virtual memory statistics (processes, memory, I/O, etc.)

  # bash
  vmstat
  

## 📬 Communication Commands

* `mail` – Send and receive system emails (server must have mail configured).

  # bash
  mail user@example.com
  


