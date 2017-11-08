# Relational DB Roadmap

## Install
### Clone repository
```bash
git@github.com:gregurco/relational-db-roadmap.git
```

### Move into dir project and up vagrant machine
```bash
$ cd relational-db-roadmap
$ vagrant up
```

After that phpmyadmin will be accessible by link: [http://192.168.0.250/phpmyadmin][1].  
User user `root` with password `root`. It will be master server.  
For slave server access [http://192.168.0.251/phpmyadmin][2].  

### Enter in master machine
```bash
$ vagrant ssh mysql_master
```

### Enter in slave machine
```bash
$ vagrant ssh mysql_slave
```

[1]: http://192.168.0.250/phpmyadmin
[2]: http://192.168.0.251/phpmyadmin
