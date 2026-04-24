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
`cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'`

### mkdir
Creating a temporary directory in /tmp:
`mktemp -d`
This does not delete by itself.

### scptransfer
Transfer file to pwd.
`scp -P 2220 user@domain:sshkey.private .`

### SSH
SSH w/Private key file:
`ssh -i sshkey.private host@domain -p 2220`

SSH also allows remote execution of commands by adding the commands after the common SSH expression. Examples:
`ssh user@hostname -p 2220 /bin/bash`
`ssh bandit18@bandit.labs.overthewire.org -p 2220 -t /bin/sh`
This creates a pseudo terminal. A pseudoterminal works by creating a pair of devices: a master and a slave. When you write to the master, the input appears as if it was typed directly into the slave terminal. Conversely, any output to the slave terminal can be read from the master.

### Netcat
nc or netcat is a command that allows to read and write data over a network connection. It can be used for TCP and UDP connections. To connect to a service (as client) on a network the command syntax is the following: nc <host> <port>. To create a server that listens to incoming packets, the command looks like this: nc -l <port>.

### OpenSSL
OpenSSL is a library for secure communication over networks. It uses TLS and SSL cryptographic protocols that are, for example, used in HTTPS to secure the web traffic.
`openssl s_client -connect host:port`

### SUID
The SUID bit replaces the 'x' in a file's permission. It allows a user to execute the file if 
To give a file SETUID bit:
`chmod u+s <filename>`
Example from bandit:
`bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20`
This executes bandit20-do and since bandit20 is the owner and the file has the SUID bit for this owner, run the cat command for a file that only bandit20 has access to.














