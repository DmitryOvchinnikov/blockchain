## Running The Project

This project can be run in one of two ways, you can use docker compose or run different nodes separately.

### Docker Compose

Start a docker compose environment which will run three instances of a node with local disk space. These nodes will all start with an empty blockchain database.

```
$ make docker-up
```

Bring down the nodes cleanly.

```
$ make docker-down
```

To see the logs from the three running nodes.

```
$ make docker-logs
```

### Run Manually

This is the way I prefer to run the project and we will run like this in class. Open two terminal windows in your terminal application.

To run the primary node.

```
$ make up
```

To run the second node.

```
$ make up2
```

To bring both nodes dow, run this command twice.

```
$ make down
$ make down
```

### Sending Transactions

You can use the Wallet to send transactions. In the genesis file you will see two origin accounts with a million coins each. These are the public addresses for the known accounts.

```
Dmitry: 0xF01813E4B85e178A83e29B8E7bF26BD830a25f32  (Origin Account)
Pavel:   0xdd6B972ffcc631a62CAE1BB9d80b7ff429c8ebA4  (Origin Account)
Ceasar:  0xbEE6ACE826eC3DE1B6349888B9151B92522F7F76
Baba:    0x6Fe6CF3c8fF57c58d24BfC869668F48BCbDb3BD9
Ed:      0xa988b1866EaBF72B4c53b592c97aAD8e4b9bDCC0
Miner1:  0xFef311483Cc040e1A89fb9bb469eeB8A70935EF8
Miner2:  0xb8Ee4c7ac4ca3269fEc242780D7D960bd6272a61
```

When a node starts it will read the `zblock/accounts` folder for accessing the known accounts and their private keys.

You can also use this command to send in an initial six transactions.

```
$ make load
```

This command issues the following commands using the project's CLI tooling.

```
$ go run app/wallet/cli/main.go send -a dmitry -n 1 -t 0xbEE6ACE826eC3DE1B6349888B9151B92522F7F76 -v 100
$ go run app/wallet/cli/main.go send -a pavel -n 1 -t 0xbEE6ACE826eC3DE1B6349888B9151B92522F7F76 -v 75
$ go run app/wallet/cli/main.go send -a dmitry -n 2 -t 0x6Fe6CF3c8fF57c58d24BfC869668F48BCbDb3BD9 -v 150
$ go run app/wallet/cli/main.go send -a pavel -n 2 -t 0xa988b1866EaBF72B4c53b592c97aAD8e4b9bDCC0 -v 125
$ go run app/wallet/cli/main.go send -a dmitry -n 3 -t 0xa988b1866EaBF72B4c53b592c97aAD8e4b9bDCC0 -v 200
$ go run app/wallet/cli/main.go send -a pavel -n 3 -t 0x6Fe6CF3c8fF57c58d24BfC869668F48BCbDb3BD9 -v 250
```

### Consensus

The default is Proof Of Work and the two blocks that come with the project are built on this protocol. If you want to try running Proof of Authority, change the setting in main.go for the node.

```
State struct {
	Beneficiary    string   `conf:"default:miner1"`
	DBPath         string   `conf:"default:zblock/miner1/"`
	SelectStrategy string   `conf:"default:Tip"`
	OriginPeers    []string `conf:"default:0.0.0.0:9080"`
	Consensus      string   `conf:"default:POW"`            <- Change to POA
}
``` 

Then remove the existing blocks from the `zblock` folder and run the `make up` and `make up2` commands.

### Other Functionality

Please review the project's makefile for other commands and options.