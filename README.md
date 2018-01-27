# private_node

make sure nodes is installed
curl -sL https://deb.nodesource.com/setup_9.x | sudo -E bash -
sudo apt-get install -y nodejs


make sure fiber is installed
npm install fibers

make sure you get the build-essentials
sudo apt-get install -y build-essential

make sure you havekvhost
npm install vhost

install all the modules missing with npm install express,vhost,body-parser,node-json-rpc,bignumber.js, wait.for


snakeoil problem check here
https://github.com/sous-chefs/postgresql/issues/156
or better here
https://askubuntu.com/questions/49196/how-do-i-create-a-self-signed-ssl-certificate
or even better here
https://askubuntu.com/questions/51840/ssl-certification-is-missing
or even better
The program 'make-ssl-cert' is currently not installed. You can install it by typing:
sudo apt-get install ssl-cert


make sure you start with sudo:

download mew rep (check for updates first!)
wget -O MEWV3.zip https://github.com/kvhnuke/etherwallet/archive/v3.11.3.2.zip?raw=true 
sudo apt-get install unzip
After installing the unzip utility, if you want to extract to a particular destination folder, you can use:
unzip MEW3.zip -d destination_folder
or easier 
unzip MEW.zip

then
cd etherwallet-3.11.2.4/


cd json_relay_node
edit IP in nodeIP.js and not response.js
see:
https://ethereum.stackexchange.com/questions/11188/etherwallet-3-4-1-on-private-chain-setup-having-404-error

edit Ports in response.js

then sudo node runLocalServer.j

go and use https://github.com/expanse-org/HTTPS-NODE-JS to start geth accordingly



Not sure about this
stop apache on bitnami
https://community.bitnami.com/t/how-can-i-completely-disable-apache-and-use-node-js-on-port-80/10330/2

edit ports in runLocalServer.js and runServer.js

sudo node runLocalServer.js runServer.js respectively

check if you get a 404 on http://localhost:port/api.mew

sudo node runServer.js

on bitnami make sure apache works right /80/443 SSL: Error: listen EADDRINUSE :::443
https://community.bitnami.com/t/how-do-i-host-my-app-on-port-80/40977/7
switch of bitnami apache altogether
https://community.bitnami.com/t/how-can-i-completely-disable-apache-and-use-node-js-on-port-80/10330/2

