# Easily adding executable scripts to a container image

- Create folder `scripts` in your project 
eg.
```bash
$ ls -1a scripts/
script1.py
script2.rb
script3.sh
script4
```
- Add these lines to your Dockerfile:
> will create the link without the extension
```
ADD ./scripts /opt/scripts
while read f; do
  chmod +x $f;
  ln -s /opt/scripts/$(basename $f) /usr/local/bin/$(basename $f | sed -e 's/\..*//g');
done
```

> tags: shell; docker; linux; container;

> uid: 20211021123142Z

> links: 

