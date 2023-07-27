---
slug: yaml-pt-1
id: fhaqt7jxeppt
type: challenge
title: YAML pt 1
notes:
- type: text
  contents: <br>
tabs:
- title: YAML pt 1
  type: website
  url: https://docs.google.com/presentation/d/e/2PACX-1vQfiE4Iq9Qifl_cD7ls2lpUtHFnt-bK6CBeDG3RDv7nopSmZXh8KSMAeAicyY3BWQ/embed?start=false&loop=false&delayms=3000
difficulty: basic
timelimit: 600
---

<iframe style="position: relative; height: 80px; width: 80%;" src="https://drive.google.com/file/d/1D_3J9hF3fhKGAcB5hznSTa9DgdCRdTpz/preview" title="Mp3 player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

This option is ideal for situations where the user already has the Kubernetes YAML for their application.

During workload deployment, the controller will validate the provided yaml file and deploy it to multiple managed Kubernetes clusters (as per configured policy).

Benefits

1. Cloaked k8s Control Plane (no inbound access needed, no roles in every cluster)
2. Multi Cluster Deployments
3. No need for kubectl
