# Text Reading / Display Commands #


* 1. echo       - for display purpose we will use like system.out.println ( ) method in java.
* 2. cat        - Display the contents of a file .
* 3. head       - print the first 10 lines of each FILE to standard output.
* 4. tail       - it will display the last 10 rows.
* 5. more       - it is a Filter for paging through text one Screenful at a time.( stops the display on each screen ).
* 6. less       - less is the same except you can scroll back and forward.
* 7. sort       - it is used to sort the outputin numeric or alphabetic order.
* 8. tr         - Translate Characters.
* 9. sed        - Stream Editor.
* 10. grep      - which stands for " global regular expression print " processes text line and prints any lines which match a specified pattern.




## 1️⃣ echo - Display Messages
Used for printing output (similar to `System.out.println()` in Java).

### ✅ Real-time Examples

echo "Welcome to DevOps Automation!"

📌 Displays a simple message.


echo "PATH Variable: $PATH"

📌 Prints the system's PATH variable.


## 2️⃣ cat - Display File Contents**
Concatenates and displays the content of a file.

### ✅ Real-time Examples

cat /var/log/syslog

📌 Reads system logs in real-time.


cat /etc/passwd | grep "ubuntu"

📌 Searches for a specific user in the system.



## 3️⃣ head - Show First 10 Lines
By default, it prints the first 10 lines of a file.

### ✅ Real-time Examples

head -15 /var/log/auth.log

📌 Displays the first 15 lines of the authentication logs.


head -n 20 access.log

📌 Shows the first 20 lines of the web server log.



## 4️⃣ tail - Show Last 10 Lines
By default, it prints the last 10 lines of a file.

### ✅ Real-time Examples

tail -f /var/log/syslog

📌 Continuously monitors live system logs in real-time.


tail -n 50 application.log

📌 Shows the last 50 lines of an application log.



## 5️⃣ more - Paginated File Viewing**
Allos you to read a file page by page.

### ✅ Real-time Examples

more /var/log/dmesg

📌 Reads kernel logs page by page (press `Space` to move forward).

cat largefile.txt | more

📌 Reads a large text file without overloading the screen.



## 6️⃣ less - Scrollable File Viewer**
Similar to `more`, but allows scrolling forward & backward.

### ✅ Real-time Examples

less /etc/nginx/nginx.conf

* Opens and scrolls through the Nginx configuration file.


journalctl -xe | less

📌 Views system logs interactively.


## 7️⃣ sort - Sort Text Data
Sorts a file alphabetically or numerically.

### ✅ Real-time Examples

sort users.txt

📌 Sorts a list of usernames alphabetically.


sort -n sales.txt

📌 Sorts sales numbers numerically. 


## 8️⃣ tr - Translate Characters
Used to convert case, delete characters, or replace text.

### ✅ Real-time Examples

echo "hello world" | tr 'a-z' 'A-Z'

📌 Converts lowercase to uppercase.


echo "123-456-789" | tr -d '-'

📌 Removes dashes from a phone number.



## 9️⃣ sed - Stream Editor (Find & Replace)
Edits a file without opening it.

### ✅ Real-time Examples

sed 's/error/success/g' logfile.txt

📌 Replaces all occurrences of "error" with "success".


sed -i 's/localhost/192.168.1.100/g' config.yaml

📌 Replaces "localhost" with an IP address in a config file.


## 🔟 grep - Search for Patterns
Finds and prints lines containing a specific pattern.

### ✅ Real-time Examples

grep "ERROR" /var/log/syslog
