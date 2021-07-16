# Validator FAQs

## General Validator FAQs

### What are the Thousand Validators Programme and shall I apply?

See the [official link](https://wiki.polkadot.network/docs/en/thousand-validators).

### What is the minimum amount of KSM/DOT to become a validator?

You can become a "waiting" validator with as little as 1 DOT and 0.002 KSM. The challenge is to get into the active set. You can consider joining the Thousand Validators Programme to get a smooth start.

### I see some validators with a "Para Validator" icon in front of them. What are those and do I need to perform special actions to get it?

The "Para Validator" duty is assigned to a parachain to validator its blocks. It is assigned randomly and changes with each session/epoch. You get higher rewards with the duty. You do not need to perform special actions as a validator.

### Do I need to run an archive node or pruned node?

Both are okay as a validator. An archive node requires much larger storage space, so most validators probably run pruned nodes.

### How do I quickly sync up my validator with the latest block?

When you start out, it typically takes days to sync up to the latest block for your validator. If you want to quickly sync up, you can use the chain snapshots provided by [https://polkashots.io](https://polkashots.io/). This is for pruned nodes only. If you prefer to run an archive node, you cannot use the snapshot.

### How do I do server maintenance while minimizing downtime?

Your starting point is the [official upgrade guide](https://wiki.polkadot.network/docs/en/maintain-guides-how-to-upgrade). That said, we have found that a short period of downtime is harmless when you are not in the active set. This is much less hassle than the Server A -&gt; Server B -&gt; Server A switch described in the official guide.

### Which cloud providers should I choose?

It seems that most validators are operated within popular public cloud providers such as AWS, GCP, Digital Ocean, etc. They all provide adequate infrastructure to run a successful validator node. However, you should not purely focus on CPU, memory or storage. Validator node is heavy or ingress and egress, so make sure that the cloud provider offers a good rate in data transfer.

In this [Medium post](https://mswezey.medium.com/kusama-validator-node-setup-643190a8ac7e), Matt Swezey documented how AWS gave him a surprisingly large bill in data transfer and he switched to Digital Ocean as a result.

### NVMe or SSD: what storage type should I choose?

The validator node is quite heavy in disk writing. NVMe is a new generation of storage that offers better speed in disk reading/writing. I \(the site editor\) did an experiment on Digital Ocean with two machines with the same specs except storage type \(NVMe vs SSD\). In a very limited sample size of one experiment, NVMe outperforms SSD by about 20% in CPU efficiency. Interestingly, NVMe droplet is about 20% more expensive than SSD droplet, everything else equal.

## General Thousand Validators Programme FAQs

### What should I expect after submitting my application?

Applications are accepted on a rolling basis. As long as you fulfill all requirements detailed in the [official program guide](https://wiki.polkadot.network/docs/en/thousand-validators), your validator will automatically be included in the programme in the next admission cycle.

### Can I add a second validator in the 1K Programme?

Yes for Kusama, and no for Polkadot. For Kusama, when you add a second validator, you need a separate set of controller account and stash account, thus a new set of minimum KSM deposit.

Your chance of being nominated by Web3 is independent between your two nodes.

### What are good commission strategies to get the most out of the programme?

There is no one-size-fits-all strategy. That said, we have observed three common strategies attempted by various validators:

1. **Lowest Commission in Town**: These validators give up short-term gains by setting 0% commission. They believe that they can get external nominators quickly so they can fly solo without the help of Web3 ASAP.
2. **Maximum Commission Allowed**: These validators set the maximum commission allowed while participating in the programme: 10% for Kusama and 3% for Polkadot. Running a good validator node is a noteworthy commitment, and they want to be rewarded for it. 
3. **Breakeven with Staking**: These validators calculate a breakeven commission rate as if they are staking their bonded KSM/DOT, plus the cost/effort of running a validator server. These validators probably come out with slightly different numbers depending on assumptions, but we believe that the breakeven commission rate is about 6-7% for Kusama and 1-2% for Polkadot when the validator is in the active set once a week. 

### What is Web3's algorithm to nominate validators?

You can find Web3's nomination algorithm [here](https://github.com/w3f/1k-validators-be). Here is a quick code snippet where the weight of each factor is documented. You can see where you stand in terms of these factors in the [Kusama program leaderboard](https://thousand-validators.kusama.network/#/leaderboard). Basically, you will have a higher chance of being nominated by Web3 if:

1. You joined the programme earlier
2. You have not been nominated in a while
3. You are not offline recently
4. Your rank is higher
5. You have not committed faults
6. Your self-bond is higher
7. You payout rewards in a timely fashion

```text
  // Weighted scores
  // Discovered at - earlier is preferrable
  // Nominated At - Not nominated in a while is preferrable
  // offlineAccumulated - lower if prefferable
  // rank - higher is preferrable
  // faults - lower is preferrable
  // unclaimed eras - lower is preferrable
  // inclusion - lower is preferrable
  // bonded - higher is preferrable

  INCLUSION_WEIGHT = 5;
  SPAN_INCLUSION_WEIGHT = 40;
  DISCOVERED_WEIGHT = 5;
  NOMINATED_WEIGHT = 35;
  RANK_WEIGHT = 5;
  UNCLAIMED_WEIGHT = 15;
  BONDED_WEIGHT = 13;
  FAULTS_WEIGHT = 5;
  OFFLINE_WEIGHT = 2;
```

### What is "Rank" in the Thousand Validators Programme?

Rank is a representation of status and success in the programme. Rank points are increased by 1 for every 24 hours the validator has successfully been validating in the active validator set. Ranks Points are halved when validators are offline. Rank Points are not relative to others, and the higher the better.

You need a rank of 25 or above in the Kusama programme in order to be eligible for the Polkadot programme.

### What if I forget to claim the rewards?

Not possible. You can claim your rewards for you and your nominators within 20 eras. After this, they will be claimed for you by Web3, and your negligence will decrease your rank by 3 points. So the bottom line is to claim the rewards in a timely fashion.

## Kusama Thousand Validators Programme FAQs

### How often will I be nominated by Web3?

You will be nominated roughly 1 day of every week or so when you start. Your chance of being nominated will increase as you maintain a well-behaved validator node. It is your responsibility to attract external nominators so you can eventually get into the active set without the help of Web3.

