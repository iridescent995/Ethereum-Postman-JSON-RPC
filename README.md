# Ethereum-Postman-JSON-RPC
A collection holding all the Ethereum JSON RPC API calls which can be used from POSTMAN

### POST accounts
Returns a list of addresses owned by client.
```
curl --request POST \
  --url 'http://localhost:8545/' \
  --header 'Content-Type: application/json' \
  --data '{
	"jsonrpc":"2.0",
	"method":"eth_accounts",
	"params":[],
	"id":1
}'
```

### POST getTransactionCount
Returns the number of transactions sent from an address.
```
curl --request POST \
  --url 'http://localhost:8545/' \
  --header 'Content-Type: application/json' \
  --data '{
	"jsonrpc":"2.0",
	"method":"eth_getTransactionCount",
	"params":[
		"0x407d73d8a49eeb85d32cf465507dd71d507100c1",
		"latest"
	],
	"id":1
}'
```

### POST sendTransaction
Creates new message call transaction or a contract creation, if the data field contains code.
```
curl --request POST \
  --url 'http://localhost:8545/' \
  --header 'Content-Type: application/json' \
  --data '{
	"jsonrpc":"2.0",
	"method":"eth_sendTransaction",
	"params":[{
		"from": "0xb60e8dd61c5d32be8058bb8eb970870f07233155",
		"to": "0xd46e8dd67c5d32be8058bb8eb970870f07244567",
		"gas": "0x76c0",
		"gasPrice": "0x9184e72a000",
		"value": "0x9184e72a",
		"data": "0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675"
	}],
	"id":1
}'
```
### POST call
Executes a new message call immediately without creating a transaction on the block chain.
```
curl --request POST \
  --url 'http://localhost:8545/' \
  --header 'Content-Type: application/json' \
  --data '{
	"jsonrpc":"2.0",
	"method":"eth_call",
	"params":[{
		"from": "",
		"to": "",
		"gas": "",
		"gasPrice": "",
		"value": "",
		"data": ""
	}, "latest"],
	"id":1
}'
```
