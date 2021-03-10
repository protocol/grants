# Textile Bounties

- $12,500 in prizes + 100% matching from PL
- All awards in FIL

#### **Miner Index Tools and Visualizations**

Textile recently launched the Filecoin Miner Index, the most comprehensive miner storage performance history and real-time index for the Filecoin network. The miner index is an open API that projects can use anywhere on the web. Three endpoints are available, Miner Query, Miner Profile, and Deal Calculator. We're inviting the community to propose, build, and maintain tools on top of the Index.

- **Miner Index Visual Explorer**
  - ($2500 + Protocol Labs matching)
  - The best web-based interface for exploring and using the Miner Index (can be a new integration with an existing project). We want to support all kinds of dashboards, D3 visualizations, and query interface experiments. The API is full of rich data and ready to hack. A winning project will be live online and have a complete user-experience for users to understand and make use of the final product.
- **Best Ethereum-based Oracle built on the Miner Index**
  - ($2000 + Protocol Labs matching)
  - We hope to see the index data making it into other blockchains in the form of oracles. If your project can leverage an oracle with real-time storage pricing data and information to drive miner selection, build the Index's first oracle. A winning project must include an example use of the oracle.

#### **Filecoin Storage Use-cases**

We see so many cool projects join the Filecoin network every week. Still, there is so much more room for innovation. We want to help fund new kinds of projects and data brought to the network. We're focused on three areas of development that we think are particularly well-suited to adopt Filecoin today. We want to see projects that work to store these datasets using online deal storage through [Powergate](https://docs.textile.io/buckets/archiving/), [Lotus](https://docs.filecoin.io/get-started/lotus/installation/), or Textile's [Bucket Archiving API](https://docs.textile.io/powergate/).

- **Best Video App or Platform**
  - ($1500 + Protocol Labs matching)
  - The best innovation or novelty in a video app or platform that uses Filecoin as a primary storage mechanism. The use and storage of videos online are areas with many opportunities to build new solutions for various communities. The benefit of using Filecoin to store those videos is clear. We want to support the continued exploration of these use-cases by funding new projects, platforms, libraries, and standards.
- **Best Collaboration Tool**
  - ($1500 + Protocol Labs matching)
  - The best innovation or novelty in a collaboration or organizational tool that uses Filecoin as a primary storage mechanism. We are excited to see the flourishing of social and collaboration technologies built with Textile. To support this, we want to fund projects that use Filecoin in creative ways to store organization, community, or social data. This could be as simple as embedded Filecoin "drives" into team chat apps or as complicated as wrapping Filecoin storage deals into smart contracts funded by the community.

#### ThreadDB and Buckets

Textile builds a decentralized data synchronization protocol and technology called Threads. Threads allow you to connect multiple databases (or users) and keep data in-sync across Libp2p. Buckets are one of the first applications built on Threads. Buckets provide an easy way to sync folders of data over Libp2p and accessible over IPFS. We provide remote services to host, relay, and persist Threads and Buckets for users.

- **Best App using Threads**
  - ($1500 + Protocol Labs matching)
  - The best application or novel service built on Threads. The community building with threads has snowballed over the past months. We want to support the continued growth by funding projects built on threads or buckets (themselves built on threads) to deliver new consumer applications. Example apps could include new community chat interfaces, database sync tools, and more. Examples services could include: ***Thread Exit Node***s where all updates to a thread are converted to RSS feeds, HTML webpages, JSON endpoints, webhooks, or other formats; Thread Mirrors where registered threads will be persisted on secondary IPFS nodes or in Filecoin deals; Thread Indexes where threads can be registered and discovered by broader communities to join or follow. You can read more about the [architecture here](https://docsend.com/view/gu3ywqi) and the [thread identity and registration here](https://github.com/textileio/go-threads/discussions/483). Help us build the interoperable data future! [Join our slack](https://slack.textile.io/) to learn more about the network and how services can be built.
- **Threads Benchmarks and Metrics**
  - ($1500 + Protocol Labs matching)
  - Best PR or repo that surfaces new benchmarks or metrics for [Threads](https://github.com/textileio/go-threads) or the threads network. A lot of developers ask for better benchmarks, metrics, and performance tooling for using threads. We are looking to support projects that publish [Testground](https://github.com/testground/testground) setups for threads or add OpenTracing or Prometheus to the thread daemon. If this is in your sweet spot, give it a go! A winning project must provide full usage instructions and be possible to regularly use for updated metrics.
- **Best Use of Bucket Pinning API**
  - ($1500 + Protocol Labs matching)
  - The best novel use of the Bucket Pinning API ([Buckets](https://docs.textile.io/buckets/) plus the [Pinning API Spec](https://github.com/ipfs/pinning-services-api-spec)). We have just released a novel pinning API built on buckets. This allows groups to sync pin sets, collaborate on shared pin sets, and mirror pin sets across multiple services or servers with ease. Because the full Bucket API backs each pinning API endpoint, you can do a lot more than pin here. That includes the ability to use the `bucket archive` API endpoint to snapshot buckets to Filecoin easily. Show us what you've got. Learn more about the experimental [bucket pinning API here](https://github.com/textileio/textile/discussions/499).


#### Community Enablers

- **React Boilerplates for Buckets and Filecoin APIs**
  - ($500 + PL matching)
  - Best React boilerplates to help projects build with Textile Buckets and Filecoin APIs (including the miner index). Make it easy to start up new projects that leverage threads (sync), buckets (object storage), and Filecoin (persistence) with Ethereum smart contracts or Metamask.
  