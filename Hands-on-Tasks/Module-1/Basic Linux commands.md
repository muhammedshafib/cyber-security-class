Absolutely. Here is a **beginner-friendly Linux command cheat sheet**, especially useful for your **Cybersecurity + Kali Linux learning**.

# 🐧 Linux Basic Commands — Complete Beginner Guide

Linux commands are instructions you type into the **Terminal** to interact with the operating system.

Basic structure:

```bash
command [options] [arguments]
```

Example:

```bash
ls -la /home
```

* `ls` → command
* `-la` → options
* `/home` → argument/path

---

## 1. 📍 Navigation Commands

### `pwd` — Print Working Directory

Shows your current location.

```bash
pwd
```

Example output:

```text
/home/kali
```

**Malayalam:** നിങ്ങൾ ഇപ്പോൾ ഏത് folder/directory-ൽ ആണെന്ന് കാണിക്കുന്നു.

---

### `ls` — List

Shows files and folders.

```bash
ls
```

Useful options:

```bash
ls -l
ls -a
ls -la
ls -lh
```

| Command  | Purpose              |
| -------- | -------------------- |
| `ls`     | Files/folders        |
| `ls -l`  | Detailed information |
| `ls -a`  | Hidden files         |
| `ls -lh` | Human-readable sizes |
| `ls -la` | Hidden + detailed    |

---

### `cd` — Change Directory

Move between directories.

```bash
cd Documents
```

Go back one directory:

```bash
cd ..
```

Go to home:

```bash
cd ~
```

Go to root:

```bash
cd /
```

Go to previous directory:

```bash
cd -
```

**Malayalam:** Folder-ൽ നിന്ന് മറ്റൊരു folder-ലേക്ക് പോകാൻ `cd` ഉപയോഗിക്കുന്നു.

---

## 2. 📁 File and Directory Commands

### `mkdir` — Make Directory

Create a folder.

```bash
mkdir test
```

Create multiple folders:

```bash
mkdir folder1 folder2 folder3
```

Create nested directories:

```bash
mkdir -p project/src/files
```

---

### `rmdir` — Remove Directory

Remove an empty folder.

```bash
rmdir test
```

⚠️ Only works when the directory is empty.

---

### `touch`

Create an empty file.

```bash
touch file.txt
```

Multiple files:

```bash
touch file1.txt file2.txt file3.txt
```

---

### `cp` — Copy

Copy a file:

```bash
cp file.txt backup.txt
```

Copy a file to a directory:

```bash
cp file.txt Documents/
```

Copy a directory:

```bash
cp -r folder1 folder2
```

`-r` = recursive.

---

### `mv` — Move / Rename

Move a file:

```bash
mv file.txt Documents/
```

Rename:

```bash
mv old.txt new.txt
```

---

### `rm` — Remove

Delete a file:

```bash
rm file.txt
```

Delete multiple files:

```bash
rm file1.txt file2.txt
```

Delete directory and contents:

```bash
rm -r folder
```

Force delete:

```bash
rm -rf folder
```

⚠️ **Be extremely careful with `rm -rf`.** It can permanently delete large amounts of data.

---

# 3. 📖 Reading Files

### `cat` — Concatenate

Display file contents:

```bash
cat file.txt
```

Create a file with text:

```bash
cat > file.txt
```

Then type:

```text
Hello Linux
```

Press:

```text
Ctrl + D
```

---

### `less`

Read large files page by page:

```bash
less file.txt
```

Useful keys:

```text
Space → Next page
b     → Previous page
q     → Quit
```

---

### `head`

Show beginning of a file:

```bash
head file.txt
```

First 10 lines:

```bash
head -n 10 file.txt
```

---

### `tail`

Show end of a file:

```bash
tail file.txt
```

Last 10 lines:

```bash
tail -n 10 file.txt
```

Follow a log file:

```bash
tail -f /var/log/syslog
```

`-f` = follow.

This is particularly useful for **SOC/log monitoring**.

---

# 4. ✏️ Text Editing

### `nano`

Beginner-friendly terminal editor:

```bash
nano file.txt
```

Common shortcuts:

```text
Ctrl + O → Save
Ctrl + X → Exit
Ctrl + W → Search
Ctrl + K → Cut line
Ctrl + U → Paste
```

---

### `vim`

Open a file:

```bash
vim file.txt
```

or:

```bash
vi file.txt
```

Vim is powerful but has a steeper learning curve.

---

# 5. 🔎 Searching

### `find`

Find files.

```bash
find /home -name file.txt
```

Find `.txt` files:

```bash
find /home -name "*.txt"
```

Find directories:

```bash
find /home -type d
```

Find files:

```bash
find /home -type f
```

---

### `locate`

