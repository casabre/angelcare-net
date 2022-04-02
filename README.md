# Angelradio Net

Complete service infrastructure in order to monitor analogue baby monitors. In the end, the monitor should work with all analogue monitors as long as the radio frequency parameter are known.

## Purpose

This project is intended to provide services around FM-based baby monitors in order to
connect, monitor or get alerts via smartphone or laptop.

The project is designed in order to run on a Raspberry Pi with [microk8s](https://ubuntu.com/tutorials/how-to-kubernetes-cluster-on-raspberry-pi#1-overview) either on a single node or a Raspberry Pi cluster.

## Getting started

This repository is currently a mono-repository which contains the source code / configuration for

- Kubernetes setup for router based on WAMP, DSP logic and web frontend
- Source code for
  - Hardware client (Raspberry Pi with a RTL SDR dongle)
  - DSP logic service
  - Web frontend

### Running the services

The setup is meant to run at Raspberry Pi's with a Ubuntu installation but any flavor which supports microk8s should wokr.

Finally, in order to get the setup up and running, there are two steps necessary.

#### Start the hardware client service via systemd

The hardware client package should be added to systemd services by

```shell
prepare the service installation aka fill with live
```

#### Starting K8S infrastructure

In order to start all necessary services, run

```shell
kubectl apply -k k8s
```
