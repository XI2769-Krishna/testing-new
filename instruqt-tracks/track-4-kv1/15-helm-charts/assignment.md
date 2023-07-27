---
slug: helm-charts
id: ngrjgq3dzg2y
type: challenge
title: Helm Charts
notes:
- type: text
  contents: <br>
tabs:
- title: Helm Charts
  type: website
  url: https://docs.google.com/presentation/d/e/2PACX-1vTkwl4fy6Th2Wlbhie4B2vrb7XEMuy6AB2JqJon2F86jhN96akOCZzsZxrW4CsLHg/embed?start=false&loop=false&delayms=3000
difficulty: basic
timelimit: 600
---

<iframe style="position: relative; height: 80px; width: 80%;" src="https://drive.google.com/file/d/1Dd47dewEcQaHK4tbJX67JUXj1lAP91gR/preview" title="Mp3 player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

This option is well suited for 3rd party applications that are packaged and distributed as Helm charts. It is also a good option for users that have invested in packaging their application as Helm charts.

During workload deployment, the controller will validate the provided Helm chart (a tgz file) and deploy it to multiple managed Kubernetes clusters (as per configured policy)

Benefits

1. Cloaked k8s Control Plane (no inbound access needed, no roles in every cluster)
2. Multi Cluster Deployments
3. No need for a Helm Client
