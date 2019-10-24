# eth_private_chain
以太坊私有鏈——初始檔案

* 全節點 tx while mining
```shell=
geth --datadir data --networkid 33 --ws --wsaddr "0.0.0.0" --wsapi "eth,web3,personal,debug,db,admin,miner,net,shh,txpool" --wsport 8546 --wsorigins "*" --rpc --shh --rpcport 8545 --rpccorsdomain "*" --rpcapi " eth,web3,personal,debug,db,admin,miner,net,shh,txpool " --preload "mineWhenNeeded.js" --nodiscover console
```


* 當使用light node時，主節點用（加上-lightpeers 50 --lightserv 90 ）
```shell=
geth --datadir data --networkid 33 --ws --wsaddr "0.0.0.0" --lightpeers 50 --lightserv 90 --wsapi "eth,web3,personal,debug,db,admin,miner,net,shh,txpool" --wsport 8546 --wsorigins "*" --rpc --shh --rpcport 8545 --rpccorsdomain "*" --rpcapi " eth,web3,personal,debug,db,admin,miner,net,shh,txpool " --nodiscover console
```

* 當使用light node時，主節點用,有tx時在mining模式（加上-lightpeers 50 --lightserv 90 ）
```shell=
geth --datadir data --networkid 33 --ws --wsaddr "0.0.0.0" --lightpeers 50 --lightserv 90 --wsapi "eth,web3,personal,debug,db,admin,miner,net,shh,txpool" --wsport 8546 --wsorigins "*" --rpc --shh --rpcport 8545 --rpccorsdomain "*" --rpcapi " eth,web3,personal,debug,db,admin,miner,net,shh,txpool " --preload "mineWhenNeeded.js" --nodiscover console
```

* 輕節點
```shell=
geth --datadir data --networkid 33 --ws --wsaddr "0.0.0.0" --wsapi "eth,web3,personal,debug,db,admin,miner,net,shh,txpool" --wsport 8546 --wsorigins "*" --syncmode="light" --rpc --shh --rpcport 8545 --rpccorsdomain "*" --rpcapi " eth,web3,personal,debug,db,admin,miner,net,shh,txpool " --nodiscover console
```


