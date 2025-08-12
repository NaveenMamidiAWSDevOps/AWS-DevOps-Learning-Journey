

# Shell Scripting Basics – Class Notes

## 1. Common Linux Commands

| Command                     | What it does                          |
| --------------------------- | ------------------------------------- |
| `free`                      | Shows memory usage                    |
| `df`                        | Shows disk usage                      |
| `top`                       | Shows running processes               |
| `dbbackup.sh`               | Custom script – takes database backup |
| `Serverresourcesmonitor.sh` | Custom script – monitors server       |
| `deploy.sh`                 | Custom script – deploys code          |
| `cleanup.sh`                | Custom script – cleans old files/logs |
| `mail`                      | Sends email from the terminal         |
| `echo`                      | Prints text                           |
| `hostname`                  | Shows server’s name                   |
| `ifconfig`                  | Shows network info                    |

---

## 2. Monitoring Tools

* **Grafana** → For creating dashboards & monitoring.
* **NewRelic** → For application performance tracking.



## 3. Before You Start

* Have access to Linux/Unix server.
* Know basic Linux commands.
* Know basic programming (loops, conditions, variables).



## 4. Writing a Shell Script

1. Open an editor (e.g., `vi`, `gedit`):

   bash
   vi scriptname.sh
   
2. Add the shebang line at the top:

   bash
   #!/bin/bash
  
3. Write your script code.
4. Give execute permission:

   bash
   chmod +x scriptname.sh
   
5. Run it:

   bash
   ./scriptname.sh
   

   *(or `bash scriptname.sh`)*

---

## 5. Command Line Arguments (CLA)

* Values given when running the script.
* Examples:

  * `$#` → number of arguments
  * `$*` → all arguments as one string
  * `$@` → all arguments separately
  * `$$` → process ID of the script
  * `$?` → exit status of the last command

---

## 6. Comparison Operators

| Symbol | Meaning               |
| ------ | --------------------- |
| `-eq`  | equal to              |
| `-ne`  | not equal             |
| `-lt`  | less than             |
| `-le`  | less than or equal    |
| `-gt`  | greater than          |
| `-ge`  | greater than or equal |

---

## 7. String Operations

```bash
String_var="Hello Team, I am learning Shell Scripting"

echo "${String_var:6}"       # from index 6
echo "${String_var:10:5}"    # from index 10, length 5
echo "${String_var: -8}"     # last 8 characters
```



## 8. Arithmetic Operations

bash
expr 2 + 3     # addition
expr 10 - 2    # subtraction
expr 10 / 2    # division
expr 2 \* 3    # multiplication
expr 20 % 3    # remainder





