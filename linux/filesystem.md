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

## cronjobs
cronjobs are programs running automatically at regular intervals. In Linux, there are multiple folders that can contain these cronjobs:
* cron.d
* cron.daily
* cron.hourly
* cron.monthly
* crontab
* cron.weekly
The folders contain files with instructions on how the programs are run.
A file starts with the first five columns which indicate at what time/interval the program should be done. Five stars '*****' indicate it is run every minute, every day.

Next is the command/program that is to be executed which can be found in `/usr/bin/cronjob_filename.sh`








