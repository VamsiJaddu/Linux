# Linux commands

"ncdu" instead of du -sh *
du -sh * ---check size of the files,folders
apt install ncdu
ncdu (to check sizes in one go)

"tldr" instead of "man"
find -name *
man find
apt install tldr
tldr find( it shows top used arguments with find)

"rg"instead of "grep"
apt install rg
rg test.sh( to check any files in folder insted of grep)

"fzf" instead of "find"
apt install fzf
fzf (to check the files with complete path) - gui form

"bat" instead of "cat"
apt install bat
bat main.sh (format of the file to read)

"ranger" instead of "vscode" to check files and read only
apt install ranger
ranger (command in some projects folder --->ansible ---->playbook.yaml) --gui form

"lazygit" instead of  "git status,git commits" while checking only
apt install lazygit
lazygit (it shows status, commits..)

"glances" instead of "top"
apt install glances
glances( cpu,memory, ps , diskfiles)

"lazydocker" instaed of "docker ps , docker images ,docker volume" to check only
apt install lazydocker 
lazydocker (shows volumes, images,containers running)

"cmatrix" ---- it is for display like hacking 
apt install cmatrix
cmatrix



cron job:
 * * * * * (minutes hours day month day of week)
        
min - 0..59
hour - 0..23
day - 1..31
month - 1..12
day of week - 0..6

crontab -e 
crontab -l 
crontab -r --- to remove all cron jobs
crontab -u username -l -- to view another user cron job.

/etc/crontab - this file which stores system wide cronjobs
directory of system wide cronjobs --- etc/cron.d/ , /etc/cron.daily/ , /etc/cron.hourly/ ,  /etc/cron.weekly/
/var/log/syslog // /var/log/cron - cron logs stored
tail -f /var/log/syslog ---- to watch live logs

systemctl status cron --- service cron

scripts works manually but fails in cron?
cron runs with minimal environment , so commands may fail.
python script.py
/usr/bin/python3 /home/user/script.py

@reboot /home/user/script.sh --- runs after reboot

cronjob used in kubernetes for backups, database cleanup, report generation

