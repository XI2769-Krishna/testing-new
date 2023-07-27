---
slug: policy-based-deployments-pt-1
id: 2jrxm7grrje3
type: challenge
title: Policy-Based Deployments pt 1
notes:
- type: text
  contents: <br>
tabs:
- title: Policy-Based Deployments pt 1
  type: website
  url: https://docs.google.com/presentation/d/e/2PACX-1vQlPvl0Ix5lGypYPQ2-8CM66qeaEVacrzWs7ctQCydfVDSeBXb7FKJvVJQVSxJ4Xg/embed?start=false&loop=false&delayms=3000
difficulty: basic
timelimit: 600
---

<iframe style="position: relative; height: 80px; width: 80%;" src="https://drive.google.com/file/d/1DlaJnLgpF3Y-cemgod7nuOxR3QX1y7Qx/preview" title="Mp3 player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Placement Policy in the Controller is where a user indicates "intent" for where/how they wish to operate their applications. Depending on the nature of the application, they may have very different ways of tracking the Service Level Objective (SLO). Within Rafay, you have the ability to steer workloads based on Location (datacenter, region, etc), Specific Clusters, or Custom Labels.

- Location Policy - Well-suited for scenarios where the customer's workload needs to deployed to multiple locations and they prefer to "abstract" themselves from the specific clusters which may come and go.
- Specific Cluster Policy - Suited for scenarios where the customer only has a few clusters and knows the exact name of the cluster(s) they would like to deploy to.
- Custom Label Policy - For scenarios where the customer would like to deploy their workload to clusters that match a specified list of "cluster labels.”  Example at left.
