- FireEye M-Trends Report of 2020: https://services.google.com/fh/files/misc/m-trends-report-2020-en.pdf

```text
# Connect openvpn hackthebox 
sudo openvpn academy-regular.openvpn
# Open new terminal and connect server via ssh 
ssh htb-student@server-id 
e.g: ssh htb-student@10.129.66.140
# Enter password: 

# Find full path of php.ini
sudo find / -name "php.ini" 2>/dev/null

sudo nano /etc/php/7.4/apache2/php.ini
# Enter password: 
# append 'system' to line 'disable_system' of ..php.init

# Create shell.php
echo '<?php system($_GET["cmd"]); ?>' | sudo tee /var/www/html/shell.php

# Curl it
curl -X GET 'http://localhost/shell.php'

# 
cat /var/log/apache2/error.log

# Read error message and input answer on hackthebox question

```


## Key words

<pre>
Edit the php.ini file to block system(), then try to execute PHP Code that uses system. Read the /var/log/apache2/error.log file and fill in the blank: system() has been disabled for ________ reasons.
</pre>

