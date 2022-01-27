# Replace values on conf files using env variables

## Simple usage of bash + sed before the starting command of the container
This is what mk0-x/docker-clamav uses:
- https://github.com/mko-x/docker-clamav/blob/master/alpine/main/envconfig.sh

```
...
for OUTPUT in $(env | awk -F "=" '{print $1}' | grep "^CLAMD_CONF_"); do
    test "$OUTPUT" = "CLAMD_CONF_FILE" && continue  # skip configuration file variable

    TRIMMED="${OUTPUT/CLAMD_CONF_/}"
    grep -q "^$TRIMMED " /etc/clamav/clamd.conf && sed "s/^$TRIMMED .*/$TRIMMED ${!OUTPUT}/" -i /etc/clamav/clamd.conf ||
        sed "$ a\\$TRIMMED ${!OUTPUT}" -i /etc/clamav/clamd.conf
done
...
```

So you can customize your installation with env variables such as:
```
export CLAMD_CONF_MaxFileSize=200M
```


> tags: bash; clamav; k8s;

> uid: 20220127172816Z

> links: 

