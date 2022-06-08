#  bash string array to JSON string array


```bash
my_array=("a" "b")
my_array+=("c")
printf '%s\n' "${my_array[@]}" | sort | uniq | grep -v '^$' | jq -R . | jq -s .
```

> tags: bash; jq;

> uid: 20220607213235Z

> links: 

