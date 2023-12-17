### kubeplugin

This is a kubectl plugin that retrieves resource usage statistics from Kubernetes.

## Requirements

[kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)

## Installation 

```bash
curl -O https://raw.githubusercontent.com/vasyl-babynets/AsciiArtify/main/scripts/kubeplugin
sudo chmod +x kubeplugin
sudo mv kubeplugin /usr/local/bin/kubectl-kubeplugin
sudo kubectl plugin list
```

## Usage

```
kubectl kubeplugin ['node' or 'pod'] [namespace]
```

## Example

```
kubectl kubeplugin pod kube-system



Resource: pod
Namespace: kube-system

Name                                    CPU  Memory
coredns-77ccd57875-vf7vr                5m   27Mi
local-path-provisioner-957fdf8bc-ngchx  2m   16Mi
metrics-server-648b5df564-ggzqd         13m  33Mi
svclb-traefik-b0044e2b-2fjdd            0m   2Mi
traefik-64f55bb67d-xjf4s                1m   34Mi
```