---
title: Update #14 - More Information on Suspected Lubian.com Hack
category: 陈志太子比特币事件
---
# Update #14 - More Information on Suspected Lubian.com Hack

**Christian Reitter**  
Published: Aug 4, 2025

Our research update#7 from April 2024 first reported on a “billion dollar range” of weak wallets which previously held huge amounts of Bitcoins, and had all of their funds suddenly withdrawn in December 2020. Based on significant Bitcoin mining activity, we associated them with lubian.com as the former owner. In light of recent media coverage of this topic, here is some new research information on this wallet cluster, and what may have happened to it.

## Table of Contents

- Billion Dollar Wallets
- Recent News
- New Research Breakthrough
- New Wallet List
- Transaction Volume
- Curious On-Chain Notes
- More Data for Researchers, Note

## Billion Dollar Wallets

### Recent News

On Saturday, August 2, 2025, the Twitter (X) account of Arkham Intelligence posted a widely seen thread outlining the lubian.com-related weak wallets and corresponding wallet movements. They directly cited the Milk Sad research from last year through screenshots.

My previous list of related victim wallet addresses from weak private keys is composed of 8 addresses with major transaction histories, plus one (`35v6FmTJSChgwcH6tgAwCwsEj315bvq3tB`) which was older, but similar enough to include in the first list.

Through new research conducted over the last months, I’ve now found about 20 additional wallet private keys that were previously hidden. This new information gives a more complete view into what appears to be a massive trove of weakly secured Bitcoins that were controlled by a major entity, and then likely stolen on 2020-12-28 by an actor who found out about the weak private keys.

## New Research Breakthrough

Please see the research update#7 for an overview on the specific mechanisms, wallet types and Pseudo Random Number Generator (PRNG) configurations that describe how the weak wallet private keys were created and doomed from the start. That blogpost also outlines the connections to Bitcoin mining and lubian.com, as well as the different sources of funds.

From a research point of view, the essential new discovery is the use of PRNG offsets by the vulnerable software which created the weak wallets, like I described in the recent research update#13 for an unrelated cluster of weak wallets. This explains how I didn’t find all of them in my previous searches, and helps to further establish direct connections between seemingly separate wallets through shared PRNG states. I think we’re the first to publish about this as well, and want to thank a fellow white hat security researcher who gave us a hint about the new search pattern.

## New Wallet List

Here is a new list of weak wallets that were likely controlled by the actor behind lubian.com:

| PRNG index group | PRNG offset | Primary Wallet Address                     | Comments                              |
|------------------|-------------|--------------------------------------------|---------------------------------------|
| A                | 0           | 338uPVW8drux5gSemDS4gFLSGrSfAiEvpX        |                                       |
| A                | 32          | 3GaB3nRWA1PLc3XQkkbpVtFwYYZEuMxD4i        |                                       |
| A                | 64          | 3AWpzKtkHfWsiv9RGXKA3Z8951LefsUGXQ        |                                       |
| A                | 96          | 3NmHmQte2rP8pS54U3B8LPYQKkpG1pFF69        |                                       |
| A                | 128         | 3FrM1He2ZDbsSKmYpEZQNGjFTLMgCZZkaf        |                                       |
| B                | 0           | 32vpyd3jos4mEe8CmBnreRRXJJnwLMF3Gn        |                                       |
| C                | 0           | 34Jpa4Eu3ApoPVUKNTN2WeuXVVq1jzxgPi        |                                       |
| C                | 32          | 3KabDvdetZXDHNm9HXowLc9SppiSXKn7UU        |                                       |
| C                | 64          | 3LjTXe31gepN8nW3AZyKpyD2QwbtmfjNwm        |                                       |
| C                | 96          | 38Md7BghVmV7XUUT1Vt9CvVcc5ssMD6ojt        |                                       |
| C                | 128         | 3BA3PEF4BMoy9y3kdMRUdMhL8Gp24vikhF        |                                       |
| D                | 0           | 36UNrMNN3xk1dTfqCWAPmrfBXA2gykCPBK        |                                       |
| D                | 0           | 3Jx6enuiaBi1tk1KJsx6LzAeVgiMcjx7NZ        | m/49'/0'/0'/1/0 derivation, first use in 2024 !? |
| E                | 0           | 3Pja5FPK1wFB9LkWWJai8XYL1qjbqqT9Ye        |                                       |
| F                | 0           | 3JJ8b7voMPSPChHazdHkrZMqxC7Cb4vNk2        |                                       |
| F                | 32          | 33uEsaGLcF9H46Dvzx1kMnuMCQ13ndkAjV        |                                       |
| F                | 64          | 32i6n2vXhjvJg1vniURFy7A5VK6eG6oDgg        |                                       |
| F                | 96          | 3B1u4PsuFzww1P8if5jYmitXxpMs2EMSqt        |                                       |
| G                | 32          | 3PQzDoiwW7pYh49MotPrVcsydQCq5ES1Bz        |                                       |
| H                | 0           | 3PWNGS2357TnjRX7FpewqR3e3qsWwpFrJH        |                                       |
| H                | 32          | 3HuUiXmKN3beQSoM97kWjK1fesWWJvKvaZ        |                                       |
| H                | 64          | 34KYo7VdVr5CJ7m4hYhH9RpwqXhbsTrw4T        |                                       |
| H                | 96          | 339khCuymVi4FKbW9hCHkH3CQwdopXiTvA        |                                       |
| H                | 128         | 389JrNcn8trYgYi2EtHi4X7bTCqtVbep86        |                                       |
| I                | 0           | 3J4sTPyD1g6KvNUSJxjwLs4iaPeDPqxUZr        |                                       |
| I                | 32          | 34MFtk9iMxYcUPZWXHfiGfqz4o7X3kpJbV        |                                       |
| I                | 64          | 3MHa8JJ3bu8j3x3iQHhqsrZvk1EjBQmC78        |                                       |
| I                | 96          | 3DdFSGcXaP2rZ9CaL3tjnqRARvQ5K3VW4a        |                                       |
| I                | 128         | 39B6oSa58qNpFMGpuowtRHAYp3fM4ghXRq        |                                       |

