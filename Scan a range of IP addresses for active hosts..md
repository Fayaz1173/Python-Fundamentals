## Scan a range of IP addresses for active hosts.

input:

```python
import subprocess
import platform

param = "-n" if platform.system().lower() == "windows" else "-c"

network = input("Enter network prefix: ")
start = int(input("Start host number: "))
end = int(input("End host number: "))

active_hosts = []

print("\nScanning...\n")

for i in range(start, end + 1):
    ip = network + str(i)

    result = subprocess.run(
        ["ping", param, "1", ip],
        stdout=subprocess.DEVNULL
    )

    if result.returncode == 0:
        print(ip, "is active")
        active_hosts.append(ip)

print("\nScan Complete")
print("Total Active Hosts:", len(active_hosts))
```

Output:

```bash
Enter network prefix (example 192.168.1.): 192.168.25.
Start host number: 1
End host number: 250

Scanning...

192.168.25.1 is active
192.168.25.2 is active
192.168.25.3 is active
192.168.25.4 is active
192.168.25.6 is active
192.168.25.7 is active
192.168.25.8 is active
192.168.25.10 is active
192.168.25.12 is active
192.168.25.15 is active
192.168.25.16 is active
192.168.25.18 is active
192.168.25.21 is active
192.168.25.23 is active
192.168.25.24 is active
192.168.25.25 is active
192.168.25.26 is active
192.168.25.27 is active
192.168.25.29 is active
192.168.25.30 is active
192.168.25.31 is active
192.168.25.33 is active
```
