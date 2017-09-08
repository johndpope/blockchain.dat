# blockchain.dat
torrent location https://getbitcoinblockchain.com/blockchain.torrent

⛳️   


https://gist.github.com/sathoro/9770281
     
   
check https://getbitcoinblockchain.com/ for latest torrent    
      
Torrent	Size	Last update	Status     
blockchain.torrent	138.53 Gb      
(148,746,848,245 bytes)	2017-09-01 05:30:38       
UTC+02:00	seeding      
update.torrent	3.67 Gb      
(3,941,208,891 bytes)	2017-09-08 01:20:42          
UTC+02:00	seeding                   


````bash
# note: the blockchain is over 140 GBs and continues to grow. make sure you have adequate storage

mkdir ~/.bitcoin/

# use transmission to download the bootstrap.dat file
sudo apt-get install transmission-cli
wget http://sourceforge.net/projects/bitcoin/files/Bitcoin/blockchain/bootstrap.dat.torrent/download
mkdir ./blockchain
transmission-cli -D -u 0 -w ~/.bitcoin bootstrap.torrent

# install bitcoind
sudo apt-get install python-software-properties
sudo add-apt-repository ppa:bitcoin/bitcoin
sudo apt-get update
sudo apt-get install bitcoind

# create configuration file for bitcoind
nano ~/.bitcoin/bitcoin.conf




server=1
daemon=1
rpcuser=RANDOM
rpcpassword=RANDOM

bitcoind -loadblock=~/.bitcoin/bootstrap.dat

