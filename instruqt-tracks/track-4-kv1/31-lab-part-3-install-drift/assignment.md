---
slug: lab-part-3-install-drift
id: djxmttpalfde
type: challenge
title: Technical Challenge Part 3
notes:
- type: text
  contents: Wait for the green Start button to appear in the bottom right corner.
tabs:
- title: Rafay Console
  type: website
  url: https://console.rafay.dev/
  new_window: true
- title: Terminal
  type: terminal
  hostname: workstation
difficulty: intermediate
timelimit: 1800
---

This is Part 3 of 3 for the technical challenge is designed to provide an overview of the following topics:

* Part 1: Connecting to the Controller and Importing Kubernetes Clusters
* Part 2: Creating a Custom Blueprint
* **Part 3: Installation and Drift Detection**

In Part 3, you will install the custom blueprint onto the rafay-training-1 cluster and observe how the blueprint
enforces Drift protection.

Install the Blueprint
======================

**1. Within the Rafay Console, navigate to Clusters > Infrastructure. In the top-right corner, click on the gear icon for your cluster and select "Update Blueprint".**

![](..\assets\tech_challenge\part_3\0000_cluster_update_blueprint.png)

**2. Select the blueprint you created and click "Save and Publish".**
![](..\assets\tech_challenge\part_3\0001_update_blueprint.png)

**3. Wait until the Blueprint Sync Status is "SUCCESS".**
![](..\assets\tech_challenge\part_3\0002_success.png)

The blueprint will install the node-exporter service as a Kubernetes DaemonSet.



Drift Action
============

**1. Within the Rafay Console, navigate to Infrastructure > Clusters. Click on 'RESOURCES' for your cluster.**
![](..\assets\tech_challenge\part_3\0003_cluster_resources.png)

**2. Navigate to DaemonSets, and then the Namespace where the Node Exporter add-on was installed ([[ Instruqt-Var key="PROJECT" hostname="workstation" ]]-ns). Attempt to delete it from the 3 dots in the top-right corner.**

![](..\assets\tech_challenge\part_3\0004_delete_ds.png)

**3. Confirm that you are attempting to delete the Node Exporter add-on.**
![](..\assets\tech_challenge\part_3\0005_confirm_delete_ds.png)

> HINT: You will be blocked from deleting the DaemonSet because of the Drift Action policy that was associated with the Custom Blueprint.

An alert will be briefly shown in the top-right corner.
![](..\assets\tech_challenge\part_3\0006_brief_alert.png)

**4. Navigate to the Dashboard within your Project, which is the top left menu option. Review the Audit Logs panel. The attempt to delete the DaemonSet will be logged.**

![](..\assets\tech_challenge\part_3\0007_audit_logs.png)

This concludes this exercise. You have created and deployed a custom blueprint that can enforce cluster configuration, guarding against misconfiguration or unauthorized changes.
