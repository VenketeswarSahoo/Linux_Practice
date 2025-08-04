# 🐧 Basic Linux Commands Cheat Sheet

A handy reference for commonly used Linux commands.

---

## ✅ Steps to Install WSL and Ubuntu

### 1. Check if WSL is Already Installed

Open **PowerShell as Administrator** and run:

```powershell
wsl --list --verbose

If WSL is not installed, follow the next steps.

### 2. Install WSL (First Time Only)

```powershell
wsl --install

### 3. Launch Ubuntu

```powershell
wsl -d Ubuntu

or

```powershell
wsl

---

## 📁 1. File & Directory Management

| Command                         | Description                         | Example                               |
|---------------------------------|-------------------------------------|---------------------------------------|
| `pwd`                           | Print current directory            | `pwd`                                 |
| `ls`                            | List files                         | `ls -l`                               |
| `cd`                            | Change directory                   | `cd ~/Downloads`                      |
| `mkdir`                         | Make directory                     | `mkdir projects`                      |
| `touch`                         | Create empty file                  | `touch notes.txt`                     |
| `cp`                            | Copy files/folders                 | `cp file.txt backup.txt`              |
| `mv`                            | Move/rename files                  | `mv file.txt newname.txt`             |
| `rm`                            | Remove file                        | `rm file.txt`                         |
| `rm -r`                         | Remove directory recursively       | `rm -r folder`                        |
| `tree`                          | View directory tree                | `tree` *(install with `sudo apt install tree`)* |

---

## 📄 2. Viewing & Editing Files

| Command                         | Description                         | Example                               |
|---------------------------------|-------------------------------------|---------------------------------------|
| `cat`                           | Show file contents                 | `cat readme.md`                       |
| `less`                          | View file page by page             | `less bigfile.log`                    |
| `head`                          | First lines of file                | `head -n 5 file.txt`                  |
| `tail`                          | Last lines of file                 | `tail -n 10 file.txt`                 |
| `nano`                          | Terminal text editor               | `nano notes.txt`                      |
| `vim` / `vi`                    | Advanced text editor               | `vim script.sh`                       |
| `echo`                          | Output or write to file            | `echo "Hello" > greet.txt`            |

---

## 🔍 3. Searching

| Command                         | Description                         | Example                               |
|---------------------------------|-------------------------------------|---------------------------------------|
| `find`                          | Find files and directories         | `find . -name "*.js"`                 |
| `grep`                          | Search inside files                | `grep "main" *.py`                    |
| `locate`                        | Quickly find files                 | `locate nginx.conf`                   |

---

## 🖥️ 4. System Information

| Command                         | Description                         | Example                               |
|---------------------------------|-------------------------------------|---------------------------------------|
| `uname -a`                      | Kernel and system info             | `uname -a`                            |
| `top`                           | Show running processes             | `top`                                 |
| `htop`                          | Interactive process viewer         | `htop` *(install with `sudo apt install htop`)* |
| `df -h`                         | Disk space usage                   | `df -h`                               |
| `free -h`                       | Memory usage                       | `free -h`                             |
| `uptime`                        | How long system has been running   | `uptime`                              |
| `whoami`                        | Current user                       | `whoami`                              |
| `id`                            | User and group IDs                 | `id`                                  |

---

## ⚙️ 5. Package Management (APT)

| Command                         | Description                         | Example                               |
|---------------------------------|-------------------------------------|---------------------------------------|
| `sudo apt update`               | Refresh package lists              | `sudo apt update`                     |
| `sudo apt upgrade`              | Upgrade installed packages         | `sudo apt upgrade`                    |
| `sudo apt install <pkg>`        | Install package                    | `sudo apt install git`                |
| `sudo apt remove <pkg>`         | Remove package                     | `sudo apt remove nodejs`              |

---

## 🌐 6. Networking

