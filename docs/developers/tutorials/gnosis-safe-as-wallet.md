---
id: gnosis-safe-tutorial
title: Gnosis Safe as Wallet
slug: /developers/tutorials/gnosis-safe-as-wallet
---

Circles comes with circles.garden as a web wallet for Circles (CRC Tokens). Internally, during the setup, a smart contract is deployed as a multisignature wallet. This smart contract is a [Gnosis Safe](https://gnosis-safe.io/) contract, therefore the Gnosis Safe web wallet can be used to access the Circles wallet.

## Open Gnosis Safe in read-only mode

This step-by-step-guide shows how to reuse the Gnosis Safe web wallet for Circles.

1. Login to [circles.garden/profile](https://circles.garden/profile), click on "Your Profile"

![](../assets/gnosis-safe-1.png)

2. Note down the address shown in the URL of your browser, eg. https://circles.garden/profile/YOUR_PROFILE_ADDRESS it starts with "0x"

![](../assets/gnosis-safe-2.png)

3. Go to https://xdai.gnosis-safe.io/app/#/safes/YOUR_PROFILE_ADDRESS/balances

So are now in read-only mode, but can see the current balances of your (and other) CRCs, but also xDai and other Tokens.

## Import wallet address for write access

_Note: For write access you need xDai on your account, a small amount like $0.1 already allows for some dozen transactions. You can try https://xdai-faucet.top/ - if it doesn't work, ask someone for sending $0.1 to your wallet address._

1. Visit circles.garden in Google Chrome, open developer tools with Ctrl+Shift+I
2. Go to Storage/Local Storage/https://circles.garden
3. Copy private key (circles-production-mainnet-privateKey)

![](../assets/gnosis-safe-3.jpeg)

4. Install [Nifty Wallet](https://www.poa.network/for-users/nifty-wallet) or [MetaMask](https://metamask.io/) in Chrome
5. Import Account with copied private key

![](../assets/gnosis-safe-4.jpeg)

Now you have "write-access" and can also send Tokens as the one Owner of the multisig Gnosis Safe is imported to the browser wallet. You can now add new multisig users, but be aware that this might conflict with the original garden wallet.