# python3 mysql example

## Install driver
```bash
pip3 install mysql-connector-python
```

## Test connection
```python
from getpass import getpass
from mysql.connector import connect, Error

try:
    with connect(
        host="localhost",
        user=input("Enter username: "),
        password=getpass("Enter password: "),
    ) as connection:
        print(connection)
except Error as e:
    print(e)
```

## select query
```python
from getpass import getpass
from mysql.connector import connect, Error

query = "select count(*) from wp_posts;"

try:
    with connect(
        host="localhost",
        user=input("Enter username: "),
        password=getpass("Enter password: "),
        database=input("Database: "),
    ) as connection:
        print(connection)
        with connection.cursor() as cursor:
            cursor.execute(query)
            for row in cursor.fetchall():
                print(row)
except Error as e:
    print(e)
```

## multiple statements with variable

```python
from getpass import getpass
from mysql.connector import connect, Error
import re

query = """
SET @str='%foo%';
SELECT id, content FROM my_table WHERE content LIKE @str;
"""

records = []
try:
    with connect(
        host="localhost",
        user=input("Enter username: "),
        password=getpass("Enter password: "),
        database=input("Database: "),
    ) as connection:
        with connection.cursor() as cursor:
            for result in cursor.execute(query, multi=True):
                if result.with_rows:
                    for row in cursor.fetchall():
                        records.append(row)
except Error as e:
    print(e)
```

> tags: python3, mysql

> uid: 20211026083732Z

> links: 

