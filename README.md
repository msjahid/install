# Linux Software Install Commands
```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
sudo apt install gnome-shell-extensions
sudo apt install net-tools
sudo apt install gnome-tweaks
sudo apt install htop
sudo apt-get install snapd
sudo apt install python3-pip
sudo apt install spyder
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
Open xampp GUI through the terminal
```bash
sudo /opt/lampp/manager-linux-x64.run
```
## Back up MySQL or MariaDB database
to back up the database to a file called **mydata-backup.sql**, use the following command syntax. This will prompt you for a password when entering the command.
```bash
mysqldump -u root -p mydata > mydata-backup.sql
```
If you need to avoid the password prompt, such as the case in a Bash script, then you can put the password into the command itself by using the **--password** option.
```bash
mysqldump -u root --password="mypassword" mydata > mydata-backup.sql
```
to back up the database to some other location than your present working directory, just put the path in your command.
```bash
mysqldump -u root -p mydata > /home/linuxconfig/mysql/mydata-backup.sql
```
to back up more than one database at once, you can list them separately in your command after the **--databases** option. In this example, we will backup the databases **mydata** and **accounting**.
```bash
mysqldump -u root -p --databases mydata accounting > mydata-backup.sql
```
You can also make a backup of every MySQL or MariaDB database at once by specifying the **--all-databases** option.
```bash
mysqldump -u root -p --all-databases > mydata-backup.sql
```
## Restore a MySQL or MariaDB database backup
This command will restore our database data to our mydata database from previous examples.
```bash
mysql -u root -p mydata < mydata-backup.sql
```
If your backup file contains multiple databases, you can select which ones to restore by using the --one-database flag in your command.
```bash
mysql --one-database mydata < mydata-backup.sql
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
**Nodemon use in npm or yarn command**:
```bash
sudo npm install -g nodemon
#or
sudo yarn global add nodemon
sudo nodemon -v
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
**Secure PostgreSQL**:
```bash
sudo passwd postgres
# su - postgres 
psql -c "ALTER USER postgres WITH PASSWORD 'secure_password_here';" 
exit
sudo systemctl restart postgresql 
```
### pgAdmin 4 install
```bash
sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add -
sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
sudo apt update
sudo apt install pgadmin4 
```
## Gimp install with GMIC and Resynthesizer  
Launch Terminal and following these below command
```bash
sudo apt install flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
sudo flatpak install https://dl.flathub.org/repo/appstream/org.gimp.GIMP.flatpakref
sudo flatpak install org.gimp.GIMP.Plugin.GMic//2-40
sudo flatpak install org.gimp.GIMP.Plugin.Resynthesizer//2-40
sudo flatpak install org.gimp.GIMP.Plugin.BIMP//2-40
```
# Machine Learning Tools & Library
```bash
pip3 install pandas
pip3 install numpy
pip3 install scipy
pip3 install -U scikit-learn
pip3 install seaborn
pip3 install streamlit
```
**Jupyter Autocomplete Extension**:
```bash
pip3 install jupyter_contrib_nbextensions && jupyter contrib nbextension install
pip3 install jupyter-tabnine --user
jupyter nbextension install --py jupyter_tabnine --user
jupyter nbextension enable --py jupyter_tabnine --user
jupyter serverextension enable --py jupyter_tabnine --user
```
**Jupyter Themes**:
```bash
pip3 install jupyterthemes
pip3 install --upgrade jupyterthemes
jt -l #list of all themes
jt -t chesterish
```
## How to Work With JSON in Your Terminal With fx
```bash
sudo apt install curl
npm install -g fx
```
**use fx command**:
```bash
curl https://api.coindesk.com/v1/bpi/currentprice.json | fx .
```
# Python Specific version install not mandatory
```bash
sudo apt-get install libssl-dev openssl
wget https://www.python.org/ftp/python/3.5.0/Python-3.10.4.tgz
tar xzvf Python-3.10.4.tgz
cd Python-3.10.04
./configure
make
sudo make install
```
**Python idle specific version**:
```bash
sudo apt-get install idle-python3.10
```
## Install the network scanning tool Nmap
```bash
sudo apt install nmap
```
Now find your ip address using the *ifconfig'* command
```bash
nmap -sP 192.168.12.208/24
```
## Git configure
```bash
git config --global user.name "msjahid" 
git config --global user.email "msjahid.ai@gmail.com"
# Checking command
git config --global user.name
git config --global user.email
```
##Mongodb Warning 
```bash
echo "deb http://security.ubuntu.com/ubuntu impish-security main" | sudo tee /etc/apt/sources.list.d/impish-security.list
sudo apt-get update
sudo apt-get install libssl1.1
```