| Command                         | Description                         | Example                               |
|---------------------------------|-------------------------------------|---------------------------------------|
| `ping`                          | Check network connectivity         | `ping google.com`                     |
| `curl`                          | Fetch URL                          | `curl https://api.github.com`         |
| `wget`                          | Download files                     | `wget https://example.com/file.zip`   |
| `ip a`                          | Show IP addresses                  | `ip a`                                |
| `ifconfig`                      | Network interfaces *(install `net-tools`)* | `ifconfig`                    |
| `netstat`                       | Show ports and connections *(install `net-tools`)* | `netstat -tulnp`            |

---

## 🔐 7. Permissions

| Command                         | Description                         | Example                               |
|---------------------------------|-------------------------------------|---------------------------------------|
| `chmod`                         | Change permissions                 | `chmod +x script.sh`                  |
| `chown`                         | Change file owner                  | `sudo chown $USER file.txt`           |
| `ls -l`                         | Show permissions                   | `ls -l`                               |

---

## 👥 8. User Management

| Command                         | Description                         | Example                               |
|---------------------------------|-------------------------------------|---------------------------------------|
| `who`                           | Show logged-in users               | `who`                                 |
| `adduser`                       | Add a user                         | `sudo adduser john`                   |
| `passwd`                        | Change password                    | `passwd`                              |
| `su`                            | Switch user                        | `su - root`                           |
| `sudo`                          | Run command as superuser           | `sudo apt update`                     |

---

# 📄 `cat` vs `less` vs `nano` vs `vim` – Linux Command Comparison

---

## 📋 Summary Comparison

| Command | Purpose                           | Editing Capability | Use Case                       | Difficulty | Exit Shortcut             |
|---------|-----------------------------------|--------------------|-------------------------------|------------|---------------------------|
| `cat`   | Display file content              | ❌ No               | Quickly view file content     | ⭐ Very Easy  | `Ctrl+C` or close terminal |
| `less`  | Display large file content        | ❌ No               | Quickly view large file       | ⭐⭐ Very Easy | `q` or close terminal |
| `nano`  | Simple terminal text editor       | ✅ Yes              | Quick file edits              | ⭐⭐⭐ Easy     | `Ctrl+X`, then `Y` to save |
| `vim`   | Advanced terminal text editor     | ✅ Yes              | Power editing, scripting      | ⭐⭐⭐⭐ Hard   | `Esc` → `:q!` or `:wq`     |

---

## 🔍 Detailed Descriptions

### 🐱 `cat` – Concatenate and Display

- **Usage**: `cat file.txt`
- **Purpose**: Print the contents of a file to the terminal.
- **Limitations**: You can't edit with `cat`.
- **Best for**: Viewing small files, combining file contents.

---

### 🐱 `less` – Pager for long files

- **Usage**: `less /var/log/syslog`
- **Purpose**: View large files page by page, scroll up/down.
- **Limitations**: You can't edit with `less`.
- **Best for**: Long logs, config files.
- **Best for**:
   - Navigation: ↑, ↓, PgUp, PgDn, / to search
   - Press `q` to quit

---

### ✏️ `nano` – Beginner-Friendly Editor

- **Usage**: `nano file.txt`
- **Purpose**: A simple and easy-to-use terminal text editor.
- **Features**:
  - Easy navigation and editing
  - Useful keyboard shortcuts shown at the bottom
- **Exit**: `Ctrl + X`
- **Save**: `Ctrl + O`, then press `Enter`
- **Best for**: Quick edits, config changes, and beginners.

---

### ⚙️ `vim` – Advanced Text Editor

- **Usage**: `vim file.txt`
- **Purpose**: A powerful and fast editor used by developers and power users.
- **Modes**:
  - `i` = Insert mode (to type text)
  - `Esc` = Exit to normal mode
- **Exit**:
  - `:w` = Save
  - `:q` = Quit
  - `:wq` = Save and quit
  - `:q!` = Quit without saving
- **Best for**: Advanced editing, scripting, programming.

---

## ✅ When to Use Which?

| Task                          | Recommended Tool |
|-------------------------------|------------------|
| Just view a file              | `cat`            |
| Pager for long files          | `less`           |
| Make a quick text edit        | `nano`           |
| Work on code or long scripts  | `vim`            |

---
