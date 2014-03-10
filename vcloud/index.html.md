---
title: Deploying Cloud Foundry on vCloud Hybrid Service or vCloud Director
---

## Overview ##

Installation of Cloud Foundry on vCloud Hybrid Service (vCHS) or vCloud Director goes through the following steps:

1. [Set up vCHS or vCloud Director](setup-vcloud.html)  
Configure a **virtual datacenter** for the installation, then deploy a **jump box** in the virtual datacenter. The rest of the installation is driven from this jump box.

2. [Deploy Micro BOSH](deploying_micro_bosh.html)  
Deploy **Micro BOSH** from the jump box. Micro BOSH is a single VM version of BOSH.

3. **Optional:** [Deploy BOSH using Micro BOSH](deploying_bosh_with_micro_bosh.html)  
If you need production level resilience and/or large scale, install **BOSH** using Micro BOSH. Most installations of Cloud Foundry can be done without this step by using Micro BOSH installed in step 3. Since it adds some complexity we suggest avoiding this step if possible.

4. [Deploy Cloud Foundry using Micro BOSH or BOSH](deploy_cf.html)


## Sample manifest files ##


The following pages provide example manifests for deploying Micro BOSH, BOSH and Cloud Foundry.

[Micro BOSH example manifest](micro-bosh-example-manifest.html)

[BOSH example manifest](bosh-example-manifest.html)

[Cloud Foundry example manifest](cloud-foundry-example-manifest.html)