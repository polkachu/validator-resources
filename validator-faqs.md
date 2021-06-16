# Validator FAQs

## General Validator FAQs

### Which cloud providers should I choose?

It seems that most validators are operated within popular public cloud providers such as AWS, GCP, Digital Ocean, etc. They all provide adequate infrastructure to run a successful validator node. However, you should not purely focus on CPU, memory or storage. Validator node is heavy or ingress and egress, so make sure that the cloud provider offers a good rate in data transfer. 

In this [Medium post](https://mswezey.medium.com/kusama-validator-node-setup-643190a8ac7e), Matt Swezey documented how AWS gave him a surprisingly large bill in data transfer and he switched to Digital Ocean as a result. 

### NVMe or SSD: what storage type should I choose? 

Validator node is quite heavy in disk writing. NVMe is a new generation of storage that offers better speed in disk reading/writing. I \(the site editor\) did an experiment on Digital Ocean with two machines with the same specs except storage type \(NVMe vs SSD\). In a very limited sample size of one experiment, NVMe outperforms SSD by about 20% in CPU efficiency. Interestingly, NVMe droplet is about 20% more expensive than SSD droplet, everything else equal. 

### What are the Thousand Validators Programs and shall I apply?

See the [official link](https://wiki.polkadot.network/docs/en/thousand-validators). 

### What is the minimum amount of KSM/DOT to become a validator?

You can become a "waiting" validator with any amount of KSM/DOT. The challenge is to get into the active set. You can consider to join the Thousand Validators Programs to get a smooth start. 

### I see some validators with a "Para Validator" icon in front of them. What are those and do I need to perform special actions to get it?

The "Para Validator" duty is assigned to a parachain to validator its blocks. It is assigned randomly and changes with each session/epoch. You get higher rewards with the duty. You do not need to perform special actions as a validator. 

### Do I need to run an archive node or pruned node?

Both are okay as a validator. An archive node requires much larger storage space, so most validators probably run pruned nodes. 

## General Thousand Validators Program FAQs

### What should I expect after submitting my application?

### Can I add a second validator in the 1K Program?

Yes for Kusama, and no for Polkadot. For Kusama, when you add a second validator, you need a separate set of controller account and stash account, thus a new set of minimum KSM deposit. 

Your chance of being nominated by Web3 is independent between your two nodes. 

## Kusama Thousand Validators Program FAQs

### How often will I be nominated by Web3?

You will be nominated roughly 1 day of every week or so when you start. Your chance of being nominated will increase as you maintain a well-behaved validator node. It is your responsibility to attract external nominators so you can eventually get into the active set without the help of Web3.   

### 



## 

## 



