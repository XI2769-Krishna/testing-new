---
slug: blueprints-and-add-ons
id: jytjx0zvyt0w
type: challenge
title: Blueprints and Add-ons
notes:
- type: text
  contents: <br>
tabs:
- title: Blueprints and Add-ons
  type: website
  url: https://docs.google.com/presentation/d/e/2PACX-1vT26rTO5vPjVEciCPUZUcXgq9WiKgJa313vzAeZzroxjNBcqjthiRmI6C9bBINvdg/embed?start=false&loop=false&delayms=3000
difficulty: basic
timelimit: 600
---

<iframe style="position: relative; height: 80px; width: 80%;" src="https://drive.google.com/file/d/1D-wFpHkBCC5jZPbSm4MRYY9GsM1eX7h1/preview" title="Mp3 player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Blueprints are composed of add-ons. A blueprint requires at least the essential add-ons, and can optionally include more, depending on the use-case.

Rafay requires essential add-ons to manage the Kubernetes cluster. This is standard no matter which blueprint is applied to a cluster.

Rafay-Managed optional add-ons are prepackaged software that enhance/build-upon a default Kubernetes distribution.

Customer Add-Ons are fully customizable packages that can include home-grown packages or user-facing software

Managed System Add-ons can be added to a cluster blueprint and be deployed on clusters. Once enabled in a blueprint, the required k8s software components - usually in the form of cluster utilities such as logging, monitoring, ingress, as well as higher-level user-facing software packages - and configuration are automatically deployed to the target clusters.
