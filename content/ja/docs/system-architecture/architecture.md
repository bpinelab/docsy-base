---
title: Azure Landing Zone Architecture
date: 2024-10-03
description: >
  This document outlines the system architecture based on the Azure Landing Zone
  model. The focus is on scalable, automated, and secure operations.
categories: [Architecture]
tags: [Azure, Landing Zone, System Architecture]
---

{{% pageinfo %}} This document describes the architecture of an IT system using
the Azure Landing Zone framework, aiming for full automation and operational
efficiency. {{% /pageinfo %}}

## Overview

Azure Landing Zone provides the foundation for deploying and managing scalable,
secure, and automated environments in the cloud. By following best practices, it
ensures that your infrastructure is well-architected for automation and future
growth.

## Subscription Breakdown in Azure Landing Zone

In an Azure Landing Zone architecture, subscriptions are separated by key
functions such as identity, management, connectivity, and more. Each
subscription is designated to handle specific responsibilities, ensuring clear
boundaries for governance, security, and operational management.

### 1. **Identity Subscription**

- **Purpose**: Manages identity-related services, primarily Azure Active
  Directory (AAD) and associated security roles.
- **Includes**: Azure AD, Role-Based Access Control (RBAC), Conditional Access
  Policies.
- **Role**: Centralized identity management across all environments, ensuring
  secure access to resources.

### 2. **Management Subscription**

- **Purpose**: Handles the management and monitoring tools needed for governance
  and operational oversight.
- **Includes**: Azure Monitor, Azure Security Center, Azure Automation, Log
  Analytics.
- **Role**: Centralized location for operations management, including
  monitoring, patching, and automation of cloud resources.

### 3. **Connectivity Subscription**

- **Purpose**: Provides the foundational networking services to connect
  resources across all subscriptions.
- **Includes**: Azure Virtual Network (VNet), Azure Firewall, Network Security
  Groups (NSGs), ExpressRoute, VPN Gateway.
- **Role**: Ensures a secure, scalable network infrastructure that supports
  hybrid connectivity, network isolation, and traffic control.

### 4. **Landing Zone Application Subscription**

- **Purpose**: This is where application-specific resources reside, divided by
  workload or department.
- **Includes**: Virtual Machines (VMs), App Services, Databases, Storage
  Accounts.
- **Role**: Dedicated environments for specific workloads, with production,
  development, and test environments clearly isolated.
- **Sub-Subscriptions**:
  - **Production Subscription**: Runs the live workloads.
  - **Development Subscription**: For development and testing purposes, separate
    from production.

### 5. **Sandbox Subscription**

- **Purpose**: A dedicated subscription for experimentation, testing, and
  training with minimal governance policies.
- **Includes**: General-purpose compute, storage, and network resources.
- **Role**: Isolated environment where developers and engineers can test without
  affecting production or other critical environments.

## Architecture Diagram

For a visual representation of the subscription architecture in Azure Landing
Zone, please refer to the following
[diagram](https://learn.microsoft.com/ja-jp/azure/cloud-adoption-framework/ready/enterprise-scale/media/ns-arch-cust-expanded.svg#lightbox).

![Azure Landing Zone Subscription Architecture](https://learn.microsoft.com/ja-jp/azure/cloud-adoption-framework/ready/enterprise-scale/media/ns-arch-cust-expanded.svg#lightbox)

This diagram illustrates how subscriptions are structured within a landing zone
to provide clear separation of environments and services, ensuring effective
management and security.

### Benefits of Subscription Segmentation

- **Security Isolation**: Each subscription can have its own security and
  compliance policies, ensuring a clear boundary between critical and
  non-critical systems.
- **Cost Management**: Subscriptions allow cost segregation by project,
  department, or workload, making it easier to track and manage expenses.
- **Governance**: With defined roles and responsibilities across subscriptions,
  policies and governance are easier to implement and maintain.

## Automation Strategy

Azure Landing Zone heavily focuses on automation for deployment, maintenance,
and recovery operations. These automated processes span across all subscriptions
to ensure consistency and reduce manual intervention.

### 1. **Resource Deployment Automation**

Azure Resource Manager (ARM) templates and Terraform scripts automate the
provisioning of cloud resources across all subscriptions.

This is an example Terraform snippet. resource "azurerm_virtual_network"
"example" { name = "example-vnet" location =
azurerm_resource_group.example.location resource_group_name =
azurerm_resource_group.example.name address_space = ["10.0.0.0/16"] }

### 2. **Patch Automation**

Azure Automation and Update Management services automate patch deployment for
resources.

- **KPI**: Achieve X% reduction in manual patch application by automating update
  tasks.

### 3. **Backup Automation**

Azure Backup ensures that all critical resources are automatically backed up on
a regular schedule.

- **KGI**: Reach 100% automated backup coverage across all essential resources
  by [Year].

## Conclusion

Azure Landing Zone provides a robust, scalable architecture that enables
organizations to streamline operations, increase security, and reduce manual
intervention through automation. By adopting this model, your IT infrastructure
can efficiently meet the growing demands of modern business operations.