*Technical notes (click to unfold)*

## Transaction Volume

There were around **136,951 BTC** (Bitcoin) in all weak wallets of this PRNG range as of transaction `8b9de493..08f4a4c2`. With transaction `95384d1c..8617c9e2`, a massive withdrawal run started and continued for about two hours until `14bb56a2..07983bcd`, with the overall balance down to about **193 BTC**. In the days after, the balance went down further to about **4 BTC**.

Based on the estimated USD value of Bitcoins at the time of each withdrawal, this combines to an approximated **$3.7 billion** moved on **2020-12-28**.

As Arkham Intelligence noted in their tweets, not all of the funds moved that day went to the (likely) attacker. For example, a sizeable chunk of around **9,500 BTC** went to `3HRzRMNbcHR5PTfAzt5Lo7AHgT3oUhq9zG`, which lubian.com continued to use as a Bitcoin payout address. Overall, I currently suspect that about **$3.44 billion** went to the attacker, which is still an absolutely insane figure 🤯.

Note the use of a fixed transaction fee of exactly **75,000 sats** for many of the suspicious transactions, which is unusual.

## Curious On-Chain Notes

Many of the previously listed Bitcoin victim wallet addresses have some interesting outgoing transactions on **2022-07-03** and **2024-07-25**, which is a long time after the (likely) theft on **2020-12-28**. Similar messages were apparently sent to the (suspected) attacker addresses. The purpose of those transactions appears to be a public broadcast message of some sort. The transactions include two short message snippets via the `OP_RETURN` Bitcoin mechanism, which combine to:

> MSG from LB. To the whitehat who is saving our asset, you can contact us through 1228btc@gmail.com to discuss the return of asset and your reward.

I suspect that “LB” refers to lubian.com, and that “saving our asset” alludes to the huge withdrawal of funds from the weak addresses on 2020-12-28.

The messages are visible in blockchain explorers which show `OP_RETURN` information. Identical messages were sent multiple times to different addresses in the cluster. Here are two examples: [first message](#), [second message](#). Notably, the second part of the message wasn’t mentioned in the screenshots of Arkham Intelligence yet.

Please keep in mind that since the underlying wallet private keys are compromised, basically anyone can both send and withdraw funds to and from these wallet addresses while attaching arbitrary messages. Wallet addresses with a history of large balances also frequently get some form of odd broadcast messages sent to them, for example [here](#) (`640ebe62..b5caac0c`) with words encoded in bogus receiver addresses. To make informed guesses about whether the previously cited "MSG from LB" is a misleading scam/prank or a real (and late!) attempt by the lubian.com actor to get their funds back, I recommend looking into the origin of the Bitcoins that were used for this and drawing your own conclusions.

## More Data for Researchers, Note

There is a research data repository with more weak addresses in this range and other data.

A quick reminder: we have no involvement with the funds’ former and current owners or any withdrawal of funds in this range. The Bitcoins in question were moved years before we as the Milk Sad team discovered it, or reported about it. As researchers, we’re mainly trying to shine a light at what happened, hoping to help avoid future disasters through more public awareness of the dangerous software flaws that caused them.