Search for files quickly:

```bash
locate filename
```

If the database needs updating:

```bash
sudo updatedb
```

---

### `which`

Find the location of a command:

```bash
which python
```

Example:

```text
/usr/bin/python
```

---

### `whereis`

Find binary, source, and manual locations:

```bash
whereis python
```

---

# 6. 🔤 Text Searching

### `grep`

Search for text inside files.

```bash
grep "password" file.txt
```

Case-insensitive:

```bash
grep -i "password" file.txt
```

Search recursively:

```bash
grep -r "password" /home/user/
```

Show line numbers:

```bash
grep -n "error" logfile.txt
```

`grep` is **extremely important in cybersecurity** for searching logs and configuration files.

---

# 7. 🔗 Pipes and Redirection

These are very important Linux concepts.

### `|` — Pipe

Send output from one command to another.

```bash
ls -l | grep ".txt"
```

Workflow:

```text
ls -l
  ↓
output
  ↓
grep ".txt"
  ↓
TXT files
```

---

### `>` — Redirect Output

```bash
ls > files.txt
```

The output goes into `files.txt`.

---

### `>>` — Append

```bash
ls >> files.txt
```

Adds output without deleting existing content.

---

### `<` — Input Redirection

```bash
command < file.txt
```

---

# 8. 👤 User Commands

### `whoami`

Shows current username.

```bash
whoami
```

---

### `id`

Shows user and group IDs.

```bash
id
```

---

### `who`

Shows logged-in users:

```bash
who
```

---

### `w`

Shows logged-in users and their activity:

```bash
w
```

---

### `passwd`

Change your password:

```bash
passwd
```

---

# 9. 🔐 `sudo`

`sudo` means **Superuser Do**.

Run a command with administrator privileges:

```bash
sudo command
```

Example:

```bash
sudo apt update
```

**Malayalam:** Administrator/root permission ആവശ്യമുള്ള command execute ചെയ്യാൻ സാധാരണയായി `sudo` ഉപയോഗിക്കുന്നു.

---

# 10. 👑 Root User

Switch to a root shell:

```bash
sudo -i
```

Check:

```bash
whoami
```

You should see:

```text
root
```

Exit root:

```bash
exit
```

⚠️ Avoid working as root unnecessarily.

---

# 11. 🔑 File Permissions

Linux permissions are very important for cybersecurity.

Check permissions:

```bash
ls -l
```

Example:

```text
-rwxr-xr--
```

Basic permission types:

```text
r = read
w = write
x = execute
```

Three permission groups:

```text
Owner
Group
Others
```

---

### `chmod` — Change Mode

Give execute permission:

```bash
chmod +x script.sh
```

Remove execute:

```bash
chmod -x script.sh
```

Example numeric permissions:

```bash
chmod 755 script.sh
```

Meaning:

```text
Owner  → rwx
Group  → r-x
Others → r-x
```

Another common permission:

```bash
chmod 644 file.txt
```

---

### `chown` — Change Owner

```bash
sudo chown user file.txt
```

Change owner and group:

```bash
sudo chown user:group file.txt
```

---

# 12. 💾 Disk and Storage

### `df`

Show disk space:

```bash
df
```

Human-readable:

```bash
df -h
```

---

### `du`

Show directory/file size:

```bash
du file.txt
```

Human-readable:

```bash
du -h file.txt
```

Directory size:

```bash
du -sh folder/
```

---

### `lsblk`

Show storage devices:

```bash
lsblk
```

Useful when working with disks and USB devices.

---

### `mount`

Mount a filesystem:

```bash
mount
```

Unmount:

```bash
sudo umount /path
```

⚠️ Disk operations require care.

---

# 13. 🧠 System Information

### `uname`

Show system information:

```bash
uname
```

Kernel information:

```bash
uname -a
```

---

### `hostname`

Show computer hostname:

```bash
hostname
```

---

### `hostnamectl`

Detailed hostname/system information:

```bash
hostnamectl
```

---

### `uptime`

Shows how long system has been running:

```bash
uptime
```

---

### `date`

Show date/time:

```bash
date
```

---

### `cal`

Calendar:

```bash
cal
```

---

# 14. ⚙️ Process Management

### `ps`

Show running processes:

```bash
ps
```

Detailed:

```bash
ps aux
```

---

### `top`

Real-time process monitor:

```bash
top
```

Exit:

```text
q
```

---

### `htop`

More user-friendly process monitor:

```bash
htop
```

It may need installation depending on your Linux distribution.

---

### `kill`

Terminate a process:

```bash
kill PID
```

Example:

```bash
kill 1234
```

Force termination:

```bash
kill -9 1234
```

⚠️ Use `-9` only when necessary.

---

### `pkill`

