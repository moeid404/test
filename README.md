# wordpress-app
- **LEMP Stack with a wordpress App**
- **Supposing you just having a server ip and password**

## Beginning 📌
### Project Directory Structure:
1. Put your password in passwd_file
2. Encrypt it with via Ansible Vault
3. Put your ip in hosts file
4. Define hosts variable in play.yml file
----
## 1.server_provisioning role 🚩
### defaults/main.yml
- Define the user you want to create
- Define the port you want to contact through via ssh
### tasks/main.yml
> After this role you will be able to:
- Connect to the server via ssh without any password
- Have a user on that server with sudo privileges
### vars/main.yml
- Define the path of the passwd_file
----
## 2.nginx role 🚩
### tasks/main.yml
> After this role you will get:
- Nginx at latest version
- Empty /etc/nginx/sites-availabe
- Nginx server tokens off
----
## 3.php-fpm role 🚩
### defaults/main.yml
- Define php_version variable
### tasks/main.yml
> After this role you will get:
- php-fpm, php-mysql at latest version
- Some configuration for php-fpm
----
## 4.mariadb role 🚩
### defaults/main.yml
- Define db_name, db_user, db_host
### tasks/main.yml
> After this role you will get:
- mariadb-server, python3-mysqldb at latest version
- Data base and it's user with all privileges on all data bases
- if you want to give the privileges only on the data base use >> priv: '{{db_name}}.*:ALL'
### vars/main.yml
- Define the path of the db_passwd
----
## 4.mariadb role 🚩
### defaults/main.yml
- Define db_name, db_user, db_host
### tasks/main.yml
> After this role you will get:
- mariadb-server, python3-mysqldb at latest version
- Data base and it's user with all privileges on all data bases
- if you want to give the privileges only on the data base use >> priv: '{{db_name}}.*:ALL'
### vars/main.yml
- Define the path of the db_passwd
