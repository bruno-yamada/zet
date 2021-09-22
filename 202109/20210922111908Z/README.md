# MacOS uses BSD sed and grep

MacOS comes with BSD version of `sed` and `grep` which can cause some problems
as some flags are not supported, you should install the `GNU` variant instead,
which can be done using `brew`:
```
brew install gnu-sed
brew install grep
```
After that they will become available as `gsed` and `ggrep`

> tags: linux; macos; sed; cli; grep;

> uid: 20210922111908Z

> links: 

