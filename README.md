# network_pipeline
## Table of contents
1. Overview
1.1 Summary
1.2 Problem Statement
1.3 Goal
1.4 Scenarios
2. Solution
2.1 Workflow
2.2 Infrastructure 
3. Implementation
4. Test
---

## 1 Overview
### 1.1 Summary:
The necessary success of an enterprise network should provide stable resource access, rapid and frequent code deployment, full control of security measurements, readiness to accelerate scaling, and instant feedback generation. To drive the approach to enterprise networking to be secure, fast to integrate, scalable, and fully automated, we want to build a network CI/CD pipeline to make it happen.
CI: new code changes are regularly built, tested, and merged to a shared repository
CD: automatically releasing a developer's changes from the repository to production

### 1.2 Problem Statement:

1. Git code management: automate device configuration generation based on unique values per device
2. Inventory mangement: automate device import from planning resources to production and deployment
3. Config Validation/Confirmance: automatically validate devices have correct configurations and contain required config lines
4. CI/CD: gather specific network insight data and display in a custom format
5. Issue Tracking& reporting: automate network and device issue reporting and integrate with ticketing systems

### 1.3 Goal
What is the desired impact? Who are the customers? How will success be measured?
1. Easier for Secure team to audit and do the secure measurement within the whole pipeline
2. More efficient for NetEng team to conduct code deployment, reduce the harddown time during maintainence windows, accelerate scaling
3. Achieve enterprise network management though Infrastructure as Code(IaC) instead of though manual processes
4. Begin to think of network operations as applications to kickoff more tools' development

### 1.4 Scenarios
1. device onboarding
2. device change commit


## 2 Solution:
### 2.1 Workflow:
1. Plan: 
- define sites/device/topology
- scope out IP subnetting
2. Code
- define config templates
- create scripts/playbooks
3. Test
- pre-validate in Batfish
- test in Lab environment?
- report the issue
4. Delivery
- check the target device status
- push to production
- report issues
5. Monitor
- post-validate
- verify network health
- report issues




### 2.2 Infrastructure:
1. Docker: PaaS
1. Netbox: IPAM&Inventory Mangement
2. Vault: Secrets Mangement
3. Git: Version control
4. Jenkins: Automation Engine
5. Batfish: pre-validate
6. Terrform: CD process
7. Grafana: Monitoring

