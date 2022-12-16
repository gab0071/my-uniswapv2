<h1 aling="center">Uniswap V2 📚⛓✨</h1>


 <a href="https://github.com/maurodesouza/profile-readme-generator/blob/master/LICENSE.md" target="_blank">
    <img alt="Badge showing project license type" src="https://img.shields.io/github/license/maurodesouza/profile-readme-generator?color=f85149">
  </a>


  <a href="#" target="_blank">
    <img src="https://img.shields.io/badge/Solidity-%5E8.0.4-363636?style=flat-square" alt="Badge showing the solidity version"/>
  </a>


  <a href="https://www.npmjs.com/package/remixd" target="_blank">
    <img src="https://img.shields.io/badge/remixd-^0.6.9-blue.svg" alt="Badge showing the remixd version"/>
  </a>

  <a href="https://github.com/gab0071" target="_blank">
    <img alt="Author" src="https://img.shields.io/badge/made%20by-CatellaTech-blueviolet?style=flat-square">
  </a>
 

  <br>
  <br>

 Working with uniswap v2, both `v2-core-master/contracts/UniswapV2Factory.sol` and `v2-periphery-master/contracts/UniswapV2Router02.sol`. All to understand the design of the first DEX in web3, I was able to successfully implement and deploy the contract.

First we must add to the Factory contract this variable `bytes32 public constant INIT_CODE_HASH = keccak256(abi.encodePacked(type(UniswapV2Pair).creationCode));` we will need this when we deploy our router.

To properly implement `v2-periphery-master/contracts/UniswapV2Router02.sol`, you must add `INIT_CODE_HASH` in the `v2-periphery-master/contracts/libraries/UniswapV2Library.sol` file and remove `0x` so that it does not return any error, then we must have the Factory address and this Wrapped Eth address for testnet `0xb4fbf271143f4fbf7b91a5ded31805e42b2208d6`.

Once the router is deployed we can access the great functions of the DEX, such as:

- addLiquidity
- removeLiquidity
- swapTokensForExactTokens

among others.

🚨 One of the errors I found when trying to deploy the router was this error `the size of the contract code exceeds 24576 bytes`, to fix it you must enable the optimizer in remix ide and put `2000`, if you are working with a framework like truffle or hardhat you can do it too, no problem.


It was super interesting to do this, to better understand the architecture of one of the most important Dexs in the web3 ecosystem.
<br>

<h2> Installing / Getting started </h2>

```bash

# Clone this project
$ git clone https://github.com/gab0071/my-uniswapv2

# Access
$ cd my-uniswapv2

# Install dependencies
$ npm install 

``` 

<p>Drop all necessary dependencies</p>
<hr>

<h2>Commands</h2>

- $ `npm run start `

<h2> Technologies / Built With </h2>

- Solidity
- Remix -Ethereum-IDE
- Metamask
- Fake ETH (🚨 Note: <a href="https://goerlifaucet.com/"> Goerli Faucet</a>)
- <a href="https://remix-ide.readthedocs.io/en/latest/remixd.html"> Remixd  </a>


<h2>Contributing</h2>

<p> Contributions are always welcome! Open a PR or an issue!</p>

<p> Thank you! 😊 </p>
  
<br>
<br>

<p align="center">
<a href="https://www.linkedin.com/in/blockchain-gabriela-mendes/" target="_blank" >
  <img alt="Linkedin - J.Gabriela" src="https://img.shields.io/badge/Linkedin--%23F8952D?style=social&logo=linkedin">
</a>
<a href="mailto:jeicarm7@gmail.com" target="_blank" >
  <img alt="Email - J.Gabriela" src="https://img.shields.io/badge/Email--%23F8952D?style=social&logo=gmail">
</a> 
<br/>
  Made with ❤️ by <b>catellaTech</b>.
<p/>