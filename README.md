# Decentralized-Asset-Registration
This paper composed by the contributers of this repository under the CC0 1.0 Universal license aims to comparing different concepts of decentralized digital asset registration and tracking.

## Table of contents

- [Abstract](#abstract)
- [Introduction](#introduction)
  - [Ownership and Certification Titles for Assets](#ownership-and-certification-titles-for-assets)
  - [Imposed Functional Requirements](#imposed-functional-requirements)
- [Concepts of Decentralized Digital Asset Registration](#concepts-of-decentralized-digital-asset-registration)
  - [Bitcoin Transaction based Token Systems](#bitcoin-transaction-based-token-systems)
  - [Bitcoin Embedded Consensus Systems](#bitcoin-embedded-consensus-systems)
    - [Counterparty](#counterparty)
    - [Omni-Layer](#omni-layer)
  - [Native distributed Asset Issuance Systems](#native-distributed-asset-issuance-systems)
    - [Distributed Asset Issuance Layer Model](#distributed-asset-issuance-layer-model)
    - [Ethereum](#ethereum)
- [Comparison of different Systems](#comparison-of-different-systems)
  - [Comparison Criteria](#comparison-criteria)
  - [Conclusion](#conclusion)
- [Appendix A: Souces](#souces)
- Appendix B: Supply Chains Research

## Abstract

tbd

tbd

tbd

tbd

## Introduction

The products consumed on european and american markets show increasingly global origins. The companies producing, handling and/or distributing those products are spread over the globe. The network these companies form - supply chains - span suppliers, manufacturers and retailers. The degree of optimization they apply to the network - supply chain management - determine their success in their respective industries. (source?)

The global reach of supply chains, specifically into jurisdictions where fair labor and environmental protection are little enforced, creates an often negative ethical footprint for products. (source?) In a movement to more conscious consumption, “There is a growing rallying call by customers and governments demanding more transparency from brands, manufacturers, and producers throughout the supply chain.” ([2](#souces))

For businesses to deliver the demanded transparency, be it out of commitment to values and ethics, or driven by regulations that first world markets increasingly apply, there is a multitude of challenges and problems.(source?) We can agree that effective solutions can only be found by precisely modeling the problem space, which is, among other factors, determined by market composition and degree of integration within the respective industry. Yet, an analysis of a specific industry or market is not scope of this paper. Rather, we want to put the cart before the horse and pick a theoretical problem: the tracking of asset and certification titles along the different parties of a supply chain. With this problem at hand, we will analyse different blockchain based technologies on their ability to deliver the required functionality.

### Ownership and Certification Titles for Assets

A produced physical good - an asset - moves through companies along a supply chain and gets enhanced, combined with other assets, split or modified in another way. To disclose the ethical footprint of this process, the social and environmental conditions of production and modification need to be recorded. Furthermore, the integrity of this recorded information needs to be protected from interests of individual parties that are involved and be accessible further down the chain.
(https://www.zebra.com/content/dam/zebra_new_ia/en-us/solutions-verticals/product/RFID/GENERAL/White%20Papers/WP_Item-Level_Supply_Chain_0413.pdf)

chain of custody
deduct how claims can be aggregated using chain of custody.

certification
deduct how due to a conflict of interests, a third party is required to support claims about quality of asset.

### Imposed Functional Requirements

explain how transformations would be nice to have.

## Concepts of Decentralized Digital Asset Registration

the blockchain has started with bitcoin, digital currency, 7 years ago. the currency has created a big hype, but never reached main market adoption.

http://www.coindesk.com/report-blockchain-could-disrupt-capital-markets-within-decade/

security assumptions -> prove of work / double spend /
([1](#souces))

Over the past three years, investors are turning to Bitcoin’s inherent technology - blockchain - in the attempt to expand it’s functionality beyond tracking of just one specific on-chain asset. 
(Fred Wilson with Union Square Ventures shared his view that blockchain applications are still the biggest opportunities in bitcoin (http://www.coindesk.com/fred-wilson-blockchain-applications-still-biggest-opportunity-bitcoin/))

The intention is to use different methods to either watermark bitcoins, create custom validation rules, or entire new blockchains to represent a sundry of off-chain assets. ([5](#souces))

http://chromaway.com/papers/A-blockchain-based-property-registry.pdf

In the following we will compare bitcoin based systems and then generalize towards custom blockchains.

### Bitcoin Transaction based Token Systems

The seemingly simplest way to issue off-chain assets onto Blockchain is to piggyback on the Bitcoin protocol. 

The Open Asset Protocol is such an implementation that allows to encapsulate a quantity of user-defined asset on top of a Bitcoin amount. ([3](#souces)) "An issuer would first issue colored coins and associate them with a formal or informal promise that he will redeem the coins according to terms he has defined. Colored coins can then be transferred using transactions that preserve the quantity of every asset." ([3](#souces))

![image](http://gendal.files.wordpress.com/2013/11/colored-coin-diagram.jpg?w=600&h=288)

Simple model of a “colored coin.” Source: Richard Brown ([5](#souces))

easy to implement, but no network level verification. ([6](#souces))


at least 3 different companies are utilizing this scheme to create products:

Colu , CoinPrism, and ChromaWay ([7](#souces))

## Bitcoin Embedded Consensus Systems

While in the colored coins architecture bitcoin ownership transfer and colored asset ownership transfer can not be separated ([3](#souces)), Counterparty and OmniLayer have created systems that use Bitcoin as a storage/proof-of-publication layer, while operating and validating a custom protocol on their own nodes.

### Counterparty

Counterparty is one of the examples of an Embedded Consesus System. While having created a new platform for asset issuance, it relies on the security concerns of the Bitcoin blockchain and the inherent computation power of its miners. ([8](#souces))

Counterparty has pioneered the issuance of a native crypto currency (XCP) through “proof of burn”. By sending Bitcoins to an provably invalid address investors could receive an appropriate amount of XCP. XCP is needed to interact with the protocol for issuing new assets. (https://en.wikipedia.org/wiki/Counterparty_(technology))

### Omni-Layer

Omni (formerly Mastercoin) is another example of an Embedded Consesus System, providing complex financial functions on top of the Bitcoin blockchain. Similar to Counterparty it uses Bitcoin as storage/proof-of-publication layer while allowing for custom rules and validation.

![image](https://camo.githubusercontent.com/2aef368d69b82573e5ed61a35ed5700f61a1e4d5/68747470733a2f2f7261772e6769746875622e636f6d2f6d6173746572636f696e2d4d53432f737065632f6d61737465722f696d616765732f6c61796572732e706e67)

source (https://github.com/DavidJohnstonCEO/APIcoin-Spec)

## Native distributed Asset Issuance Systems

describe 
	NXT	?

	bitshares	?

	ethereum

	skuchain	?
		thingchain


### Distributed Asset Issuance Layer Model

“What is the motivation for doing this? Why have these coloring and ECS projects been created? In (Mizrahi 2015), the author notes one alleged advantage of using colored coins via the Bitcoin blockchain: Reduced implementation cost: we only need a thin layer on top of Bitcoin, there is no need to implement a cryptocurrency from scratch. 22 Colored coins, metacoins and other graffiticoins were originally proposed as a “hack” that could rapidly bootstrap by using the Bitcoin blockchain for consensus without building an entire network from the ground up. Since Bitcoin does not natively support the type of asset issuance or financial contracts that are required for financial applications, and because Bitcoin Core is not quickly amendable to such requirements (due to coordination problems discussed in Appendix A), external groups looking to quickly ramp up and use a public blockchain to create an off-chain asset tracking system must implement their protocol on top of the existing network. “ (watermark)

| Protocol Layer  | Functionality |
| ------------- | ------------- |
| Layer 1  | Network  |
| Layer 2  | Consensus  |
| Layer 3  | Transaction  |
| Layer 4  | Quasi Layer for Asset token  |

source ([8](#souces))

### Ethereum

deep dive into ethereum

## Comparison of different Systems

### Comparison Criteria

	http://blog.coinprism.com/comparison-coinprism-counterparty-mastercoin/
	
| Criteria  | | | |
| ------------- | ------------- | ------------- | ------------- |
| Architecture  | Bitcoin based  | Embedded Consensus | Native Asset |
| Protocols  | colored coins  | courterparty, Omni | Ethereum |
| Companies  |   | | |
| Applications | | | |
| Asset divisibility| 0 to 18 places | 0 to 8 places | any |
| Combining asset classes | non trivial | non trivial | yes |

## Conclusion
“The blockchain, in essence, could become the new operating system for Supply Chain Operating Networks — like Descartes, Elemica, GT Nexus, LeanLogistics, and others that combine B2B connectivity with software applications — and also help federate those networks.”
“way ahead of what most companies are willing or ready to implement in the near future.”
http://talkinglogistics.com/2015/01/26/bitcoin-new-supply-chain-operating-system/

## Souces

1. Bitcoin whitepaper https://bitcoin.org/bitcoin.pdf
2. Provenance whitepaper https://medium.com/@provenancehq/using-the-blockchain-to-provide-transparency-in-product-supply-chains-7acf4b8d1d74#.jdmquwhek
3. Open asset specification
https://github.com/OpenAssets/open-assets-protocol/blob/master/specification.mediawiki
4. Ethereum whitepaper https://github.com/ethereum/wiki/wiki/White-Paper
5. Decentralized Digital Asset Registration - Concepts http://gendal.me/2013/11/10/decentralised-digital-asset-registers-concepts/
6. Multichain whitepaper http://www.multichain.com/download/MultiChain-White-Paper.pdf
7. https://www.colu.co/ , https://www.coinprism.com/ , http://chromaway.com/ , http://coinspark.org/ (also offers private blockchains) , BlockCypher
8. Wartermarked tokens http://www.ofnumbers.com/wp-content/uploads/2015/11/Watermarked-tokens-and-pseudonymity-on-public-blockchains-Swanson.pdf


critique assets on blockchain:
	http://www.ofnumbers.com/wp-content/uploads/2015/11/Watermarked-tokens-and-pseudonymity-on-public-blockchains-Swanson.pdf
	http://www.adroitlawyers.com.au/overstock-issuing-stock-taking-asset-securities-distribution-blockchain/
	
## Appendix B: Supply Chains Research

	challenges in supply chain tracking

	Supply Chain Operating Networks




supply chain wording:
	POs
	Invoices
	ASNs
	Payments

	SKU
	Orders
	Lines
	Items
	Subcomponents

	https://spendmatters.com/2015/11/09/why-bitcoins-blockchain-technology-could-revolutionize-supply-chain-transparency/

	3PL
	OEM

	Supply Chain Operating Networks
		- combine EDI (purchase orders and invoices) and software
		- Descartes, Elemica, GT Nexus, LeanLogistics
		- processes are inherent network centric (if execution focused)
		- data quality part of SLA
		=> better analytics / supply chain convergance


