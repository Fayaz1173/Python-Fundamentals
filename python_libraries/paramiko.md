# Paramiko

### What is Paramiko?

Paramiko is a Python library used to establish **SSH (Secure Shell)** connections and automate remote system tasks.

It allows you to:

- Connect to remote servers
- Execute commands remotely
- Transfer files (SFTP)
- Automate server administration

# Basic SSH Connection Example

Version with User Input

```python
import paramiko

host = input("Enter host IP: ")
user = input("Enter username: ")
password = input("Enter password: ")
command = input("Enter command to execute: ")

client = paramiko.SSHClient()
client.set_missing_host_key_policy(paramiko.AutoAddPolicy())

try:
    client.connect(hostname=host, username=user, password=password)
    stdin, stdout, stderr = client.exec_command(command)

    print("\nCommand Output:\n")
    print(stdout.read().decode())

except Exception as e:
    print("Error:", e)

finally:
    client.close()
```

output:

```bash
Output:
Brocamp
burp suite mastery
cpu_mem_usage.log
cpu_monitor.sh.save
Desktop
Documents
dos_baseline.txt
Downloads
fim
fim-project
hashes.txt
hulk
image_base64.txt
instagram-bruteforce
lab
Music
neofetch
nmap_8983.txt
Pictures
Public
rainbow_tables
sample.txt
slowloris
stegnography
target_hashes.txt
Templates
text.txt
Videos
wazuh-install.sh
web_hashes.txt
```
