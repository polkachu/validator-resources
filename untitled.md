# Validator Setup

The most comprehensive guide can be found on the official wiki [for Polkadot](https://wiki.polkadot.network/docs/en/maintain-guides-how-to-validate-polkadot) and [for Kusama](https://guide.kusama.network/docs/en/mirror-maintain-guides-how-to-validate-kusama). The setup process is mostly similar, as both are based on the [Substrate Framework](https://substrate.dev/).  

The best way to automate the validator deployment process is through the polkadot-validator-setup script provided by W3F: [https://github.com/w3f/polkadot-validator-setup](https://github.com/w3f/polkadot-validator-setup). It uses Terraform to provision virtual machines and Ansible to automate deployment. You can watch Parity's Joe Petrowski \(research analyst\) and Will Pankiewicz \(master of validators\) speed-running the validator setup process below. 

{% embed url="https://www.youtube.com/watch?v=ejgPSwdLj5o" %}

Of course, you do not need to adopt the full script to make your life easy as a validator. For example, you can just adopt the Ansible script while still manually provisioning machines on AWS, GCP or Digital Ocean without Terraform, especially when you do not have an army of validator servers. 

If you are more of a visual learner, you should check out a comprehensive 3-part YouTube series on validator setup by Paradoxxx, who is an active community member in various support channels. 

{% embed url="https://www.youtube.com/watch?v=maJdf-hfGac&t=23s" %}

{% embed url="https://www.youtube.com/watch?v=l8C06JCdKqo" %}

{% embed url="https://www.youtube.com/watch?v=JEHVZIrTdC4&t=135s" %}

When you need to perform server upgrade, please follow this [official guide](https://wiki.polkadot.network/docs/en/maintain-guides-how-to-upgrade) to minimize downtime and avoid slashing. 

