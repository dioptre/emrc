# Global human health database

## Resources
* Homepage [medgraph.io](medgraph.io)
* [Top Level Architecture](https://www.draw.io/#G1lAaM-LQrw81S_t7lRKxwoz7YMOKBchuf)

## Why
* I met with the national director of health for a smaller country who mentioned their medical record system was in disarray, and needed a decentralized and methodical way to obfuscate and share patient data.
* I have a friend who is a doctor who mentioned our medical records didn't belong to us.
* I want to pass my medical data to science or my future kids like I do my organs when I die.
* I ran out of research data for my implementation of an EEG classifier. We need to share more data. Universities are actually horrible at this.
* Alternatives are slim. Google made baselayer, but there's no code and no data. Very Google. The collaborations with universities aren't public.
* No single component exists today that works out of the box.
* There's a lot of hype around bitcoin blockchain and coins. The idea is well suited to be taken up and implemented only now.
* I reverse engineered the BTC protocol for fun from the stream up without docs 5 years ago, so maybe I should put some knowledge to some good use instead of all the @#$$ that's floating around.
* **Cheaper to save lives. If we get more data, health providers will get cheaper and provide better services.**

## Requirements
1. Need a method to exchange health data
2. Counterparties should be known or a proxy representative
3. No "private" data should be public even if it's encrypted. (Why? Look into elliptical cryptography, NSA, quantum computing)
4. "Public" data should be difficult to determine the owner. Searchable, and usable for research publicly.
5. People should be paid to store the data. They can choose to store it with a trusted 3rd party or directly for a health insurer/provider.
6. Should be easy for existing products and services to interoperate with it.

## How
Loosely thinking something like:
* Corda (mitigates public risk, and provides counterparty solution - notaries are redundant so can be removed but need to keep in mind BFT https://en.wikipedia.org/wiki/Byzantine_fault_tolerance)
* IPFS (global storage - clusters available, but independent trusted counterparty stroage is required)
* Filecoin (storage should be paid for, not sure of the implementation or the legitimacy of the whitepapers https://filecoin.io/proof-of-replication.pdf - but the idea behind it is good - again needs to be separated into trusted/firewalled clusters) https://filecoin.io/filecoin.pdf
* Alt Payment system - could be something like Filecoin, could be a sidechain on the lightning network with takebacks for unfulfilled promises - sidechains could be implemented with shared addresses (shared public keys across coins) http://lightning.network/lightning-network-paper.pdf http://www.ieee-security.org/TC/SP2015/papers-archived/6949a104.pdf
* User data could be indexed via addresses  - and a single user could have multiple addresses based on data types to be stored.
* OpenEMR for health records (need something more interesting to include research data)
* Trafodion/GunDB for public data
* Elastic for search

## Contributors

Email me and let's do this.

## Future considerations
* Search records
* Political sensitive data
* Truly private internet

## Reading
* [Andy's research on pocket](http://sharedli.st/dioptre#)


