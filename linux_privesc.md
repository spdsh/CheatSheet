# Cheatsheet linux privilege escalation

## SUID scan

```
find / -perm -u=s -type f 2>/dev/null
```

## Get sudo permissions (Must have the user password)

```
sudo -l
```
