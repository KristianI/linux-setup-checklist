# linux-setup-checklist

Personal checklist of tasks/commands to run when setting up a new Linux server.

# General checklist

[ ] Add **hostname** to `PS1` in .bashrc (to avoid running command on wrong environment)
[ ] `sudo apt update`
[ ] `sudo apt upgrade -y`
[ ] `sudo apt install ntpdate htop -y`
[ ] `sudo apt autoremove -y`
[ ] `(crontab -l 2>/dev/null; echo "0 0 1 * * sudo /usr/sbin/ntpdate -u pool.ntp.org") | crontab -`
[ ] Secure sshd `sudo vim /etc/ssh/sshd_config`
[ ] Setup Nagios monitoring.
[ ] Configure firewall.
[ ] Install clamscan with nightly freshclam and scanning cron.
[ ] Allow only specific user to setup cron jobs, `echo "username-here"  > /etc/cron.allow`
[ ] Deactivate services not in use.
[ ] Setup backup service.

# Webserver additional checklist

[ ] Add to secondary uptime monitor that listens on https.
[ ] Setup SSL expiration monitor.
