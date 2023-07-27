---
slug: lab-part-2-create-blueprint
id: umejj9gfg7lx
type: challenge
title: Technical Challenge Part 2
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

This is Part 2 of 3 for the technical challenge is designed to provide an overview of the following topics:

* Part 1: Connecting to the Controller and Importing Kubernetes Clusters
* **Part 2: Creating a Custom Blueprint**
* Part 3: Installation and Drift Detection

In Part 2, you will create a Custom Blueprint that is built upon the minimal blueprint to extend functionality.
In this scenario you will define a namespace, create an Add-On, and install the Add-On using a Custom Blueprint.


Create and Publish a Namespace
========================
Create a namespace that will be the target of the Add-On installed by the Blueprint.

**1. Within the Rafay Console, navigate to Clusters > Infrastructure > Namespaces. Click "New Namespace".**

**Name the namespace the following:**
```
[[ Instruqt-Var key="PROJECT" hostname="workstation" ]]-ns
```

**Set the type to "Wizard", and provide a description. Click "Save" to continue.**

![](..\assets\tech_challenge\part_2\create_namespace\0000_namespace_create_namespace.png)

**2. Keep the default settings within the Configuration tab, click "Save & Go to Placement".**

![](..\assets\tech_challenge\part_2\create_namespace\0001_save_and_placement.png)

**3. Select the Kubernetes cluster under the Placement Policy.**

![](..\assets\tech_challenge\part_2\create_namespace\0002_placement.png)

**4. Publish the Namespace.**

![](..\assets\tech_challenge\part_2\create_namespace\0003_ready.png)

Create an Add-On
================
Create a custom Add-On from by choosing the "node-exporter" service from the Catalog.

**1. Within the Rafay Console, navigate to Infrastructure > Add Ons. Click "New Add-On" and create a new Add-On from the Catalog.**

![](..\assets\tech_challenge\part_2\create_add_on\0000_new_addon.png)

**2. Search the Catalog for "node-exporter" and create the Add-On.**

![](..\assets\tech_challenge\part_2\create_add_on\0001_add_on_catalog_node_exporter.png)

**3. Review the helm chart, and click "Create Add-On".**

![](..\assets\tech_challenge\part_2\create_add_on\0002_create_add_on.png)

**4. Name the Add-On the following:**
```
node-exporter-add-on
```
![](..\assets\tech_challenge\part_2\create_add_on\0003_create_add_on_prompt.png)

**5. Provide a version to the Add-On, and click "Save Changes".**
![](..\assets\tech_challenge\part_2\create_add_on\0004_create_add_on_version.png)

Create a Custom Blueprint
=========================
Create a Custom Blueprint that extends the "minimal" blueprint with the "node-exporter-add-on" Add-On
you created in the previous step.

**1. Navigate to Infrastructure > Blueprints and click on "New Blueprint".**

![](..\assets\tech_challenge\part_2\create_blueprint\0000_new_blueprint.png)

**2. Name the blueprint the following:**
```
node-exporter-bp
```
**Then click Save.**
![](..\assets\tech_challenge\part_2\create_blueprint\0001_blueprint_info.png)

**3. Within the General tab, enter a version number, specify the "minimal" blueprint as the base blueprint, and specify "Block and Notify" for the Drift Action.**
![](..\assets\tech_challenge\part_2\create_blueprint\0002_general_info.png)

**4. Click 'Configure Add-Ons'. You may need to scroll down to see this.**
![](..\assets\tech_challenge\part_2\create_blueprint\0003_configure_add_ons.png)

**4. Add your Add-On.**
![](..\assets\tech_challenge\part_2\create_blueprint\0004_add_add_on.png)

**4. Save the configured Add-On.**
![](..\assets\tech_challenge\part_2\create_blueprint\0005_save_configured_add_on.png)

**3. Make sure no configurable 'Managed System Add-Ons' are enabled. They are not needed for this lab. Finally click Save.**
![](..\assets\tech_challenge\part_2\create_blueprint\0006_managed_system_add_ons.png)

In the next section, you will install the blueprint to your Kubernetes cluster.
