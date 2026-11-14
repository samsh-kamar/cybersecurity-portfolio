# Linux File Permissions Lab

## What I Did
I learned how Linux file permissions work and how wrong permissions can lead to privilege escalation.

## Commands I Used
```bash
ls -la
chmod 600 secret.txt
chmod 755 script.sh
chown samsh:samsh secret.txt
ls -l
```

## What I Learned
- r = read (4), w = write (2), x = execute (1)
- chmod 777 is dangerous - anyone can read, write and execute the file
- If a sensitive file has 777 permission, an attacker can change it and get access
- Least Privilege in Linux means: give only the permission that is needed, nothing extra

## Why It Matters for SOC Analyst
SOC analysts may encounter permission misconfigurations during investigations and audits. A misconfigured permission is a common contributor to privilege escalation and unauthorized access.

## Status: Completed in my Ubuntu VM
