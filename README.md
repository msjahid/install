# Linux Software Install Commands
```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
sudo apt-get install snapd
sudo apt install python3-pip
```

## Xampp and Mysql 
Launch Xampp through the Terminal
```bash
sudo /opt/lampp/lampp start
```

Open xampp MySQL as mysql -u root -p so adding path in bashrc file
```bash
export PATH=/opt/lampp/bin/:$PATH
```
Then close it and source it with:
```bash
source ~/.bashrc
```
Adding password Xampp and MySQL, phpMyAdmin
```bash
sudo /opt/lampp/lampp security
```
## Neovim install configure 
At first install Neovim
```bash
sudo apt install neovim
```
Prerequisite system files
```bash
sudo apt-get install curl
sudo apt-get install git
sudo apt install exuberant-ctags
pip3 install jedi
```
**Node.js v18.x**:

```sh
# Using Ubuntu
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs
sudo npm install -g yarn
```
configure neovim in config folder
```bash
cd .config 
mkdir nvim 
cd nvim 
nvim init.vim
mkdir autoload
cd autoload
curl https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
curl https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim -o plug.vim
```
Then install plugin on your neovim
```bash
:PlugInstall
```
Plugin Open command
```bash
:NERDTreeToggle
:TerminalSplit bash
:TagbarToggle
```
Python install
```bash
cd plugged/coc.nvim/
yarn install
yarn build
:CocInstall coc-python
```
## Create Project of JavaScript
```bash
mkdir nodeproject
cd nodeproject/
yarn init
yarn add express
yarn # if you delete some items then type yarn can back items
touch index.js
```
Expree Code for first time
```JavaScript
const express = require('express')
const app = express()

app.get("/",(req,res)=>{
    res.end("Hello World")
})

app.listen(4000)
```
Debug true mode for developing 
```bash
yarn global add nodemon
#just run your code insted of node to nodemon
```
## Git

###### Cloning remote
```
git clone remote_link 
```
###### Initialize local git repo
```
git init 
```
###### Add all files to index
```
git add .
```
###### Check status of working tree
```
git status
```
###### Commit changes in index
```
git commit -m 'messages'
```
###### Push to remote repo
```
git push
```
###### Push with remote name
```
git push -u origin branch-name
```
###### Pull latest from remote repo
```
git pull
```
###### Clone repo into a local new directory
```
git clone
```
###### Switching branch
```
git checkout branch-name
```
###### Merging branch
```
git merge branch-name
```
###### View information about previous commits that have occurred recent
```
git log
```
###### Displaying individual links of origins
```
git remote -v 
```
###### Setting Global Username
```
git config --global user.name "siyam04"
```
###### Setting Global Email
```
git config --global user.email "galib.abdullah04@gmail.com" 
```

--------------------------------------------------------------------------------

## Heroku

###### Login
```
heroku login
```
###### Create App
```
heroku create app-name
```
###### Push App
```
git push heroku main
```
###### Bash Access
```
heroku run bash
```
```
ls
```
```
cd /
```
```
ls
```
```
exit
```
###### Setup Heroku PostgreSQL Database
```
heroku addons:create heroku-postgresql:hobby-dev
```
###### Access Heroku PostgreSQL Database
```
heroku pg:credentials:url --app app-name
```
###### Heroku + Django: Collect Static Files (No need if collected from locally)
```
heroku run python manage.py collectstatic
```

--------------------------------------------------------------------------------

## Django

###### Create virtualenv
```
python3 -m venv venv
```
```
source venv/bin/activate
```
###### Install django
```
pip3 install django
```
```
python3 -m django --version
```
###### Create Project
```
django-admin startproject project-name
```
###### Create Project Using Current Dir
```
django-admin startproject project_name .
```
###### Create App
```
python manage.py startapp app-name
```
###### Create superuser
```
python manage.py createsuperuser
```
###### Database
```
python manage.py makemigrations
```
```
python manage.py migrate
```
###### Runserver
```
python manage.py runserver
```
###### Shell
```
python manage.py shell
```
###### Flush database
```
python manage.py flush
```
###### Requirements
```
pip3 freeze
```
```
pip3 list
```
```
pip3 freeze > requirements.txt
```
```
pip3 install -r requirements.txt
```

--------------------------------------------------------------------------------

## NPM

###### Install
```
npm install
```
###### Compiles and hot-reloads for development
```
npm run serve
```
###### Compiles and minifies for production
```
npm run build
```
```
npm run build --watch
```
###### Remove caches and reinstall 
```
rm -rf node_modules package-lock.json && npm install
```

