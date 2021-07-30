# Check CIDR ranges overlapping

Checks when network CIDR blocks overlaps over one another

```python
import ipaddr
import itertools

ranges = [
  ipaddr.IPNetwork("10.210.192.0/21"),
  ipaddr.IPNetwork("10.210.200.0/21"),
  ipaddr.IPNetwork("10.211.200.0/22"),
]

r = itertools.combinations(ranges, 2)

for a,b in r:
  print("{} overlaps with {}: {}".format(a, b, a.overlaps(b)))

```

> tags: cidr; network; overlap;

> uid: 20210730001059Z

> links: 

