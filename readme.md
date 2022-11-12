# steps to create your own private neywork using ethereum Geth

Getg(Go lang, Ethereum) - So geth is an command line interface for running ethereum node . It is implemented in Go lang

You can join etehreum network and do mining and become a node to confirm your transaction

visit - https://geth.ethereum.org/downloads/ and dowload geth based on your operating system

Type <strong>geth</strong> in your terminal an it start in fastsync mode

Fastsync - Only sync headers

Stop the terminal and retype geth in your terminal and it will start in fullsync mode

Fullsync - Download whole blockchain from its nearest nodes

To connect with your runnig network on your local machine type following commnand
    <code> geth attach ipc://./pipe/geth.ipc </code>

create accounts 
    <code>personal.newAccount()</code>

Get accounts
    <code>eth.accounts</code>

<h1>Create private network</h1>

use genesisi.json file to configure your network
after create genesis.json file type following command 
    <code> geth init --datadir Eth .\genesis.json</code>

To start it run 
    <code> geth --datadir .\Eth\ --nodiscover</code>

nodiscover - The chain ID will not be available for other nodes , so that these will become a private network

Then open new terminal and run connect command 
    <code> geth attach ipc://./pipe/geth.ipc </code>

Create an account

Set the account as miner
    <code>eth.setEtherbase(eth.accounts[0]) </code>

Start mining
    <code>miner.start(Number of core you eant to used by miner)</code>

Get account balance
    <code> eth.getBalance(eth.accounts[0])

For more information visit
    https://geth.ethereum.org/docs/