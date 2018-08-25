# ansible-webserver
Configure apache, php and mysql in distrubutions Debian, Ubutnu, CentOS e RedHat

## Confs:

* Add in /etc/ansible/hosts:

```
[mygroup] 
192.168.1.1
192.168.1.2
.
.
.
192.168.1.n
```

* Alter in file /etc/ansible/palybooks/webserver.yml:

```
- hosts: mygroup
```

* Alter password in mysql root user:

```
command:  mysql -u root --execute="UPDATE mysql.user SET authentication_string = PASSWORD('senha') WHERE User = 'root' AND Host = 'localhost';"
```
