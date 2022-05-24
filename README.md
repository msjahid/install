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
