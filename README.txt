Simplyvitahlth is one of three pieces that work together in a one-way flow among the three (like in a money circle).

The hashed components here are de-identified. Identity is retrievable outside this blockchain, through another blockchain. Any person can thereby get their personal puzzle re- pieced back together, since the person knows the pieces (where they were, with whom, which subject was discussed) and they have the means to activate the (re-)assembly of their personal aggregate file, and without informing anyone internal to this system or the associated systems, whether the "anyone" is a provider or any other role.

Service providers work together to manage the shareable information of their people. The use of blockchain technology enables providers to view records across all providers: the records are authenticated and non-repudiable, viewable in realtime (i.e. simultaneously).

Caveat: trends are revealed in data, metadata and metametadata, that impact our insurability, hirability, and security (safety). So sharing requires strong de-identification and one-way checks. The right care pathway must follow in the right order by the right providers. More about this, later. 

Simplyvitahlth allows providers to share CCD-level files, and allows higher-order access to administrators and coordinators. Also, authorized stakeholders (e.g. payors) can audit with real time access, and can dig into event history data e.g. to identify root causes where results deviate significantly from averages.


Instructions for this fork.
Git clone the Repo
npm install
Download and install Geth
Go to https://www.myetherwallet.com/
Create two wallets, save all the information and download the keystores
Perform geth -datadir "path" --networkid 12345 init
Go to the data directory and delete everything but the keystore, then add the keys you obtained from the wallet to it
After that edit the genesis block with your addresses, delete the extras or create more keys, by adding in the address for the keys you generated earlier and make sure you make the first allocation your keybase, Also  sub out the same corresponding addresses in the controllers/blockchain
now perform geth  --datadir="pathToKeystoreDir"  --networkid 12345 init "pathToGensisBlock"
example
  geth --datadir="/tmp/eth/60/01" init ./config/genesis.json

then exit geth
now launch the ethereum server
geth --dev --datadir="pathToKeystoreDir" --etherbase "coinbase address"  --maxpeers 0 --gasprice 0 --port 0 --shh --networkid 12345 --mine --minerthreads 8  --nodiscover --ipcdisable --port 30301 --rpc  --rpcport 8101 console
example
geth --dev --datadir="/tmp/eth/60/01" --etherbase 0xDDF083793273Dbb490282e09007EEb61020433c8  --maxpeers 0 --gasprice 0 --port 0 --shh --networkid 12345 --mine --minerthreads 8  --nodiscover --ipcdisable --port 30301 --rpc  --rpcport 8101 console

In another terminal go to the project file and perform node app.js

This demo's data storage and viewing. It is a "smart contract" in the Ethereum sense of smart contract.




