##YXcoin (YXC) - 

http://devtome.com/doku.php?id=scrypt_altcoin_cloning_guide     

=======================================================================    
##Installation Linux  

sudo apt-get install   
sudo apt-get install build-essential libboost-all-dev libcurl4-openssl-dev libdb5.1-dev libdb5.1++-dev git qt-sdk libminiupnpc-dev

Libraries & dependencies:   
libboost-all-dev - Boost C++ Libraries dev   
libcurl4-openssl-dev - libcurl (OpenSSL flavour)   
libdb5.1-dev - Berkeley v5.1 Database Libraries   
libdb5.1++-dev - Berkeley v5.1 Database Libraries runtime   
git - git version control system   
qt-sdk - QT-SDK platform  https://qt-project.org/    
libminiupnpc-dev - UPnP IGD client lightweight library dev   

=======================================================================

a fork of smallchange, https://github.com/bfroemel/smallchange    
diff - https://github.com/bfroemel/smallchange/commit/947a0fafd8d033f6f0960c4ff0748f76a3d58326   


a 'faster' version of Litecoin which also uses scrypt
as a proof of work scheme and is intended for microtransactions.
 - 15 seconds block targets: beat that MinCoin! ;)
 - 42 007 680 total coins
 - no subsidy within the first 3 days and after approximately 5 years;
    in between: 4 coins per generated block
 - difficulty retargets every 0.35 days
 - currently peers are looked up over IRC only
 - currently no block checkpoints are in the code (but could be easily
   added)
Other than that, this coin is exactly like Litecoin and should by no
means be used as a real cryptocurrency. All of the coin parameters
are chosen arbitrarily or at most with 'fairness' towards everyone in mind.

So actually, this 'new' coin exists for the following reasons:
 - SMC proves that really anyone(!) can start a Litecoin/Bitcoin based currency
    (just look at the changes I applied to the original Litecoin source,
     for genesis block generation look at main.cpp)
 - allows me to experiment with coin parameters (in a private network)

Finally, I only tested the command line server/tool 'smallchange' for the
first 30 blocks. Credits go to the original authors/communities that
created Bitcoin and Litecoin.

