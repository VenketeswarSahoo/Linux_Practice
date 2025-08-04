# 🐧 Basic Linux Commands Cheat Sheet

A handy reference for commonly used Linux commands.

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

## 🧪 Practice Example

```bash
# Practice block
mkdir linux_practice
cd linux_practice
touch file1.txt file2.txt
echo "Hello Linux" > file1.txt
cat file1.txt
cp file1.txt copied.txt
mv copied.txt renamed.txt
rm renamed.txt
cd ..
rm -r linux_practice
