# Overview

Kaspa is a proof of work consensus stack, designed to address what we believe to be leading challenges for the second decade of crypto. As the technology matures and its adoption and integration with other web applications gain momentum, we identify two primary vectors which require a deep revisit of the base consensus: the speed of transaction-inclusion in the ledger, and the control over transaction-ordering in the ledger.

We postulate that instant time-to-inclusion (a.k.a. first confirmation) in the ledger is of primary importance to user- and developer-experience, and to integration with other web applications, as well as fast (probabilistic) finality. Kaspa optimizes for minimizing the latency imposed by the consensus engine on transaction flow and user experience. Additionally, we contend that the ability of peripheral nodes that control a small fraction of the hashrate to mine blocks very frequently, in an asynchronous fashion, is key to mitigating serious “flashbots” and MEV threats referring to the ability of miners, and of trading bots, to manipulate transaction ordering and gain an unfair and occasionally undetected advantage over ordinary users. Sub-second block times enable pre-trade privacy, and pre-trade stealth transactions, to protect the users from such manipulations. Kaspa’s current testnet operates with 1 block per second. Down the road, core developers and researchers will work on stretching the capability to the limits—think 10 or even 100 blocks per second (enabling a miner of 1% of the hashrate to mine on average 1 block every second!). 

Providing instant confirmation is a trivial task, if willing to compromise on the principles of decentralization, or to operate under strong assumptions on the network’s topology and with minimal safety margins. Kaspa took the hard path of designing the system based off Satoshi’s paradigm and first principles. There has yet to be, in the blooming field of cryptocurrencies, a serious attempt at following Satosh’s v1 protocol, and proving and providing new capabilities based yet on the same fundamentals. While Bitcoin is becoming the Internet’s ultimate reserve asset, we believe there is still demand—and an urgent one, at that—for an implementation of Satosi’s original vision: a peer-to-peer electronic cash system.

Since transaction ordering is the main challenge of any consensus protocol, Kaspa’s base layer focuses on becoming a fast and scalable transaction ordering and data availability (a.k.a. proof-of-publication) engine. The base consensus will therefore maintain the state of payments only (aka the UTXO set), whereas computing the more general and expressive state will be outsourced to Layer Two operations. This should be done by adopting the thought process and innovation led by several Ethereum researchers and developers who are building rollups. The rollups technology reduces the cost of running base consensus nodes by decoupling computation from data availability. 

In fact, a rollups-centric Ethereum will fragment the network, hinder composability, and dramatically change the underlying assumptions and dynamics. Smooth operation between the siloed rollups will require special liquidity providers that serve the purpose of bridging the gap—specifically, providing instant confirmation to circumvent the prohibitive finality periods required for securing optimistic rollups. Providing these rollups with a shared scalable data availability layer, allowing shorter finality times, enabling stealth pre-trade transactions which protect against censoring miners, and bootstrapping an ecosystem of cross-silo communication, is another natural way in which Kaspa network aims to solve a timely pain point for crypto projects and users.