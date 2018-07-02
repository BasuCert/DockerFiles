# motoshub docker

## Installation
1. You need to install ``docker`` and ``docker-compose`` and then run the following commands:
```shell
~$ git clone https://github.com/BasuCert/DockerFiles.git
~$ cd DockerFiles/motoshub
```

2. edit ``docker-compose.yml`` and change database default credentials.

![database default credentials](/motoshub/screenshots/dbconfig.png?raw=true)

3. run containers :
```shell
~$ docker-compose up -d 
```

4. open URI and continue installation in your browser:

![database default credentials](/motoshub/screenshots/webinterface-config.png?raw=true)

note: if you have made a change in database config section, use the new information in the next step of the installation:
```
hostname=mariadb
username=[MYSQL_USER]
password=[MYSQL_PASSWORD]
database name=[MYSQL_DATABASE]
```

![database default credentials](/motoshub/screenshots/webinterface-dbconfig.png?raw=true)
