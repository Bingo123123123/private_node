# private_node

make sure nodes is installed
curl -sL https://deb.nodesource.com/setup_9.x | sudo -E bash -
sudo apt-get install -y nodejs


make sure fiber is installed
npm install fibers



make sure you get the build-essentials
sudo apt-get install -y build-essential

make sure you have vhost
npm install vhost


make sure you start with sudo:

download mew rep
wget -O MEWV3.zip https://github.com/kvhnuke/etherwallet/archive/v3.11.2.4.zip?raw=true 
sudo apt-get install unzip
After installing the unzip utility, if you want to extract to a particular destination folder, you can use:
unzip MEW3.zip -d destination_folder
or easier 
unzip MEW.zip

then
cd etherwallet-3.11.2.4/


edit ip in nodeIP.js and not response.js
see:
https://ethereum.stackexchange.com/questions/11188/etherwallet-3-4-1-on-private-chain-setup-having-404-error

sudo node runLocalServer.js

check if you get a 404 on http://localhost:port/api.mew

