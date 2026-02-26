## Parse log files

input:

```bash
logextract.py
def extract_errors(log_file):
    try:
        with open(log_file, "r") as file:
            found = False
            for line in file:
                if "error" in line.lower():
                    print(line.strip())
                    found = True

            if not found:
                print("No error lines found in the log.")

    except FileNotFoundError:
        print("Log file not found. Check the path.")
    except PermissionError:
        print("Permission denied. Try running with sudo.")
    except Exception as e:
        print("Unexpected error:", e)

if __name__ == "__main__":
    log_path = input("Enter full log file path: ")
    extract_errors(log_path)
                                                      
```

output:

```bash
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/python]
└─$ python3 logextract.py
Enter full log file path: /var/log/syslog
No error lines found in the log.
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/python]
└─$ python3 logextract.py
Enter full log file path: /var/log/auth.log
No error lines found in the log.

```
