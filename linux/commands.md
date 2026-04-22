## Commands
https://docs.google.com/spreadsheets/d/1LcZpKIRh7qDFbL-yKj8nXdjCxrK6fuYANPvzZlFwde8/edit?gid=2074172094#gid=2074172094

### find
By default, find recursively looks for files and subfolders.
Cheatsheet
`https://quickref.me/find.html`

Finding SUID bit files
`find / -perm -4000 -type f 2>/dev/null`
https://gtfobins.org/gtfobins/head/

Finding files/directories
`find / -type f -iname '*filename*' 2>/dev/null`

Finding a file with 1033 bytes, not-executable, human readable.
`find . -type f -size 1033c ! -executable -exec file '{}' \; | grep ASCII`
`-exec file '{}' \;` For each file that passed the filters so far, run the file command on it.
`! -perm /111` is equivalent to `!-executable`


### grep
```https://quickref.me/grep```

### Operators
```
&	Allows you to run commands in the background of your terminal.
&&	Allows you to combine multiple commands together in one line of your terminal.
>   redirects output (such as using cat to output a file) and direct it elsewhere.
>>  same function of the > operator but appends the output rather than replacing (meaning nothing is overwritten).
```

### Safe shutdown
```
sudo shutdown -h now
sudo poweroff
```
### Cat
Reading '-' file
cat ./-

### diff

### touch
Changing modified time of changeme file with reference file
touch -r reference changeme

### More
env
$VARIABLE

### Strings

### File command
Can easily see all file types.
`file file*`

### Sort and uniq
Only display lines that occur once.
`sort file.txt | uniq -u`

### tr Translate
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