--------------------------------------------------------------------------------

## Docker

* Docker-Compose

###### Build
```
docker-compose build --no-cache --force-rm
```
###### Push
```
docker-compose push
```
###### Pull
```
docker-compose pull
```
###### Up
```
docker-compose up
```
###### Down
```
docker-compose down
```
###### Up, Down (run in background)
```
docker-compose up -d
```
```
docker-compose down -d
```

* Docker

###### Image list
```
docker images
```
###### Container list
```
docker container ls -a
```
###### Stop Container
```
docker container stop container_id
```
###### Process list
```
docker ps -a
```
###### Remove images
```
docker image rm image_id_1 image_id_2 image_id_3
```
###### Remove Container
```
docker container rm container_id
```
* Project Related (from project directory)

###### Show Images
``` 
docker-compose images
```
###### All Commands
```
docker-compose
```
###### Pull
```
docker-compose pull
```
###### Migrate
```
docker-compose run my_service_name python manage.py migrate
```
###### Faker
```
docker-compose run my_service_name python fake_data.py (if available)
```
###### Up
```
docker-compose up
```   
###### Show host ip
```
docker-compose exec my_service_name bash
```
```
hostname -i
```
```
docker-compose exec my_db_service_name bash
```
```
hostname -i   
```
* Manage docker as a non-root user (post-installation steps for linux)

###### 1. Create the docker group
```
sudo groupadd docker
```
###### 2. Add your user to the docker group
```
sudo usermod -aG docker $USER
```
###### 3. Log out and log back in so that your group membership is re-evaluated
```
newgrp docker 
```
###### 4. Verify that you can run 'docker' commands without 'sudo'
```
docker run hello-world
```

--------------------------------------------------------------------------------

## Linux

###### Logging in as root
```
ssh root@your_server_ip
```
###### Creating a new user
```
adduser siyam
```
###### Granting administrative privileges
```
usermod -aG sudo siyam
```
###### Logging in as user
```
ssh root@siyam
```
###### Free up disk space
```
sudo du -sh /var/cache/apt
```
```
sudo apt-get clean
```
###### User permission
```
sudo chown -R $USER:$USER ./
```
###### Blank screen fix (lightdm)
```
Ctrl + Alt + F4
```
```
your username & password
```
```
sudo apt-get purge lightdm
```
```
sudo apt-get update
```
```
sudo apt-get install lightdm 
```
```
dpkg-reconfigure lightdm
```
```
sudo shutdown -r now 
```
###### Reboot immediately with killing all the processes
```
sudo shutdown -r now 
```
###### Reboot
```
sudo reboot
```
###### Power off
```
sudo poweroff
```
###### Systemctl
```
sudo systemctl status package_name
```
```
sudo systemctl enable package_name
```
```
sudo systemctl start package_name
```
```
sudo systemctl stop package_name
```
```
sudo systemctl disable package_name
```
###### Remove directory
```
sudo rm -rf dir_name
```
###### View file
```
cat file_name
```
###### Edit file
```
vim file_name
```
```
gedit file_name
```
###### Copy
```
cp file.txt /backup
```
```
cp file.txt /backup/new_file.txt
```
```
cp file.txt dir file1.txt file2.txt dir1
```
###### Move
```
mv testfile testfile2
```
```
mv /home/jack/testfile /home/jack/testfile2
```
```
mv /home/jack/testfile /home/jack/Documents/
```
###### Restart apache for server
```
sudo systemctl restart apache2
```

--------------------------------------------------------------------------------

## PostgreSQL Setup on Linux

###### Install
```
sudo apt update
```
```
sudo apt install postgresql postgresql-contrib
```
###### Start service
```
sudo service postgresql start
```
###### Check status
```
sudo systemctl status postgresql
```
###### Login postgres with password
```
sudo -i -u postgres
```
```
psql
```
###### Connection details
```
postgres=# \conninfo
```
###### Exit prompt
```
postgres=# \q
```
###### Login direct
```
sudo -u postgres psql
```
###### Set password
```
CREATE USER postgres WITH PASSWORD 'postgres';
```
###### Create database
```
CREATE DATABASE database_name;
```
###### Set permissions
```
GRANT ALL PRIVILEGES ON DATABASE postgres TO postgres;
```
###### Database list
```
postgres=# \l
```

