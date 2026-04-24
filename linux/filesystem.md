# Linux Files

## /tmp
The /tmp directory is always writeable. If the home directory is not writeable:
`mktemp -d`
Once created, you can move to this directory and use
```
cp filename .
mv filename better_filename
```
## .bashrc
.bashrc is run every time a terminal is loaded, including when SSH in.
