

## About Metronome

**What is Metronome?**

Metronome ("Metronome" or "MTN") is the world's first cross-blockchain cryptocurrency. It is designed to bring institutional-class endurance to the cryptocurrency category through:

*   **Self-governance** - MTN is designed to function indefinitely and without management by a group or individual, even its authors.
*   **Reliability** - The system is architected for steady and predictable token supply with descending price auctions.
*   **Portability** - With the ability to move between blockchains, the cryptocurrency is further protected from management issues and instability.

<a>What can Metronome do that other cryptocurrencies cannot do?</a>



We expect that MTN will act as a store of value that is decentralized across blockchains. Since MTN can be exported and imported across chains, it empowers users to move MTN for whatever reason they desire. Other cryptocurrencies cannot do this.

Cross-chain export and import of MTN provides the ability to emigrate from one blockchain to another in the event of a failure.

MTN also allows for subscriptions, or recurring payments on the blockchain that are automatic. This is something cryptocurrencies have struggled with, until now—MTN users can schedule repeat payments easily.


**What can Metronome be used for?**

While many different communities and institutions will discover their own use for Metronome, it was designed for any scenario where reliability is a first-order variable for selecting a cryptocurrency.

Some possible use cases include, but are not limited to:

*   Decentralized store of value across blockchains
*   Advanced payment settlement:
    *   Mass Pay — allowing users to send tokens to multiple addresses with one action. While mass pay is a well-known and used feature on the Bitcoin network, it is lacking on the Ethereum network.
    *   Subscriptions — allowing users to set up recurring payments between themselves and other parties. Subscription is a payment feature unique to Metronome. Users can set up recurring payments between themselves and other parties by authorizing that party to take a certain amount of MTN from a wallet on a recurring, periodic basis.

A unique Metronome payments feature is subscription. Users can set up recurring payments between themselves and other parties by authorizing that party to take a certain amount from a wallet on a weekly basis.


**Where can I read the full Metronome Owner's Manual?**

The owner's manual is available [here](https://www.metronome.io/pdf/owners_manual.pdf).


**How will Metronome be launched?**

