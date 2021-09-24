# source vs eval for loading environment variables 

`eval` is used to interpret a string and invoke the result, so it makes 2
executions

Not very safe because it can be risky to run arbitrary generated expressions,
and it can result in dirty strings

`source` is used to invoke a file into the current shell, or optionally a new
shell from a string:
```
source envfile
# or
source <(echo "export TEST=1")
```
which invokes a new shell to take the place of the current one, and calling the provided command within ("echo..")

> tags: needs-revision;

> uid: 20210924150930Z

> links: 

