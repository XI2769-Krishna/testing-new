---
slug: declarative-cluster-provisioning-pt-1
id: d1nrymp0o6cs
type: challenge
title: Declarative Cluster Provisioning pt 1
notes:
- type: text
  contents: <br>
tabs:
- title: Declarative Cluster Provisioning pt 1
  type: website
  url: https://docs.google.com/presentation/d/e/2PACX-1vQjex3Vn46GhOS3omWapHEmgECGDWshkxBRA6tfFFxLx0A7SIfdG9gkM-vxa64Pmw/embed?start=false&loop=false&delayms=3000
difficulty: basic
timelimit: 600
---

<iframe style="position: relative; height: 80px; width: 80%;" src="https://drive.google.com/file/d/1DTPr8zMgzJ5xifszunNn3HbRQ0Q1xcy1/preview" title="Mp3 player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

A common pattern is for users to use Terraform to provision Kubernetes clusters perhaps using a Jenkins based pipeline. These brownfield clusters can then be imported into the controller.

**Typical Automation Sequence**

The image showcases a Jenkins based "pipeline" that automates the following steps.

* Uses Terraform to provision a Kubernetes cluster based on a version controlled cluster spec in a Git repo.
* Imports the raw Kubernetes cluster into the Controller
* Brings the cluster to a state of compliance with specified cluster blueprint.
