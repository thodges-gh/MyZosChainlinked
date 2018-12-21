# Create a Chainlinked contract with ZeppelinOS

Setup

```
npm install
zos init MyZosChainlinkedProject
zos link chainlinked
```

Add and deploy the contract

```
zos add MyContract
zos session --network ropsten
zos push --force
zos create MyContract --init initialize
```

Interact with the contract

```
truffle console --network ropsten
MyContract.at('<your-contract-instance-address>').then(s => s.getChainlinkToken())
```