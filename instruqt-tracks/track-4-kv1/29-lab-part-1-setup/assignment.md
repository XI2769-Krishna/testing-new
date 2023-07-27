---
slug: lab-part-1-setup
id: 9l4aseyvldye
type: challenge
title: Technical Challenge Part 1
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
- title: Editor
  type: code
  hostname: workstation
  path: /root/workspace
difficulty: intermediate
timelimit: 1800
---

This is Part 1 of 3 for the technical challenge is designed to provide an overview of the following topics:

* **Part 1: Connecting to the Controller and Importing Kubernetes Clusters**
* Part 2: Creating a Custom Blueprint
* Part 3: Installation and Drift Detection

The first few steps will be directed at setting up the Instruqt workstation to communicate with the Rafay Controller via the API and to import a development Kubernetes cluster that will be used in Part 2 and Part 3 of this technical challenge.

Log in to the Rafay Console
===========================
In this challenge you will create a Project within the Rafay platform to use throughout this course. This creates a dedicated space for experimentation and learning.

>TIP: Open the Rafay Console in a Private Browsing Window or "Incognito Mode" to avoid interference with other sessions.


**1. Within the Instruqt Platform, click the "Open external window" button to launch the Rafay Console.**

![](..\assets\tech_challenge\part_1\login\0000_launch_console.png)

**2. Log in to the Rafay Console with your username and password.**

![](..\assets\tech_challenge\part_1\login\0001_login.png)


Setup the Rafay CLI (rctl)
============================
In order to access the Controller through the API or CLI, you will need to generate API Keys. In this challenge we will use the UI to generate a new API Key and set up a configuration file for the Rafay CLI to consume.

**1. From the Home Screen, click "MY TOOLS"**

![](..\assets\tech_challenge\part_1\cli_credentials\0000-main_console.png)

**2. Click "DOWNLOAD CLI CONFIG"**

![](..\assets\tech_challenge\part_1\cli_credentials\0001-my_tools.png)

**3. On your workstation, locate the JSON file. It's likely in your Downloads folder. Open the file and copy the contents.**

![](..\assets\tech_challenge\part_1\cli_credentials\0002-cli_credentials.png)

**4. Paste the clipboard contents to the "config.json" file of both workstations in your Instruqt environment**

Use any text editor (nano, vi, etc) to edit the file. If you choose a Linux text editor, you can access it from the `Terminal` tab within this Instruqt browser tab.

You can also click the `Editor` tab to use the built-in Instruqt text editor. The benefit of using the built-in Editor is that it has line numbers for easy reference.

> HINT: Be sure to save the file by clicking the floppy disk icon (💾) next to the filename.

![Editing the config.json file](..\assets\tech_challenge\part_1\cli_credentials\0003-cli-editor.png)

**5. Using the Instruqt Terminal Tab, initialize RCTL against your account. Use the following command.**

```
rctl config init workspace/config.json
```

Import a Kubernetes Cluster using the CLI
========================================
To further explore the Rafay Console, we will import a development Kubernetes cluster from each workstation using the Rafay Command Line Utility called `rctl`.


**1. From the Instruqt `Terminal` tab, import the cluster using the "minimal" blueprint using the following command:**

```
rctl create cluster imported [[ Instruqt-Var key="CLUSTER1" hostname="workstation" ]] --blueprint minimal --project [[ Instruqt-Var key="PROJECT" hostname="workstation" ]] > workspace/bootstrap-cluster-1.yaml
```

**2. Wait up to 1 minute for all relevant databases to be updated before applying the generated bootstrap Kubernetes manifest using the following command:**

```
kubectl apply -f workspace/bootstrap-cluster-1.yaml
```

 It will take about 5 minutes for the cluster to register within the Rafay Console.

Checking the Cluster Status
===========================
Part 1 of this technical challenge established two critical pieces for completing the rest of the challenge.

 1. Establishes API connectivity between the Instruqt Environment and the Rafay Controller.
 2. Onboards a development Kubernetes cluster that will be used to demonstrate Rafay's management capabilities.


The Rafay Console also allows you to view the status of the cluster. To view the cluster status, do the following:

**1. Click `[[ Instruqt-Var key="PROJECT" hostname="workstation" ]]`**
![](..\assets\tech_challenge\part_1\review_status\0001-step.png)

**2. Click "Clusters"**
![](..\assets\tech_challenge\part_1\review_status\0002-step.png)

**3. Click "[[ Instruqt-Var key="CLUSTER1" hostname="workstation" ]]"**
![](..\assets\tech_challenge\part_1\review_status\0003-step.png)

**4. Review the detailed status view**
![](..\assets\tech_challenge\part_1\review_status\0004-step.png)

**5. In order to proceed to the next Challenge, the Operational Status must report `READY` and the Control plane must show up as `HEALTHY`.**
![](..\assets\tech_challenge\part_1\review_status\0005-step.png)