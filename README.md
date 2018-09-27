BaisycCoin (fork of LightPayCoin) integration/staging repository
======================================


It is recommended [use the shell script](https://github.com/BaisycCoin/bsycInstall) to install a BaisycCoin Masternode on a Linux server running Ubuntu 16.04 or 18.04

***

Quick installation of the BaisycCoin daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/BaisycCoin/BaisycCoin.git
    cd BaisycCoin
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip baisyccoind
    sudo strip baisyccoin-cli
    sudo strip baisyccoin-tx
    cd ..

Running the daemon:

    baisyccoind 

Stopping the daemon:

    baisyccoin-cli stop

Demon status:

    baisyccoin-cli getinfo
    baisyccoin-cli mnsync status

All binaries for different operating systems, you can download in the releases repository:

https://github.com/BaisycCoin/BaisycCoin/releases

P2P port: 64578, RPC port: 64579
-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.
