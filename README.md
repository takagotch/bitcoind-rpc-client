### bitcoind-rpc-client
---
https://github.com/fanatid/bitcoind-rpc-client

```js
var client = new RpcClient({
  host: '127.0.0.1',
  port: 18332
});
client.set('user', 'bitcoinrpc')

client.getNewAddress(function (err, result) {
  console.log(err, result)
})

client.getNewAddress().then(function (result) {
  console.log(result)
})

client.getnewaddress().then(function (result) {
  console.log(result)
})

client.batch([
  {method: 'getnewaddress', params: ['myaccount']},
  {method: 'getnewaddress', params: ['myaccount']}
])
.then(function (result) {
  console.log(result)
})

client.batch()
  .getInfo()
  .clear()
  .getNewAddress('myaccount')
  .getNewAddress('secondaccount')
  .call()
  .then(function (result) {
    console.log(result)
  })
```

```sh
npm install bitcoind-rpc-client
```

```
```


