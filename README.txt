This is one of three pieces of a sequence. Example: a money circle.

The identity is stripped from the hashed components. Identity is then retrievable outside this blockchain, through another blockchain. Any person can thereby get their personal puzzle reassembled since the location, subject, and the recipient is known. In addition, the means to reassemble the personal aggregate file exists universally and discretely.

Service providers work together to manage shared client information. The use of blockchain technology enables providers to view all authenticated undisputed information in real-time, simultaneously.

Caveat: Trends are revealed in data and metadata that affect our liability, desirability, and sense of security. Sharing requires strong anonymity and authentication. The right care pathway must follow in the right order by the right providers. More about this, later. 

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




