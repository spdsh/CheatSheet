# Cheatsheet SMB

## SMB Scan with enum4linux [https://github.com/CiscoCXSecurity/enum4linux]

```
enum4linux.pl
```

## Crack SMB password with crackmapexec [https://github.com/byt3bl33d3r/CrackMapExec/]

```
crackmapexec smb IP -u USER -p pass.txt 
```

## Get SMB shares directory with permissions 

```
crackmapexec smb IP -u USER -p PASSWORD --shares
```

