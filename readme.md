



# Rocket.Chat

## ubuntu VM
https://rocket.chat/docs/installation/manual-installation/ubuntu/

vagrant@vagrant-ubuntu-trusty-64:~$ mongo --version
MongoDB shell version: 3.0.12


echo 'setw -g mode-keys vi' > ~/.tmux.conf

cd /Users/twer/hszou/spikes/spike-rocketchat
vagrant ssh
sudo su - root
cd /root/Rocket.Chat
export ROOT_URL=http://192.168.1.113:3009/
export MONGO_URL=mongodb://localhost:27017/rocketchat
export PORT=3009

node main.js


192.168.1.113
