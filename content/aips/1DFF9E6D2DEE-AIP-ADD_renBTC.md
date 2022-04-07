---
title: Add renBTC to Aave
status: WIP
author: Wesmultisig
shortDescription: Add renBTC support to Aave Markets
discussions: https://governance.aave.com/t/arc-proposal-to-add-support-for-renbtc/568
created: 2022-03-28
---

## Simple Summary

Add depositing, borrowing and collateral support for renBTC to the Aave market. renBTC is a 1 to 1 representation of Bitcoin using Ren Protocol.

## Abstract

This proposal presents the adding depositing, borrowing and collateral support of renBTC to the Aave market. 

## Motivation

Ren Protocol (https://mainnet.renproject.io/) has bridged 308,944 Bitcoin, 648 million Doge, 2.5 million Luna, 134,717 Zec, 89million Dgb, and 430,000 Fil between supported chains without any hacks or incidents. Aave currently only supports renFIL. It seems logical that Aave would want to add support for different types of ‘wrapped’ Bitcoin on its platform. Adding renBTC will pave the way for the Aave community to consider more renAssets to its platform. RenBTC has been available on competing platforms such as MakerDao and had 0 votes against its adoption; current stats are found here: https://makerburn.com/#/collateral/renbtc

Benefits of adding support for renBTC:
- Diversification of BTC options to users
- Increased Aave usage by renBTC users
- Assuming renBTC is added and subsequently renJS, renBTC users will be able to:
  - deposit/Lend BTC into Aave with a single btc transaction.
  - payoff/withdraw real BTC in a single ethereum transaction. An example of renJS can be found here: https://varenx.com/swap 
    
## Specification

What is the link between the author of the AIP and the Asset? ​ Wesmultisig has been a member of the Ren community for years and is now a member of the Ren Community Ecosystem Fund Multi-Sig.

Provide a brief high-level overview of the project and the token ​ Ren Protocol (https://renproject.io/) developed and launched RenVM, “a byzantine fault-tolerant protocol that provides ECDSA threshold key generation and signing via sMPC”(https://governance.aave.com/t/arc-proposal-to-add-support-for-renbtc/568). What makes RenVM unique is that it does all key management and rotation using its sMPC based protocol that the team has pioneered. The state, inputs, and outputs of all programs that RenVM runs (e.g. ECDSA private keys) are kept hidden from everyone, including the Darknodes (https://docs.renproject.io/darknodes/) that power it. This allows RenVM to securely manage (ECDSA) private keys of different assets, making it possible to mint or burn tokenized representations of these assets on external blockchains in a trustless, permissionless, and decentralized manner. One of the core features of RenVM is bringing BTC to Ethereum (i.e renBTC). RenBTC serves as collateral within the Aave ecosystem and is the sole focus of this application. ​
Explain positioning of token in the AAVE ecosystem. Why would it be a good borrow or collateral asset? ​ The REN token and renFIL are already supported in the Aave market. RenBTC is one of the most popular cross-chain tokens today; renAssets total around 1.1 Billion and the network has processed over 10 Billion USD worth of volume. Adding renAssets gives Aave more diverse 'Wrapped BTC' offerings and the UI advantage to maintain its competitive edge in its addressable market. ​
Provide a brief history of the project and the different components: DAO (is it live?), products (are they live?). How did it overcome some of the challenges it faced? ​ RenVM has been in development since 2017, is in a transition phase to a DAO (https://medium.com/renproject/renvm-mainnet-release-plan-761f1c2c0752), and is live on Mainnet. ​

## Rationale

The REN token and renFIL are already supported in the Aave market. RenBTC is one of the most popular cross-chain tokens today; renAssets total around 1.1 Billion as of today. Adding renAssets gives Aave the UI advantage to maintain its competitive edge in its addressable market. 

## Test Cases

Audits/Security Reviews: https://github.com/renproject/ren/wiki/Audits
RenBTC Technical Assessment: https://forum.makerdao.com/t/renbtc-erc20-token-smart-contract-technical-assessment/5341

## Implementation

A BTC/USD feed can be used; ETH mainnet (https://data.chain.link/ethereum/mainnet/crypto-usd/btc-usd), polygon found here (https://data.chain.link/polygon/mainnet/crypto-usd/btc-usd).

The following strategy parameters are proposed (same as wbtc..where can I see this info?). 


## References

- ARC: https://governance.aave.com/t/arc-proposal-to-add-support-for-renbtc/568
- Website: https://mainnet.renproject.io/
- Wrapped BTC Data: https://dune.xyz/eliasimos/btc-on-ethereum_1
- renBTC Token contract: https://etherscan.io/token/0xeb4c2781e4eba804ce9a9803c67d0893436bb27d
- Makerdao renBTC Vault: https://oasis.app/vaults/open/RENBTC-A
- renBTC stats on Makerdao: https://makerburn.com/#/collateral/renbtc
- renJS docs: https://github.com/renproject/ren-js
- renWiki: https://github.com/renproject/ren/wiki
- Audits: https://github.com/renproject/ren/wiki/Audits
- renBTC Technical Assessment: https://forum.makerdao.com/t/renbtc-erc20-token-smart-contract-technical-assessment/5341

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
