# private_node

make sure nodes is installed best is if you install node 6
curl -sL https://deb.nodesource.com/setup_9.x | sudo -E bash -
sudo apt-get install -y nodejs


make sure fiber is installed
npm install fibers

make sure you get the build-essentials
sudo apt-get install -y build-essential


install all the modules missing with 
npm install express vhost body-parser node-json-rpc bignumber.js wait.for



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

generally on ubuntu check here https://www.cyberciti.biz/faq/ubuntu-linux-start-restart-stop-apache-web-server/

edit ports in runLocalServer.js and runServer.js

sudo node runLocalServer.js runServer.js respectively

check if you get a 404 on http://localhost:port/api.mew

sudo node runServer.js

on bitnami make sure apache works right /80/443 SSL: Error: listen EADDRINUSE :::443
https://community.bitnami.com/t/how-do-i-host-my-app-on-port-80/40977/7
switch of bitnami apache altogether
https://community.bitnami.com/t/how-can-i-completely-disable-apache-and-use-node-js-on-port-80/10330/2

if you want to switch of apache https://www.cyberciti.biz/faq/ubuntu-linux-start-restart-stop-apache-web-server/


-------------
problems
------------

i get error 33 when I try to connect to custom node. Where can I find the source of this error?

started the node on my machine like this

nohup sudo geth --port 30304 --rpc --rpcaddr "0.0.0.0" --rpcport 8101 --rpccorsdomain "*" --rpcapi="eth,net,web3,utils" --datadir myDataDir --networkid 19720502 --bootnodes="enode:////cf2a1e3bb2cfe5a8aed058b609d6f4c844238e44425a7b24e422ce61cd971257859db2a8c4584acfe9bd65ffbec78d7db5cba14cbf32953f8f5c94e08135b20c@46.231.206.125:30304" &



on my server
I downloaded MEW 3.11.2 
changed nodeIP.json and put in the IP adress 46.231.206.125 instead of x.x.x.x
changed the ports from 8584 to 8101 in the file response.js 
made sure ssl is installed https://sslanalyzer.comodoca.com/?url=46.231.206.125

switched off apache (because port 80 was busy) using https://www.cyberciti.biz/faq/ubuntu-linux-start-restart-stop-apache-web-server/

then I typed 

sudo node runServer.js

it runs without errors however if I try to connect via MEW custom node 
https://46.231.206.125 port 8101 
clicking on custom and networkid in eip1155

I get 

(error_33) Could not connect to the node. Refresh your page, try a different node (top-right corner), check your firewall settings. If custom node, check your configs.

what can I do to find out what the problem could be?

Here is some background information

However if I do this locally on my machine it all works, i can access the local node when I do this:

changed nodeIP.json and put in the IP Adress 127.0.0.1
changed in response.js the ports to 8101
sudo node runLocalServer.js 
and accessing it by opening MEW locally and using http://127.0.0.1 port 8101 clicking on custom and typing in the correct networkid in eip1155



