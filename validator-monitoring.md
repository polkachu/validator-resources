# Validator Monitoring

Prometheus, Grafana, and Alert Manager are a good stack to monitor the validator node performance. A comprehensive step-by-step setup process is [documented in an official wiki](https://wiki.polkadot.network/docs/en/maintain-guides-how-to-monitor-your-node).

A fellow validator uses the same monitoring stack and publish a [Medium blogpost](https://medium.com/bld-nodes/monitoring-substrate-node-polkadot-kusama-parachains-validator-guide-922734ea4cdb). It is quite similar to the official guide, but does a better job in explaining the conceptual framework and how different pieces fit together. 

I also recommend a log monitoring system to gain more visibility into the node performance. Logs are especially helpful when you go trouble-shooting. I use Promtail to collect logs on validator server and Loki to receive these logs and feed into Grafana on the monitoring server. 



