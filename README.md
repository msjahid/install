# Linux Software Install Commands

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
