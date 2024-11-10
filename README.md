Perintah Install CPU Miner di Termux

pkg update
pkg upgrade
termux-setup-storage


Install Ubuntu SH
pkg update -y && pkg install curl proot tar -y && curl https://raw.githubusercontent.com/AndronixApp/AndronixOrigin/master/Installer/Ubuntu/ubuntu.sh | bash

./start-ubuntu.sh
apt update && apt upgrade
apt install wget
apt install proot
apt install git
apt install git build-essential cmake libuv1-dev libmicrohttpd-dev libssl-dev
apt-get install automake autoconf pkg-config libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev make g++

kita clone script nya dari github.com
apt-get install -qqy automake
apt-get install -qqy libcurl4-openssl-dev
apt-get install -qqy make
git clone https://github.com/magi-project/wolf-m7m-cpuminer-V2.git
cd wolf-m7m-cpuminer-V2
./autogen.sh
./configure CFLAGS="-O3"
make
 
./minerd -a sha256d -o stratum+tcp://public-pool.io:21496 -u bc1qvxth5ug4n87esl59uly3cnq0t62grp069met7z.Mobile -p x -t 4
