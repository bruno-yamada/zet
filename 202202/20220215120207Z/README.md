# Checking empty dirs

Checks directories without any files in it
```bash
COUNT=$(find my-dir -type f | wc -l)
if [ "$COUNT" -gt "0" ]; then echo "not empty"; else echo "empty" fi
```

> tags: bash; wc; find;

> uid: 20220215120207Z

> links: 

