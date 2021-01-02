# Deploy a high-availability web app using CloudFormation

## Project Problem
Your company is creating an Instagram clone called Udagram. Developers pushed the latest version of their code in a zip file located in a public S3 Bucket.

You have been tasked with deploying the application, along with the necessary supporting software into its matching infrastructure.

This needs to be done in an automated fashion so that the infrastructure can be discarded as soon as the testing team finishes their tests and gathers their results.

## Overview

- Create networking resources using cloud formation template.
```

-   Following resources are created after creating network stack:
    -   VPC
    -   Subnets
    -   Route Tables
    -   Routes
    -   Internet Gateway
    -   NAT Gateways
```
- Create servers for Udagram App which pulls source code from S3 bucket automatically while starting.

```
-   Following resources are created after creating server stack:
    -   Security Groups
    -   IAM Role, Policy, Instance Profile
    -   Launch configuration
    -   Auto Scaling Group
    -   Load Balancer
    -   Target Group
```
- Once the above steps are complete, you can find the URL of application in the outputs section of server stack.

## Project Setup

Run following commands :-

1. ./create.sh net network.yml network-params.json
2. ./create.sh app servers.yml servers-params.json