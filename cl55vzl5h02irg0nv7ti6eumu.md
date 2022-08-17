## My Week 3 @ Polygon Fellowship: Understanding DeFi

Here we are folks, at the Week 3 of learning web3 and leveling up together 🔥. Last week was all about Solidity and Smart Contracts, and this week we'll dive into Defi i.e. Decentralized Finance. Before we begin, I wanted to let you know that this week was difficult for me to follow along with because I am not good at financial. There were some definitions and words that I was unfamiliar with, so I referred frequently to publications outside of the study material and included them in this post as well.

## Week 3: Study material 📓
Just like previous week, we will start with this week's study material. I will try to cover everything I learned through the study material (and beyond it) so let's get started.

### What is DeFi?
DeFi is Decentralised finance, which basically means that it does not require a centralized authority like bank. To build trust, DeFi relies on Blockchain and Smart Contracts.
More Info can be found [here](https://finematics.com/defi-explained/). 

### What is Liquidity?
Liquidity is a term which is used frequently when it comes to finance. According to investopedia, "liquidity" describes how quickly or easily a security or asset can be turned into cash without hurting its market value.
In the crypto space, to put it simply, liquidity refers to how simple it is to buy or sell an asset.

### Liquidity Pools
Liquidity Pool is a mechanism which ensures Liquidity in DeFi space. I won't go into much detail, but how it operates is that users lock a pair of tokens in a pool, and each pool establishes a new market for that specific pair of tokens. **The liquidity provider earns some rewards for providing liquidity**. Now, this pool is capable of facilitating swaps between the pair as needed, thereby supplying liquidity.
You may read a more in-depth article regarding liquidity pools [here](https://finematics.com/liquidity-pools-explained/).

### How does Lending and Borrowing Works in DeFi
Any financial institution's core business is lending and borrowing; to borrow money from a lender, one must pay interest.
DeFi lending enables users to become lenders or borrowers while keeping full custody of their coins.
**Lender will provide the tokens and earn interest in return**. A smart contract receives the provided tokens and makes them available for other users to borrow.  
However, in DeFi  a user who wants to borrow funds has to supply tokens in the form of collateral that is worth more than the actual loan that they want to take.
A much detailed article about lending and borrowing in DeFi can be found [here](https://finematics.com/lending-and-borrowing-in-defi-explained/).

### Flash Loans
Again, not covering the details, a flash loan is a feature that allows you to borrow any available amount of assets from a designated smart contract pool with no collateral. A flash loan must be taken out and repaid in the same blockchain transaction, though.

### Some common Protocols

After learning about all these awesome DeFi terms, wouldn't it be awesome if we are able to utilize them in our smart contracts, without writing them from scratch? That's where protocols comes in, these protocols can facilitate lending, borrowing, yeild farming, stacking and a lot more with just a few lines of code.
I am myself still learning about a lot of these 

**Swapping between tokens**: Uniswap, 1Inch  
**Lending and Borrowing**: Compound   
**Liquidity Pools**: Aave, Curve   
**Flash Loans**: Aave   
Don't forget to check the official websites of these protocols to learn more about them.

### Resources to Learn more About DeFi and these Protocols:
If you want to learn more about DeFi I would highly recommend Finematics Blog and YouTube channel. You can start with this post right [here](https://finematics.com/guide-to-decentralized-finance/).

## Week3: Assignments

### Making a Lending DApp

This week's assignment was to make a Lending DAPP that takes in Ethereum as collateral and send a stable coin to the sender. This stable coin can be returned to get collateral back.

#### Steps Involved

**1) Getting ETH Price**

The first step is to get the ETH price in fiat. This is accomplished by something called oracles. Oracles are data providers that can interact with Web2 APIs and data streams and bring them on your smart contract. I have used chainlink as Oracle to get ETH / USD price. 
You can check the documentation [here](https://docs.chain.link/docs/get-the-latest-price/).  

**2) Issuing a stable token**

The tokens will not magically get generated, we have to work on our own token. For interoperability, many Web3 tokens have been given certain common definitions. We will be using ERC20 token standard. We can import the contracts created by OpenZeppelin for such standards instead of having to develop this contract from scratch. (If you don't know what OpenZeppelin is, I recommend going through the CryptoZombies course, which I discussed in my Week 2 Post.) 
Our token will have two functions mint and burn. 'mint' will issue the token and 'burn' will destroy it. These functions can only be called by owner of smart contract.
To read more about ERC20 standard refer [here](https://docs.openzeppelin.com/contracts/4.x/erc20). Also, I would highly recommend going through the documentation [here](https://docs.openzeppelin.com/contracts/4.x/api/token/erc20#IERC20). Lastly make sure to check the [Contract Wizard](https://docs.openzeppelin.com/contracts/4.x/wizard) by OpenZepplin which will generate smart contracts for us.

**3) Work on the Lending Contract**

Given that we already have everything we need, this is rather simple. Because this contract will be creating and disposing of tokens, make sure it is the owner of the stable coin.
The borrow function of this contract will use oracle to determine the price, and mint the tokens according to the price determined for the message sender. With the use of mappings, we can keep track of the debt and collatoral of the message sender after minting.
The user needs to have enough issued Stable Coin in his wallet in order to withdraw the colleteral. The stable coin equivalent to his debt will be burned from his wallet and his debt will be cleared.

That wraps up the week3. Hope you learned something new with this post. 
#WAGMI 🚀