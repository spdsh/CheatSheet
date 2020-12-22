# Cheatsheet nmap

## Basic scan (1000 first ports)

```
nmap IP
```

## Basic scan (all ports)

```
nmap -p- IP
```

## Enumerate samba server

```
nmap -p 445 --script=smb-enum-shares.nse,smb-enum-users.nse MACHINE_IP
```

## Enumerate RPC

```
nmap -p 111 --script=nfs-ls,nfs-statfs,nfs-showmount MACHINE_IP
```