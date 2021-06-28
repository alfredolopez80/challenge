# vue-nuxt-eth-todolist-dapp
The is a decentralised application (DAPP) built on Vue-nuxt framework.
1. Creation of smart contract on truffle framework
2. Local blockchain for dev and test on Ganache
3. Browser connection to Blockchain using Metamask chrome plugin

## Dev Steps
1. Install Ganache
2. Install Metamask
3. Install dependencies
4. Configure local blockchain in metamask
5. Run the application

## Architecture components
1. nuxt
2. vue
3. truffle
4. web3

## Install smart contract
1. truffle compile
2. truffle migrate --reset

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev
```

## For Testing Start Ganache
---
```
ganache-cli --accounts=11 --account="0x1b0ad9d6e8a97221c35040986ddfe97a94c25fc1bba1462e3c1a2e353f057f7c,100000000000000000000" --account="0x3a975be325e5a3036a50959964eca6196e7f69584af46fe011260911ec559333,100000000000000000000" --account="0xd38554ee3ae59e5bcc56fc1e6e410f63149253dc2985bb1ada95ed6cb4030747,100000000000000000000" --account="0x24a978303c0a5e108375291269256c16c456d20c69984d8c98d3e0a29f3d8856,100000000000000000000" --account="0x36b00c11efcf62d79a80e89ef5818aca7d41197a6ab24d7ef8d3d4d355ccb7f5,100000000000000000000" --account="0xeab12f85e1bfd5ff03b407d8edb41a65aa8553203a80f12f7b42d287dbbcc31e,100000000000000000000" --account="0x653a8335c6281c7f8b7c4e13ed109c43ffcf47e560557e40c1331b0d571b494c,100000000000000000000" --account="0x385f1cd2465f1453dcbfad46bb32f4877b35c224cfc0040e41b404fe3c571743,100000000000000000000" --account="0xd5520f4d78a75a032fabd32e6989d57990199c29b37b172f4c60c6dc0101682c,100000000000000000000" --account="0x08f66f02a5e6ab6685b9dbff2cfb841d97fcad7034e6649976ea62f6223f9e85,100000000000000000000" --account="0x14d21d01b8ec16a656db8265b55ddedaa6babe5dc69cf35b49ce5152e5a82629,100000000000000000000" --account="0x1f40466553f8bdaa6d88aaf5edcb7bd6d9e64ed987948169a7d79d6c2327121e,100000000000000000000"
```

## EMDX Front End technical test

### Summary
The goal of this test is to make you code a small VueJS app.

The app will have three views, real time updated orderbook, a small dashboard with a graphic view and Metamask form interaction. Each view can be acceded via a link in a top navbar at the top of the app. The top navbar should read "RT Orderbook", "Candlesticks graphic" and "Wallet integration".

#### 1. Realtime orderbook

For the first tab, the dev will have to create an orderbook, as seen on any exchange, with price level, colored amounts, side, real time update, etc.
For this you can check the FTX WS/API (https://docs.ftx.com/) to fetch proper data, any pair will be ok, suggested btc/usd.

The order book will need to update real time and reflect proper updates by flashing the side / level that changed (with flash we say background color momentarily changed)

Finally, the price on each level should be clickeable, and the click event will have to fetch said price and show it on a alert or any div/tag/input on the same page.

#### 2. Candlesticks graphic view

The Candlesticks graphic should have an OHLCV chart (we recommend trading-vue-js) and it should be filled with proper formatted data. An example source can be:

https://api-pub.bitfinex.com/v2/candles/trade:1h:fUSD:a30:p2:p30/hist


* Information should also be updated real time coming from a websocket and the graph component should react to reflect changes properly.

#### 3. Metamask interaction

Browser wallets like Metamask (or Nifty or Liquality) are a practical way to interact with dApps and Dex projects using the web browser and in our case a essential part of the ecosystem.
It is critical that our developers knows how to code applications that connects to user's wallets and perform operations such as balance check, network detect, send orders, etc.

For this challenge the developer should be able to write proper VueJS component(s) to connect to Metamask and perform the following operations:

- Connect the VueJS app with Metamask and any testnet blockchain (Kovan, Ropsten, Rinkeby, RSK testnet, AVAX fuji, etc)
- Force check that network should be testnet
- On the UX (inside the aforementioned tab) show connected address balance
- keep the component and vuejs store updated realtime to reflect proper balance (even when a transaction receiving or sending is made)
- Construct and sign a transaction (no need to send to blockchain) but have the hexadecimal raw result is mandatory

Useful links:

- https://infura.io/
- https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=es
- https://developers.rsk.co/rsk/public-nodes/


### Submission

Fork this repository and send us a pull request with your code.
* Put the code within a folder named as your github/bitbucket username.
* Add a readme file with the steps to run the app.

We'll review it and get back to you in order to talk about the submission

### Extra points

* Use a component library (We recommend Vuetify).
* Responsive design (Grid system, Flexbox, CSS Grid).
* Add test cases to components.



Contact us at  [jobs@emdx.io](mailto:jobs@emdx.io)  if you need more details.

