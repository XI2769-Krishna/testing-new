---
slug: custom-blueprints
id: 9ffxcnezglzl
type: challenge
title: Custom Blueprints
notes:
- type: text
  contents: <br>
tabs:
- title: Custom Blueprints
  type: website
  url: https://docs.google.com/presentation/d/e/2PACX-1vQ3o3Ydt7acAxsWzCDVtziSh9xRirXe1LJYoldf-9X4HMJzOL7bRgUuBtjG150QPw/embed?start=false&loop=false&delayms=3000
difficulty: basic
timelimit: 600
---

<iframe style="position: relative; height: 80px; width: 80%;" src="https://drive.google.com/file/d/1DIHeyjIyMzt0zD6Lw1gpvdEXDyiIi0xd/preview" title="Mp3 player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Customers can create and manage "Custom Cluster Blueprints" by adding "addons" to the default cluster blueprints. It is important to emphasize that this "builds on" and "extends" the "Default Cluster Blueprints" and does not replace it.

All cluster blueprints are comprised of one or more software addons. Cluster admins can assemble one or more addons to create a cluster blueprint. Good candidates for "addons" are software components that are meant to be cluster-wide services or operate invisibly in the background. Some examples include:

* Service Mesh (Istio, Linkerd etc)
* Ingress Controllers (Nginx etc)
* Security Products (StackRox, Twistlock, Sysdig etc)
* Cluster Monitoring (Prometheus, Datadog etc)
* Log Collection (Fluentd etc)
* Backup and Restore (Velero etc)
