# Validator FAQs

## Which cloud providers should I choose?

It seems that most validators are operated within popular public cloud providers such as AWS, GCP, Digital Ocean, etc. They all provide adequate infrastructure to run a successful validator node. However, you should not purely focus on CPU, memory or storage. Validator node is heavy or ingress and egress, so make sure that the cloud provider offers a good rate in data transfer. 

In this [Medium post](https://mswezey.medium.com/kusama-validator-node-setup-643190a8ac7e), Matt Swezey documented how AWS gave him a surprisingly large bill in data transfer and he switched to Digital Ocean as a result. 

## NVMe or SSD: what storage type should I choose? 

Validator node is quite heavy in disk writing. NVMe is a new generation of storage that offers better speed in disk reading/writing. I \(the site editor\) did an experiment on Digital Ocean with two machines with the same specs except storage type \(NVMe vs SSD\). In a very limited sample size of one experiment, NVMe outperforms SSD by about 20% in CPU efficiency. Interestingly, NVMe droplet is about 20% more expensive than SSD droplet, everything else equal. 



