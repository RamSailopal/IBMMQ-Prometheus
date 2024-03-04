# IBMMQ-Prometheus

A Prometheus integration for IBMMQ. This allows metrics from IBMMQ to then be viewed in Observability tools such as Elastic of Grafana.

This repository contains a binary built using Golang and a config file taken from [this](https://github.com/ibm-messaging/mq-metric-samples) repository

## Running the process

To run the process and get metric in a format compatible with Prometheus, edit the username and password in the **Config/config.yaml** file and then run:

    git clone https://github.com/RamSailopal/IBMMQ-Prometheus
    cd IBMMQ-Prometheus
    Binary/mq_prometheus -f Config/config.yaml -ibmmq.httpListenHost "0.0.0.0" -ibmmq.httpListenPort 9157

The metrics can then be viewed at

http://serveraddress:9157

 ![Alt text](metrics.png?raw=true?raw=true "metrics")

