# Cheatsheet linux privilege escalation

## SUID scan

```
find / -perm -u=s -type f 2>/dev/null
```

## Writables directory scan

```
find / -perm -g=s -o -perm -4000 ! -type l -maxdepth 6 -exec ls -ld {} \; 2>/dev/null
```

## Binary with exec rights 

```
find / -type f -perm /6000 -ls 2>/dev/null 
```

## Found specific file

```
binwalk socute.jpg 
```

## Get sudo permissions (Must have the user password)

```
sudo -l
```