Kill processes by name:

```bash
pkill firefox
```

---

# 15. 🌐 Network Commands

These are **very important for cybersecurity**.

### `ip`

Show network interfaces:

```bash
ip addr
```

Short form:

```bash
ip a
```

Show routes:

```bash
ip route
```

Show links:

```bash
ip link
```

---

### `ping`

Test connectivity:

```bash
ping google.com
```

Stop:

```text
Ctrl + C
```

Example:

```bash
ping 192.168.1.1
```

---

### `ss`

Show network sockets/connections:

```bash
ss
```

Listening ports:

```bash
ss -tuln
```

Very useful for security troubleshooting.

---

### `curl`

Make HTTP requests:

```bash
curl https://example.com
```

Download a file:

```bash
curl -O https://example.com/file.zip
```

---

### `wget`

Download files:

```bash
wget https://example.com/file.zip
```

---

### `dig`

DNS lookup:

```bash
dig example.com
```

---

### `nslookup`

DNS information:

```bash
nslookup example.com
```

---

### `traceroute`

Trace network path:

```bash
traceroute example.com
```

On some systems you may need to install it first.

---

# 16. 📦 Package Management

For Debian-based distributions such as **Kali Linux/Ubuntu**:

### `apt update`

Update package information:

```bash
sudo apt update
```

---

### `apt upgrade`

Upgrade installed packages:

```bash
sudo apt upgrade
```

---

### Install package

```bash
sudo apt install package-name
```

Example:

```bash
sudo apt install curl
```

---

### Remove package

```bash
sudo apt remove package-name
```

---

### Search package

```bash
apt search package-name
```

---

### Show package information

```bash
apt show package-name
```

---

# 17. 📚 Manual / Help Commands

### `man`

Open manual page:

```bash
man ls
```

Example:

```bash
man chmod
```

Exit:

```text
q
```

---

### `--help`

Most commands provide quick help:

```bash
ls --help
```

```bash
chmod --help
```

---

### `history`

Show previously executed commands:

```bash
history
```

Run a previous command:

```bash
!100
```

where `100` is the history number.

---

### `clear`

Clear terminal:

```bash
clear
```

Shortcut:

```text
Ctrl + L
```

---

# 18. 📦 Archive Commands

### `tar`

Create archive:

```bash
tar -cvf archive.tar folder/
```

Extract:

```bash
tar -xvf archive.tar
```

Create compressed `.tar.gz`:

```bash
tar -czvf archive.tar.gz folder/
```

Extract:

```bash
tar -xzvf archive.tar.gz
```

---

### `zip`

Create ZIP:

```bash
zip archive.zip file.txt
```

Directory:

```bash
zip -r archive.zip folder/
```

---

### `unzip`

Extract:

```bash
unzip archive.zip
```

---

# 19. 🔢 Text Processing

### `wc`

Count lines, words and characters:

```bash
wc file.txt
```

Count lines:

```bash
wc -l file.txt
```

---

### `sort`

Sort lines:

```bash
sort file.txt
```

---

### `uniq`

Remove repeated adjacent lines:

```bash
uniq file.txt
```

Common combination:

```bash
sort file.txt | uniq
```

---

### `cut`

Extract columns:

```bash
cut -d ":" -f 1 /etc/passwd
```

---

### `awk`

Process structured text:

```bash
awk '{print $1}' file.txt
```

---

### `sed`

Search/replace text:

```bash
sed 's/old/new/g' file.txt
```

These become especially useful when you start **Linux log analysis and SOC work**.

---

# 20. 🔧 Environment Variables

Show all environment variables:

```bash
env
```

Show one:

```bash
echo $PATH
```

---

### `echo`

Print text:

```bash
echo "Hello Linux"
```

Print variable:

```bash
echo $USER
```

---

# 21. 📋 File Information

### `file`

Determine file type:

```bash
file test.txt
```

Example:

```text
ASCII text
```

---

### `stat`

Detailed file information:

```bash
stat file.txt
```

Shows things like:

* permissions
* owner
* size
* timestamps
* inode

---

### `ln`

Create a link.

Symbolic link:

```bash
ln -s original.txt shortcut.txt
```

---

# 22. 🧾 Command History and Terminal

```bash
history
```

Clear terminal:

```bash
clear
```

Exit terminal:

```bash
exit
```

Show current shell:

```bash
echo $SHELL
```

---

# 23. 🔄 Services

Modern Linux systems commonly use `systemctl`.

Check service:

```bash
systemctl status ssh
```

Start:

```bash
sudo systemctl start ssh
```

Stop:

```bash
sudo systemctl stop ssh
```

Restart:

```bash
sudo systemctl restart ssh
```

Enable at boot:

