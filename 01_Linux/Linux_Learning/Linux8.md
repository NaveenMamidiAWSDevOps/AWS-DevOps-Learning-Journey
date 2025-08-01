
# 🚀 Process Management Commands in Linux

Master the essential commands to view, monitor, and manage system processes like a pro.

---

## 🔍 1. Viewing Processes with `ps`

The `ps` command displays currently running processes.

### ✅ Use Case  
Check if a specific process (e.g., `nginx`) is running:

```bash
ps aux | grep nginx
```

- `ps aux` → Lists all processes.
- `grep nginx` → Filters the output to show only nginx-related processes.

📌 **Tip**: Use with `grep` to quickly find any running process.

---

## 📊 2. Real-Time Monitoring with `top`

The `top` command provides dynamic, real-time monitoring of system resource usage.

```bash
top
```

Displays CPU usage, memory consumption, and running process details.

### 🎯 While inside `top`:
- Press `P` → Sort by **CPU usage**
- Press `M` → Sort by **Memory usage**
- Press `k` → Kill a process by entering its **PID**

---

## 💀 3. Killing Processes with `kill` and `pkill`

Terminate frozen or misbehaving processes by PID or name.

### 🔧 Kill by PID:

```bash
kill <PID>
kill -9 <PID>  # Force kill
```

#### 🧪 Example:

```bash
ps aux | grep node
kill -9 4567
```

This kills a frozen Node.js process after a failed deployment.

---

### 🔫 Kill by Name with `pkill`:

```bash
pkill -f python
```

This kills any running Python script directly — no need to find the PID!

📌 **Pro Tip**: Use `pkill` to quickly stop processes by name.

---

## 📈 4. Historical Monitoring with `sar`

The `sar` (System Activity Report) command is used for **historical performance analysis**.

> 🛠️ Requires `sysstat` package (install and enable to use `sar`).

### 🔍 Examples:

```bash
sar -u 1 3       # CPU usage (3 reports at 1-second intervals)
sar -r           # Memory usage
sar -n DEV 1 3   # Network usage
```

📌 **Scenario**:  
System was slow 2 hours ago? Use `sar` to analyze CPU or memory usage at that time.

🧠 **Pro Tip**:  
Set up a cron job to collect `sar` logs — great for **post-mortem debugging**!

---