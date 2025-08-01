🧑‍💻 **User / Group Administration Commands in Linux**

> ✅ *Only `root` or users with `sudo` privileges can perform most of these operations.*

---

#### 🔹 1. `useradd` – Create a new user

```bash
sudo useradd john
```

- Creates a new user named `john`.
- You can add options like `-m` to create a home directory:
```bash
sudo useradd -m john
```

---

#### 🔹 2. `passwd` – Change user password

```bash
sudo passwd john
```

- Prompts to enter and confirm the new password.
- If you're changing your own password: `passwd`

---

#### 🔹 3. `chage` – Manage user password expiry information

```bash
sudo chage -l john
```

- Lists threshold details like last password change, expiry, etc.

---

#### 🔹 4. `groupadd` – Create a new group

```bash
sudo groupadd devs
```

- Adds a new group called `devs`.

---

#### 🔹 5. `usermod` – Modify a user account

```bash
sudo usermod -aG devs john
```

- Adds user `john` to the `devs` group.
- `-aG` = append to group (without removing existing ones)

---

#### 🔹 6. `id` – Show user ID and group IDs

```bash
id john
```

- Displays UID, GID, and groups for user `john`.

---

#### 🔹 7. `groups` – Show groups a user belongs to

```bash
groups john
```

- Shows all groups associated with the user.

---

#### 🔹 8. `lid` – Show group-user relationship (requires `libuser`)

```bash
sudo lid -g devs
```

- Shows users in the `devs` group.
- May need to install: `sudo yum install libuser` or `sudo apt install libuser`

---

#### 🔹 9. `su` – Switch user

```bash
su - john
```

- Switches to user `john`.  
- Press `Ctrl+D` or type `exit` to return.

---

#### 🔹 10. `sudo` – Run command as another user (usually root)

```bash
sudo apt update
```

- Executes `apt update` with root privileges.

---

#### 🔹 11. `userdel` – Delete a user

```bash
sudo userdel john
```

- Removes the user `john`.

- To remove user and their home directory:
```bash
sudo userdel -r john
```

---

#### 🔹 12. `groupdel` – Delete a group

```bash
sudo groupdel devs
```

- Deletes the `devs` group.

---


##############################################
# 🛠️ Automating / Scheduling Tasks in Linux #
##############################################

# --------------------------------------------
# 1️⃣ cron
# --------------------------------------------
# 'cron' is a daemon (background service) that runs scheduled tasks.
# It reads job schedules from:
#     - /etc/crontab
#     - /etc/cron.d/
#     - /var/spool/cron/
#     - User crontabs

# --------------------------------------------
# 2️⃣ crontab
# --------------------------------------------
# 'crontab' is the command-line tool to manage cron jobs per user.

# 🔹 List current user's cron jobs
crontab -l

# 🔹 Edit current user's cron jobs
crontab -e

# 🔹 Remove current user's cron jobs
crontab -r

# --------------------------------------------
# 📅 Crontab Syntax Format
# --------------------------------------------
# ┌──────────── Minute        (0 - 59)
# │ ┌────────── Hour          (0 - 23)
# │ │ ┌──────── Day of Month  (1 - 31)
# │ │ │ ┌────── Month         (1 - 12)
# │ │ │ │ ┌──── Day of Week   (0 - 7) (Sunday = 0 or 7)
# │ │ │ │ │
# * * * * *  command-to-execute

# --------------------------------------------
# ✅ Example Cron Jobs
# --------------------------------------------

# Run backup script every day at 2 AM
0 2 * * * /home/user/scripts/backup.sh

# Clear logs every Sunday at midnight
0 0 * * 0 /home/user/scripts/clear_logs.sh

# Reboot system every day at 3 AM (⚠️ use carefully)
0 3 * * * /sbin/shutdown -r now
