# RFPs for IPFS and Filecoin from Protocol Labs

**Protocol Labs is seeking grant proposals for the following RFPs for IPFS, Filecoin and libp2p.**

&nbsp;

#### How to Apply

[Open an issue](https://github.com/protocol/grants/issues/new?assignees=eshon&labels=&template=rfp-proposal.md&title=%3CYour+Project+Title%3E) with your proposal, following the RFP template.

*For questions about RFPs or to submit proposals via email, contact **dev-grants@protocol.ai***

-----

## *RFPs*

- [Improved Garbage Collection in IPFS](#improved-garbage-collection-in-ipfs)
- [S3 Interface to Filecoin and IPFS](#s3-interface-to-filecoin-and-ipfs)
- [Filecoin PubSub Observatory](#filecoin-pubsub-observatory)
- [Better go-ipfs Observability](#better-go-ipfs-observability)

&nbsp;

### Improved Garbage Collection in IPFS

#### Overview

Improve the performance characteristics of garbage collection of unpinned content in IPFS and support the removal of specific content. Flexibility in supporting various GC strategies would be ideal.

#### Description

When storage is reclaimed by removing unpinned blocks, garbage collection in IPFS currently requires stopping other node activities for its duration, and can take significant time. For pinning providers with pins at scale, this can take “literally days” for a single node. Large pin sets can become expensive in both memory and time. Garbage collection needs to operate differently to reduce the impact on IPFS.

An additional request from users is to be able to remove specific content (e.g. spam) from an IPFS node. Currently, GC removes all unpinned blocks. It would be useful for GC to be able to remove all blocks associated with a specific DAG along with upgrades to reference counting.

As a result of this project, these specific pain-points will be resolved:

- GC content when it becomes unpinned
- GC specific content
- GC takes too long for nodes with large pin sets

This project has been technically scoped. To learn more about the proposed approach [see the full proposal](https://github.com/protocol/web3-dev-team/blob/771c5a1d51ceef5ffd9e1d5303fd0a9617cd41c0/proposals/new-ipfs-gc.md) as well as [PR conversation](https://github.com/protocol/web3-dev-team/pull/8).

### Effort estimate
1-2 people, 4-6 weeks

### Skills needed
go-ipfs expertise

&nbsp;
-----
&nbsp;

### S3 Interface to Filecoin and IPFS

#### Overview

A multitude of storage applications support the S3 REST API interface. Support an S3 Interface to Filecoin and IPFS so that existing users of the S3 API can easily their port existing archive and retrieve workflows.

#### Description

Proposals should include an initial analysis of the most logical API calls to support. Exploration of interesting features that have good analogies to Filecoin such as [Requester Pays Buckets](https://arxiv.org/help/bulk_data_s3) are welcome. Projects should leverage Filecoin/IPFS data structures and meta indexing considerations.

Proposals that additionally port an existing open source S3 workflow or UI (e.g. [Freezeapp](https://www.freezeapp.net/)) and can dogfood the API in a demo application are highly desired. One potential interesting demo application is an S3 to Filecoin/IPFS migration tool targeting 500 GB or less.

Deliverables:

- An S3 wrapper for Filecoin/IPFS
- A demo that can store and retrieve data via ANY S3 client or Filecoin using the S3 wrapper

**Note:** A current dev grant project is exploring a [Min.io](https://min.io) integration with Filecoin, which provides an S3 API among a number of other convenience features. A previous Min.io integration with IPFS was also explored by [RTradeLtd/s3x](https://github.com/RTradeLtd/s3x).

For a discussion of implementation approaches [see the proposal](https://github.com/protocol/web3-dev-team/blob/45763163912ac6b6e19c28a40cbe1ec9ebaca5ac/proposals/34-aws-s3-facade.md).

#### Effort estimate
- 3-5 weeks


&nbsp;
-----
&nbsp;

### Filecoin PubSub Observatory

#### Overview

Observability into the network's pubsub activity would help improve the visibility of block propagation and network health in the Filecoin network. Moreover, a reputation system for Filecoin peers would help node operators check and debug networking issues. 

#### Description

A community dashboard can help with understanding, debugging, and improving the system overall. Pubsub activity can include:

  - message flows
  - peer scores
  - low-level RPCs (that can be processed to extract higher-level insights)

Using this tool, a protocol engineer could trace block propagation through the network, or a node operator could check their node's score and eventually reputation.

Related prior work includes the PhantomDrift project (https://github.com/libp2p/observer-toolkit and https://github.com/libp2p/observation-deck) that was implemented in Q1/2 of 2020.

Also see the [original proposal](https://github.com/protocol/web3-dev-team/blob/6eb46d6bae942af483ad41b23345b9df5f67254e/proposals/filecoin-pubsub-observatory.md).

#### Effort estimate
-  2-3 weeks

### Skills needed
- go-libp2p familiarity

&nbsp;
-----
&nbsp;

### Better go-ipfs Observability

#### Overview

Although the most advanced implementation of IPFS, go-ipfs can seem like a black box to a node operator. Improving node observability can help operators identify and solve problems, notably with better tracing.

#### Description

Observability consist of 3 pillars: logs, metrics, traces. Those are in different shapes at the moment in go-ipfs and will require different amounts of work.

*Tracing*

Possible work to improve tracing the internals of go-ipfs:

- [add a go context in the data pipeline](https://github.com/ipfs/go-ipfs/issues/6803)
- add tracing in the data pipeline
- add tracing in other important subsystems (pinner, pubsub, connect to the DHT ...)
- support distributed tracing (match traces coming from another system and reaching go-ipfs)

*Logs*

Logs for most of the subsystems are implemented, although not equally. However there is a single sink (stdout) and a unique global filter. Possible work:

- develop an API to register a log sink, with dedicated filtering
- tag the logs with a request ID if availabe, which allow later to match logs and traces
- review the log instrumentation across subsystems to harmonize it

*Metrics*

go-ipfs currently exposes metrics in a Prometheus format. Possible future work:

- review the metric instrumentation across subsystems to harmonize it
- identify missing metrics and implement them

&nbsp;

If executed properly, node operators will be able to:

- diagnose and resolve a wide range of issues
- provide better feedback to the development team
- rely less on support to diagnose those issues and reduce the burden on the IPFS development team
- develop solutions to address those issues

Additionally, better observability also greatly helps during development, to verify correctness and to have actual numbers on which to base implementation decisions.


&nbsp;
-----
&nbsp;

<!--
### Project Title

#### Overview

A tool, script or tutorial to set up....

#### Description

This could help ...

#### Effort estimate

&nbsp;
-----
&nbsp;

-->