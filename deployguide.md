# Deploy App

## SSH Server
1. `ssh root@<IP server>` (-> root@ubuntu: web server)
2. `apt update & apt upgrade`

## Point domain to IP server
- Check: `ping domain`

## Create user on Server 
1. `adduser <username>`
2. Switch user: `su - <username>
3. Sudoers file: `ls -l /etc/`
4. chmod: `chmod u+w /etc/sudoers`
5. Insert: `<username> ALL=(ALL:ALL) ALL`
6: chmod: chmod: `chmod u-w /etc/sudoers`
[7]: remove user: `deluser <username>`
8: ssh username

## Nginx
1. ssh <username>domain
2. install nginx 
3. do that: https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-20-04
4.  