There will be two phases, both of which will rely on the [descending price auction](http://www.sciencedirect.com/science/article/pii/S0899825608000869) ("DPA") pricing mechanism:

*   **The initial supply auction**, serving as the official launch of Metronome, where 10,000,000 MTN tokens will be issued and made available
*   **The daily supply auction**, where new tokens are added to the auction ad infinitum, at the rate that is the greater of (i) 2,880 MTN per day, or (ii) an annual rate equal to 2.0000% of the then-outstanding supply per year.


## Initial and Daily Supply Auctions

**How will the Metronome token sale take place?**


The initial supply auction serves as the official launch of Metronome. 8,000,000 MTN tokens (10 million, less the 20% one-time author retention) will be made available to the public with a descending price auction. The price per MTN will begin at a maximum price of 2 ETH per MTN, with a floor price of 0.0000033 ETH. As time progresses and MTN remains available, the auction price will decline linearly until the auction ends or all MTN are sold. Metronome employs DPAs to establish predictable and transparent pricing for the MTN being issued by the contract.

**When will the Metronome initial supply auction start?**

The initial supply auction is targeted to launch on February 5th, 2018. Once started, it will last up to 7 days or until all MTN in the initial supply are sold as described above.

**How do I participate in Metronome's initial auction?**

To participate in Metronome's initial supply auction (and, every day thereafter, the daily supply lot) you will need access to an ERC20-compatible Ethereum wallet where you hold the private keys and sufficient ETH to purchase MTN. **Do not use wallets provided by exchanges.** Be sure to use enough [gas](https://themerkle.com/why-does-the-ethereum-ecosystem-use-gas/) when sending your ETH. If you do not use enough gas, your transaction will be rejected and you will have to send your ETH again.

Ethereum can be purchased from cryptocurrency exchanges. Again, make sure that once you purchase your ETH, you transfer it into an ERC20-compatible Ethereum wallet where you hold the private keys.

Once you have sufficient ETH in an ERC20-compatible Ethereum wallet, you may participate in the auction by sending the desired amount to:

****contract address TBD****

You should receive your MTN almost instantly following that; there is no need to wait until the end of the auction for disbursement.


**Is there a minimum or maximum number of MTN tokens I can buy during the initial auction?**

No, but each purchaser is limited to purchasing 1,000 ETH per transaction for Daily Supply Lots.


**How does new Metronome enter the ecosystem?**

Following the initial auction, MTN is added to MTN’s daily supply lot (“DSL”) every 24 hours, at the rate that is the greater of (i) 2,880 MTN per day, or (ii) an annual rate equal to 2.0000% of the then-outstanding supply per year. Newly-minted MTN from the DSL enters the ecosystem via a DPA. All tokens in the DSL start at a maximum price set by the contract at the previous auction’s minimum price multiplied by two. Every 60 seconds, the price of remaining MTN is reduced to 99% of its previous price. After some time, we expect the price of remaining tokens will become low enough for the DSL to sell out.

In the event that there are unsold MTN at the end of the daily auction, those tokens will be held over and added to the next DSL. For example, if 1,000 MTN went unsold, the next DSL would introduce the scheduled 2,880 MTN along with the remaining 1,000 MTN from the previous day.

We expect that the mintage rate for approximately the first 40 years will be 2,880 MTN per day. After approximately 40 years, the mintage rate will be higher as shown below.

| Time | Circulating MTN (End of Year) | Mintage rate (End of Year) | Daily supply lot |
| ------------ | -----------: | ------: | ------: |
| T + 1 Year   | 11,051,200   | 10.512% | 2,880   |
| T + 5 Years  | 15,258,880   | 7.399%  | 2,880   |
| T + 10 Years | 20,517,760   | 5.400%  | 2,880   |
| T + 40 Years | 52,076,800   | 2.066%  | 2,880   |
| T + 70 Years | 94,382,561   | 2.000%  | 5,070   |


**How soon will the daily auctions begin once the initial supply auction finishes?**

The first DSL will take place the following midnight UTC after the close of the initial auction.


**Who gets the proceeds of the MTN auctions?**

100% of the proceeds of the initial token sale and 100% of the future daily supply lot proceeds go to MTN’s Autonomous Proceeds Provider (“APP”) contracts – the Proceeds and Autonomous Converter Contracts – to provide long term liquidity and price support. Metronome authors receive none of the proceeds from any auction.

**What prevents a large hash-power miner (or pool of miners) from dominating purchases?**

Anyone can potentially soak up new supply, simply buying early and therefore paying more. That is how descending price auctions make the process predictable and the reason why we are using them.

Miners can potentially front-run a non-miner transaction—but they must also (a) pay more, otherwise their actions have no impact on the auction, and (b) win a block, which is unlikely unless they are extremely large pools.


## How Metronome Works

**What components make up Metronome?**

Metronome is comprised of four fully-autonomous and cooperative smart contracts.

*   Metronome Ledger ERC20
    *   This is the token’s smart contract ledger and dictates how the token behaves
*   Auctions Contract
    *   This smart contract interacts with the ledger contract above and operates as a descending price auction
    *   Sets the rules for the initial supply auction and the daily supply lot
    *   Sends ETH from the Auctions Contract to the Proceeds Contract
*   Autonomous Proceeds Provider (two contracts)
    *   Automatically provides liquidity between MTN and ETH
    *   Comprised of two smart contracts
        *   Proceeds Contract
            *   Supports liquidity by holding 100% of the DSL and transferring 0.25% of the total accumulated balance to Autonomous Converter Contract every day
        *   Autonomous Converter Contract
            *   Provides price support and liquidity
            *   Allows MTN and ETH to be interchangeable


**What blockchains are MTN compatible with?**

Metronome will be initially issued on Ethereum with Ethereum Classic, Rootstock, and Qtum support expected to follow. As the community continues developing MTN, it may be compatible with even more blockchains.


**Has the smart contract that collects ETH been professionally audited for security issues?**

The smart contract has been audited by three independent consultants: Zeppelin Solutions, Martin Swende, and Gustav Simonsson.


**What risks are involved with MTN?**

Though the Metronome code has been thoroughly audited by multiple independent parties, there are always some potential risks, as with any cryptocurrency. These potential risks include, among other risks:

*   Chain dependence (e.g., chain mutability or chain denial of service): as the first cross-chain cryptocurrency, Metronome was built to help mitigate this issue.
*   Immutable bugs: Though the code has been thoroughly audited by independent parties, there is always this possibility that a bug may be immutable or need to be worked around.
*   Contract attacks: Two categories of contract attacks are: (1) technical, which exploit some attribute of the contract's bytecode-defined EVM behavior and (2) economic, where attacks induce unintended behavior from the contract functioning as designed.


## Metronome and Bloq

**Who is Bloq?**

Bloq was launched with a vision to help companies meet a very new challenge: integrating into a world of multiple blockchains, culminating in an "Internet of blockchains."

Led by a world-class team of blockchain developers, entrepreneurs, and investors, we have developed BloqEnterprise, an open source blockchain technology that helps businesses develop blockchain-enabled solutions to address some of the biggest issues businesses are facing today.

Since Bloq's inception, we've also advised on some of the the biggest projects in this space, while sponsoring open-source developers whose passions, interests, and skills aligned with ours.

To bring the latter into operational focus, we started BloqLabs earlier this year to help accelerate our efforts in this area. This has been an essential part of our strategy to expand the surface area between blockchains and boardrooms, open-source and office suites.

We anticipate that BloqLabs will produce a number of innovations to be presented under the "Built by Bloq" brand, one such innovations being Metronome, which aims to realize the promise (and unlock the potential) of a multi-blockchain world.


**Why did Bloq create Metronome?**

We looked at the current landscape of distributed blockchain-based financial products and saw a novel opportunity to launch a cryptocurrency with equal public access and the need for a cross-chain solution. Metronome is a truly self-governed cryptocurrency that we believe is reliable, equally accessible to the public, and immune to community or individual drama.


**Why is the token called "Metronome"?**

We believe the cryptocurrency's supply and issuance is predictable and constant. Our innovation needed a name that carried the same weight as its performance. The enduring beat of tokens being added to the ecosystem per day is unending and reliable, like a musical metronome that maintains a consistent cadence.


**Will there be a lock-up in tokens retained by Bloq?**

Bloq and Metronome's authors will receive 20% of the initial MTN supply as a one-time author’s retention. 25% of this will be available upon the closing of the initial supply auction. The remaining 75% is released quarterly over 12 quarters.

100% of ETH proceeds from the auction will remain in the Metronome ecosystem. Bloq can buy and sell its own MTN at its discretion.  Following the launch of the initial auction, the Metronome ecosystem is entirely in the hands of the smart contracts and the community.

By accepting the author's retention in MTN, Bloq has an incentive to remain active with the ecosystem community.


**Will Bloq govern MTN?**

No. Metronome will be governed by its smart contracts and users. Bloq plans on remaining active within the community of users and developers by continuing to grow the ecosystem with MTN-enabled and compatible products. However, after its launch, Bloq will have no more control over MTN than any other member of the MTN community.








