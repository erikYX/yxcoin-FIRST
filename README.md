##YXcoin (YXC) - 

http://devtome.com/doku.php?id=scrypt_altcoin_cloning_guide     

=======================================================================    
##Installation Linux  

$ sudo apt-get install   
$ sudo apt-get install build-essential libboost-all-dev libcurl4-openssl-dev libdb5.1-dev libdb5.1++-dev git qt-sdk libminiupnpc-dev

Libraries & dependencies:   
libboost-all-dev - Boost C++ Libraries dev   
libcurl4-openssl-dev - libcurl (OpenSSL flavour)   
libdb5.1-dev - Berkeley v5.1 Database Libraries   
libdb5.1++-dev - Berkeley v5.1 Database Libraries runtime   
git - git version control system   
qt-sdk - QT-SDK platform  https://qt-project.org/    
libminiupnpc-dev - UPnP IGD client lightweight library dev   

s sudo dd if=/dev/zero of=/swapfile bs=64M count=16   
$ sudo mkswap /swapfile   
$ sudo swapon /swapfile   


 $ git clone https://github.com/erikYX/yxcoin.git
 $ cd yxcoin/src
 yxcoin/src$ make -f makefile.unix
 yxcoin/src$ strip yxcoin
 $ cp -r yxcoin /usr/local/bin/yxcoin
 
 
 $ yxcoin excryptwallet <passphrase>
 
 Commands:
 $ yxcoin & - start yxcoin server daemon
 $ yxcoin getinfo - basic info JSON array
 $ yxcoin listtransactions - show transactions to wallet
 $ yxcoin setgenerate true 1 - start mining
 $ yxcoin getmininginfo - mining status
 $ yxcoind setgenerate false - stop mining
 $ yxcoin stop - stop server daemon
 
 
 
Ports - 2523 RCP, 2524 P2P 

  
Coin data:   
Coins per block = 23   
Block Interval = 300   // 5 minutes   
Difficulty reset  =  1 * 24 * 60 * 60 // once/day     
Max Money = 1000000 // 1 million total coins   
Estimated coins per day = 6624 // 24 * 60 / 5 = 288 blocks * 23 YXC per block   

Pubkey Address prefix = 77  // starts with Y or X  

Images and icons in  /src/qt/res/     

Genesis Block: 
block.nTime = 1424404186
block.nNonce = 2086780778
block.GetHash = 9a3149370ea97c017b3d8853abadd614c28d59a96084efb3f97c25178cd943a1
CBlock(hash=9a3149370ea97c017b3d, PoW=00000c1a342387447aea, ver=1, hashPrevBlock=00000000000000000000, hashMerkleRoot=f9669a1832, nTime=1424404186, nBits=1e0ffff0, nNonce=2086780778, vtx=1)
  CTransaction(hash=f9669a1832, ver=1, vin.size=1, vout.size=1, nLockTime=0)
    CTxIn(COutPoint(0000000000, -1), coinbase 04ffff001d010446322e31392e323031352d56616e696c6c61204963652072656c6561736564206166746572206265696e67206368617267656420696e20466c6f7269646120627572676c617279)
    CTxOut(error)
  vMerkleTree: f9669a1832
  
  
=======================================================================

a fork of yxcoin, https://github.com/bfroemel/yxcoin    
diff - https://github.com/bfroemel/yxcoin/commit/947a0fafd8d033f6f0960c4ff0748f76a3d58326   


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
 - YXC proves that really anyone(!) can start a Litecoin/Bitcoin based currency
    (just look at the changes I applied to the original Litecoin source,
     for genesis block generation look at main.cpp)
 - allows me to experiment with coin parameters (in a private network)

Finally, I only tested the command line server/tool 'yxcoin' for the
first 30 blocks. Credits go to the original authors/communities that
created Bitcoin and Litecoin.

