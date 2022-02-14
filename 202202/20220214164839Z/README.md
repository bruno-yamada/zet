# Quickly encrypt files with a password using openssl

```bash
# encrypt 
openssl enc -in file.json -aes-256-cbc -pass stdin > file.json.enc

# decrypt 
openssl enc -in file.json.enc -d -aes-256-cbc -pass stdin
```

Password can also be in a file or environment variable:
```
-pass file:my-file
-pass env:my-env
```

> tags: openssl; security; encryption;

> uid: 20220214164839Z

> links: 

