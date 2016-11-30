# User Guide

All information for developers using `ethjs-provider-http` should consult this document.

## Install

```
npm install --save ethjs-provider-http
```

## Usage

```js
const HttpProvider = require('ethjs-provider-http');
const Eth = require('ethjs-query');
const eth = new Eth(new HttpProvider('http://ropsten.infura.io'));

eth.getBlockByNumber(45039930, cb);

// result null { hash: 0x.. etc.. }
});
```

## API Design

### constructor

[index.js:ethjs-provider-http](../../../blob/master/src/index.js "Source code on GitHub")

Intakes a `provider` URL specified as a string, and optionally the `timeout` specified as a Number, outputs a web3 standard `HttpProvider` object.

**Parameters**

-   `provider` **String** the URL path to your Http RPC Ethereum node (e.g. `http://localhost:8545`) or a service node (e.g. `http://ropsten.infura.io`).
-   `timeout` **Number** [optional] the time in seconds that an XHR2 request will wait until it times out.

Result HttpProvider **Object**.

```js
const Eth = require('ethjs-query');
const HttpProvider = require('ethjs-provider-http');
const eth = new Eth(new HttpProvider('http://localhost:8545'));

eth.accounts((err, result) => {
  // result null ['0xd89b8a74c153f0626497bc4a531f702...', ...]
});
```

## Other Awesome Modules, Tools and Frameworks

 - [web3.js](https://github.com/ethereum/web3.js) -- the original Ethereum swiss army knife **Ethereum Foundation**
 - [ethereumjs](https://github.com/ethereumjs) -- critical ethereumjs infrastructure **Ethereum Foundation**
 - [wafr](https://github.com/silentcicero/wafr) -- a super simple Solidity testing framework
 - [Truffle](https://github.com/ConsenSys/truffle) -- a solidity/js dApp framework
 - [Embark](https://github.com/iurimatias/embark-framework) -- a solidity/js dApp framework
 - [dapple](https://github.com/nexusdev/dapple) -- a solidity dApp framework
 - [chaitherium](https://github.com/SafeMarket/chaithereum) -- a JS web3 unit testing framework
 - [browser-solidity](https://ethereum.github.io/browser-solidity) -- an in browser Solidity IDE **Ethereum Foundation**
 - [contest](https://github.com/DigixGlobal/contest) -- a JS testing framework for contracts

## Our Relationship with Ethereum & EthereumJS

 We would like to mention that we are not in any way affiliated with the Ethereum Foundation or `ethereumjs`. However, we love the work they do and work with them often to make Ethereum great! Our aim is to support the Ethereum ecosystem with a policy of diversity, modularity, simplicity, transparency, clarity, optimization and extensibility.

 Many of our modules use code from `web3.js` and the `ethereumjs-` repositories. We thank the authors where we can in the relevant repositories. We use their code carefully, and make sure all test coverage is ported over and where possible, expanded on.
