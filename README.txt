Service providers to work together to manage the shareable information of their people.

Data / metadata reveals trends that impact our insurability and hirability. So, sharing requires strong de-identification and one-way checks. More technically expressed: it is necessary to ensure that the right care pathway is followed in the right order by the right providers. Our platform allows providers to easily share CCD-level files with their teams, which in turn allows higher-order access to administrators and coordinators.

The use of blockchain technology enables providers to view authenticated non-repudiable records at the same time regardless of team affiliation.

Payors can audit with real time access, and can dig into event history data to identify root causes where results deviate significantly from averages.


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
This will demo simple data storage with viewing and shows a smart contract