```bash
sudo systemctl enable ssh
```

Disable:

```bash
sudo systemctl disable ssh
```

---

# 24. 📝 Logs

Linux stores many system logs under:

```bash
/var/log/
```

List logs:

```bash
ls /var/log/
```

Read a log:

```bash
cat /var/log/syslog
```

Search:

```bash
grep "error" /var/log/syslog
```

Follow a log:

```bash
tail -f /var/log/syslog
```

On systems using `systemd`:

```bash
journalctl
```

Recent logs:

```bash
journalctl -n 50
```

Follow logs:

```bash
journalctl -f
```

For cybersecurity/SOC work, **logs + `grep` + `tail` + `journalctl`** are particularly important.

---

# 25. 🔥 Firewall Basics

On Linux systems using UFW:

Check status:

```bash
sudo ufw status
```

Enable:

```bash
sudo ufw enable
```

Disable:

```bash
sudo ufw disable
```

Allow a port:

```bash
sudo ufw allow 22/tcp
```

⚠️ Don't blindly change firewall rules on a remote system—you can lock yourself out.

---

# 26. 🗂️ Important Linux Directories

You should memorize these:

```text
/
├── /bin
├── /boot
├── /dev
├── /etc
├── /home
├── /lib
├── /media
├── /mnt
├── /opt
├── /proc
├── /root
├── /run
├── /sbin
├── /tmp
├── /usr
└── /var
```

| Directory | Purpose                        |
| --------- | ------------------------------ |
| `/`       | Root of filesystem             |
| `/home`   | Normal users' files            |
| `/root`   | Root user's home               |
| `/etc`    | Configuration files            |
| `/var`    | Variable data/logs             |
| `/tmp`    | Temporary files                |
| `/usr`    | Applications/utilities         |
| `/bin`    | Essential commands             |
| `/sbin`   | System administration commands |
| `/dev`    | Device files                   |
| `/proc`   | Process/kernel information     |
| `/opt`    | Optional software              |
| `/boot`   | Boot-related files             |

---

# 🧠 Most Important Commands to Memorize First

Don't try to memorize everything at once.

### Level 1 — Absolute Basics

```bash
pwd
ls
cd
mkdir
touch
cp
mv
rm
cat
clear
```

### Level 2 — Files

```bash
less
head
tail
find
grep
file
stat
chmod
chown
```

### Level 3 — System

```bash
ps
top
kill
df
du
free
uname
hostname
whoami
id
```

### Level 4 — Networking

```bash
ip
ping
ss
curl
wget
dig
nslookup
traceroute
```

### Level 5 — Cybersecurity/SOC

```bash
grep
find
awk
sed
tail
journalctl
ss
ps
ip
tcpdump
```

---

# 🔥 Linux Command Workflow for Cybersecurity

A very useful beginner workflow is:

```text
             Linux Terminal
                   │
                   ▼
              whoami
                   │
                   ▼
                pwd
                   │
                   ▼
                 ls
                   │
                   ▼
             cd / directory
                   │
                   ▼
             find / grep
                   │
                   ▼
            Read files/logs
                   │
                   ▼
          ps / ss / ip / systemctl
                   │
                   ▼
          Analyze system/network
                   │
                   ▼
             Document findings
```

### Example investigation

Check who you are:

```bash
whoami
```

Check location:

```bash
pwd
```

List files:

```bash
ls -la
```

Check network:

```bash
ip a
```

Check listening services:

```bash
ss -tuln
```

Check processes:

```bash
ps aux
```

Search logs:

```bash
grep -i "error" /var/log/syslog
```

Watch new logs:

```bash
tail -f /var/log/syslog
```

---

## 🎯 Your Linux Learning Order

Since you're learning **cybersecurity**, I recommend this order:

```text
Week 1
│
├── Terminal basics
├── pwd
├── ls
├── cd
├── mkdir
├── touch
└── rm

Week 2
│
├── cat
├── less
├── head
├── tail
├── cp
├── mv
└── find

Week 3
│
├── grep
├── sort
├── uniq
├── cut
├── awk
└── sed

Week 4
│
├── chmod
├── chown
├── sudo
├── users/groups
└── processes

Week 5
│
├── ip
├── ping
├── ss
├── curl
├── wget
├── dig
└── traceroute

Week 6
│
├── systemctl
├── journalctl
├── /var/log
├── log analysis
└── basic troubleshooting

Week 7+
│
├── Bash scripting
├── Networking
├── Wireshark
├── tcpdump
├── Linux security
└── SOC investigation
```

**Important:** Learn the commands by actually using them in a Linux VM such as Kali/Ubuntu rather than only memorizing the list. For cybersecurity, understanding **what the command output means** is more important than memorizing hundreds of commands.
