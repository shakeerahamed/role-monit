MONIT-Barks at your daemon



# role-monit
Installing monit and adding services to the node using ansible role.

Note:
Change permission of monitrc in templates to 0600 to 0644 
chmod 644 monitrc 
--> As centos user we cannot able to copy file to the node

change the path of user_home directory in vars section
eg. user_home=/home/centos
--> Change accordingly

To use host IP as a variable for file copies.
{{ ansible_default_ipv4.address }}
--> use this in template section in monitrc file to change IP according to node
