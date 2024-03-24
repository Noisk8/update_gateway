# update_gateway

~~~

sudo systemctl stop nym-gateway.service
~~~

~~~
wget https://github.com/nymtech/nym/releases/download/nym-binaries-v2024.2-fast-and-furious/nym-gateway
~~~



~~~
sudo chmod +x nym-gateway
~~~

~~~
./nym-gateway init --id Nodes-Hub --listening-address 0.0.0.0 --public-ips "$(curl -4 https:/ifconfig.me)" --with-network-requester --with-exit-policy true
~~~

~~~
./nym-gateway setup-ip-packet-router --id NOMBREDELNODO --enabled true
~~~


~~~
curl -o enable_networking_for_nym_nodes.sh https://gist.githubusercontent.com/tommyv1987/ccf6ca00ffb3d7e13192edda61bb2a77/raw/0840e1d2ee9949716c45655457d198607dfd3107/enable_networking_for_nym_nodes.sh -L && chmod u+x enable_networking_for_nym_nodes.sh && sudo ./enable_networking_for_nym_nodes.sh
~~~


  
~~~
sudo systemctl restart nym-gateway.service
~~~
