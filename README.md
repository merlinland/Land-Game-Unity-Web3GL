# Land Game Unity Web3GL Template

## Methods in Browser


Dispay login modal:

```javascript
window.web3gl.connect();
```

Get Network:

```javascript
window.web3gl.networkId;
```

Get Connected Address:

```javascript
window.web3gl.connectAccount;
```

To Send Transaction:

```javascript
const to = "0x0F732016741BCA7b9114ab43e179dc426aEE583b";
const value = "12300000000000000";
const gasLimit = "21000"; // gas limit
const gasPrice = "33333333333";
window.web3gl.sendTransaction(to, value, gasLimit, gasPrice);
```

To Interact with Contract:

```javascript
const method = "increment";
const abi = `[ { "inputs": [], "name": "increment", "outputs": [], "stateMutability": "nonpayable", "type": "function" }, { "inputs": [], "name": "x", "outputs": [ { "internalType": "uint256", "name": "", "type": "uint256" } ], "stateMutability": "view", "type": "function" } ]`;
const contract = "0x0F732016741BCA7b9114ab43e179dc426aEE583b";
const args = "[]";
const value = "0";
const gasLimit = "222222"; // gas limit
const gasPrice = "333333333333";
window.web3gl.sendContract(method, abi, contract, args, value, gasLimit, gasPrice);
```

Add Custom Token Contract:

```javascript
const tokenContract = "0x63c2E663A6cFb0F5568c84a1C8134aCBe1b88BEc";
const tokenSymbol = "MerlinBox";
const decimals = "18";
const tokenImage = "https://merlinland.pro/images/logo500.png";

window.web3gl.addTokenFunction(tokenContract,tokenSymbol,decimals,tokenImage);
```

