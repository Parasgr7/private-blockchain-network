# Running Private Blockchain Network

## Generate Bootnode key
`bootnode -genkey boot.key`

## Running Bootnode
`bootnode -nodekey boot.key -addr :30305`

## Initialize Genesis file
`geth init --datadir node1[or node2] genesis.json`

## Running javascript console
`geth attach geth.ipc`

## Running Node 1
`geth --datadir ./node1 --bootnodes=enode://756ca0a954e6118bc19dcdb6990d5bf826b76a17dd312a25ac9f1da1d5b2f4d8fd1641d46bca153b0170b83cdd874393bf1bd23d382771219f98ca3980b9eb08@127.0.0.1:0?discport=30301 --mine --miner.threads=1 --miner.etherbase=0x1878986763e0E964c1740df7E9bbC894972E3feF --unlock=0x1878986763e0E964c1740df7E9bbC894972E3feF  --password node1/password.txt --rpc --rpcaddr 127.0.0.1 --rpcport 8551 --rpcapi eth,web3,personal,miner,clique,net,admin --rpccorsdomain="*" --allow-insecure-unlock`

## Running Node 2
`geth --datadir ./node2 --bootnodes=enode://756ca0a954e6118bc19dcdb6990d5bf826b76a17dd312a25ac9f1da1d5b2f4d8fd1641d46bca153b0170b83cdd874393bf1bd23d382771219f98ca3980b9eb08@127.0.0.1:0?discport=30301 --mine --miner.threads=1 --miner.etherbase=0xfFc6AF2560CE5e9c9c901f05D4C312D8d8A0C50b --unlock=0xfFc6AF2560CE5e9c9c901f05D4C312D8d8A0C50b --port 30306 --password node1/password.txt --rpc --rpcaddr 127.0.0.1 --rpcport 8552 --rpcapi eth,web3,personal,miner,clique,net,admin --rpccorsdomain="*" --allow-insecure-unlock`

## Reference
Docs:
https://geth.ethereum.org/docs/fundamentals/private-network
