## My Week 4 @ Polygon Fellowship: IPFS & Graph

Okay we are halfway through the fellowship, and in this week's post, we will go through IPFS and Graph. Again, we will start with the study material and then the assignments and lastly through the sessions.

# Week 4 : Study material 📔

## Decentralized Storage
So, apparantly, blockchains can't be used to store huge data, cause that will result in high network fees. To solve this problem we have decentralized storage. A decentralized storage works on a peer to peer network where each peer acts as a file storage as well as a provider.
The study material this time has refered tons of documents, so I am refering them here:
* [Persistence mechanism/incentive structure](https://ethereum.org/en/developers/docs/storage/#persistence-mechanism).
* [Data retention enforcement](https://ethereum.org/en/developers/docs/storage/#data-retention)
* [Decentrality](https://ethereum.org/en/developers/docs/storage/#decentrality)
* [Consensus](https://ethereum.org/en/developers/docs/storage/#decentrality)

### What is IPFS

The InterPlanetary File System (IPFS) is a protocol started by Protocol Labs to create a new way to server information on the web. It's decentralized and works on content addressing. If you want to add any file to IPFS, you need access to a node, these nodes may store some data, but most importantly, they work as a file provider to other nodes.
So, consider node A is closest to node B and node C has a files, considering C is also close to B, the file will follow the path `C -> B -> A`. You can even use your laptop to make an IPFS node.   
I spent a lot of time learning about IPFS, cause I found this idea amazing, so I will link to all the docs I refered down:
* [What is IPFS?](https://docs.ipfs.io/concepts/what-is-ipfs/)
* [How IPFS works](https://docs.ipfs.io/concepts/how-ipfs-works/)
* [IPFS on command line](https://docs.ipfs.io/how-to/command-line-quick-start)
* [Using IPFS in your js](https://dev.to/edge-and-node/uploading-files-to-ipfs-from-a-web-application-50a)

### What is Filecoin

Filecoin is protocol developed as an incentive layer for the Interplanetary File System (IPFS). Filecoin allows anyone to store and retrieve data on the internet. Built-in economic incentives ensure that files are stored and retrieved reliably and continuously for however long a user specifies.
Filecoin has one of the coolest web pages I have seen so far, https://filecoin.io/.
To learn about Filecoin and how it can be utilized, you can checkout this video here:
<iframe width="560" height="315" src="https://www.youtube.com/embed/P28aNAdZDi4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>  

Also I would suggest to go through [this](https://proto.school/course/filecoin) course that will teach you everything about filecoin.

### Learning about Fleek
Fleek’s hosting solution is like Netlify for the open web, enabling developers to deploy websites to the Internet Computer in mere minutes. You can check more about them [here](https://fleek.co/).
You can check more about it, and how to use it [here](https://docs.ipfs.io/how-to/websites-on-ipfs/introducing-fleek).

### Other Decetralized storage related projects
The study material briefly introduced us to [Sia](https://sia.tech/), [Storj](https://www.storj.io/), [Swarm](https://www.ethswarm.org/) and [Arweave](https://www.arweave.org/)

## Querying Blockchain & The Graph

Reading data from blockchain is slow, so a lot of organizers index the entire blockchain and serves it's data. However, this is againt decentralization. Thus we have graph, The Graph is a decentralized protocol for indexing and querying blockchain data.
It uses GraphQuery language to query indexed chains.

Firstly to understand how graph works, you can check their official docs [here](https://thegraph.com/docs/en/about/introduction/).

To learn how to query using graph you can check this doc [here](https://thegraph.com/docs/en/developer/querying-from-your-app/).

To make your own graphs, look here: 
<iframe width="560" height="315" src="https://www.youtube.com/embed/HfDgC2oNnwo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>  
  
     
# Week 4: Assignments

## Uploading an Image on IPFS.

This one is pretty easy, you can follow along the IPFS Docs to work on this one.

## Creating a subgraph

This one took some time, cause graph is new to me, but again, the resources are great.

## Building Social Media DApp

This one took a LOT OF TIME. We were supposed to create a social media DApp that allows us to post and view images. 
You can look at my solution [here](https://devfolio.co/projects/kuesocial-4dd3). 
