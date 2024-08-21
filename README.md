# PKT Migration Signer

This tool will allow you to claim your airdrop of new PKT using the private key from your legacy PKT wallet.

This app is available for Windows, Mac (Intel and Apple), and Linux amd64.

To use the app, first you must extract the private key from your PKT wallet, a private key looks like this: `cQfM2mV4TvtUQe1UyT2CxEXAMPLExDOxNOTxUSExRENk6AbBeyGAd`, and there is one private key for each PKT wallet address.

## Getting a private key from an Electrum wallet
![getting a private key from electrum](https://github.com/pkt-cash/PKT-Migration-Signer/blob/main/images/get_private_key.png?raw=true)

Once you have your private key extracted, you must then install a Web3 wallet such as
[Coinbase](https://www.coinbase.com/wallet) or [MetaMask](https://metamask.io/).
After setting up your Web3 wallet, you will have an Ethereum style address, it will look something like this `0xd83969cxEXAMPLExDOxNOTxUSEx14553F3cae6C3`. This address will be the *destination* where your PKT will be paid
out to.

## Create your Migration Code
Download the appropriate executable for your platform. 

* [Windows](https://github.com/pkt-cash/PKT-Migration-Signer/raw/main/downloads/PKT-Migration-Signer_windows_amd64.exe)
* [Mac Intel](https://github.com/pkt-cash/PKT-Migration-Signer/raw/main/downloads/PKT-Migration-Signer_mac_amd64.tar.bz2)
* [Mac Apple Silicon](https://github.com/pkt-cash/PKT-Migration-Signer/raw/main/downloads/PKT-Migration-Signer_mac_aarch64.tar.bz2)
* [Linux (amd64)](https://github.com/pkt-cash/PKT-Migration-Signer/raw/main/downloads/PKT-Migration-Signer_linux_amd64.tar.bz2)

On Apple, first double click on the .tar.bz2 file that is downloaded, and a new file called
`PKT-Migration-Signer_mac_<something>` will be created. Right click (2 finger click) on that icon
and then select "Open" to launch the app.
There will be a terminal window while the app is running, this is normal.

![open the migration app](https://github.com/pkt-cash/PKT-Migration-Signer/blob/main/images/migration_1.png?raw=true)

Paste your private key, and your Ethereum address to receive your migration link.

![paste your information to get the link](https://github.com/pkt-cash/PKT-Migration-Signer/blob/main/images/migration_2.png?raw=true)

## You need ETH on the Base chain to transact
In order to perform any transactions at all, including claiming your airdrop, you need Ethereum to pay the gas fees.
You can purchase ETH inside of the MetaMask or the Coinbase wallets.

**IMPORTANT**: Make sure you have switched your wallet to the `Base Mainnet` network before purchasing. When you buy,
double-check that you are receiving ETH on the Base Mainnet.

![buying ethereum](https://github.com/pkt-cash/PKT-Migration-Signer/blob/main/images/buy_eth.png?raw=true)

## Claim your airdrop
With ETH in your wallet, you will be able to follow the migration link and execute the contract to receive your airdrop.

## Trivia
* You will receive 1/3 of your migration on day 1, 1/3 Feb 19, 2025, and 1/3 on Aug 20, 2025.
* To keep amounts simple and readable, the amount you receive will be exactly 1/3 of your balance rounded to the nearest hundredth of 1 PKT. If you started with 1000 PKT, you will receive 999.99 in three batches of 333.33.
* The signature that you are creating with your (Bitcoin-style) private key is transmuted into an Ethereum style
signature which can be checked by the smart contract using Solidity code.