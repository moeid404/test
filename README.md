# wordpress-app
- **LEMP Stack with a wordpress App**
- **Supposing you just having a server ip and password**

## Beginning 📌
### Project Directory Structure:
1. Put your password in passwd_file
2. Encrypt it with via Ansible Vault
3. Put your ip in hosts file
4. Define hosts variable in play.yml file

# 1.server_provisioning role 🚩
## defaults/main.yml
- Define the user you want to create
- Define the port you want to contact through via ssh
## tasks/main.yml
After this role you will be able to:
- Connect to the server via ssh without any password
- Have a user on that server with sudo privileges
## vars/main.yml
- Define the path of the passwd_file

# 2.nginx role 🚩
## tasks/main.yml
After this role you will get:
- Nginx with the latest version
- Empty /etc/nginx/sites-availabe
- Nginx server tokens off

