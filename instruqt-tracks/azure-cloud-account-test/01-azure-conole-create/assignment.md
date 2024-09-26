---
slug: azure-conole-create
id: h6frz2ortgf3
type: challenge
title: Azure-console
teaser: azure
tabs:
- title: GCP console
  type: service
  hostname: cloud-client
  path: /
  port: 80
- title: CLI
  type: terminal
  hostname: cloud-client
difficulty: basic
timelimit: 1800
---
👋 Introduction
===============

Use the terminal to create vm instance:

```
az group create --name myResourceGroup --location eastus
az vm create --resource-group myResourceGroup --name myVM --image Debian


```

To complete this challenge, press **Check**.
