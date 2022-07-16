# vicidial mysql repair command
## How to Repair the crashed database in vicidial

Login or SSH to your vicidial server, followed to that copy paste below command

### mysql command to check for any table got crashed
mysqlcheck -p --check asterisk
### mysql command to Repair the crashed mysql tables 
mysqlcheck -p --auto-repair asterisk
### mysql command to optimize the tables 
mysqlcheck -p --optimize asterisk

### How to force Repair the vicidial crashed mysql table like call_log
mysql -p
mysql>use asterisk
mysql>REPAIR table table_name USE_FRM;
eg: REPAIR table vicidial_live_agents USE_FRM;

### Reference 
<url>https://www.striker24x7.com/2011/05/vicidial-mysql-repair-command.html</url>

