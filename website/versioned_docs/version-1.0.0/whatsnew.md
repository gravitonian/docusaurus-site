---
id: version-1.0.0-whatsnew
title: What's new in Alfresco Content Services
sidebar_label: What's new in ACS
original_id: whatsnew
---

See what's new in this Alfresco Content Services 6.1 release.
You can follow our latest updates at Alfrescodocs.

* Alfresco Digital Workspace
* Alfresco Identity Service
* ActiveMQ
* Transform Service
* Cloud deployment templates
* Java 11 support
* Upgraded integrations
* Library upgrades
* REST APIs
* Removed features
* Deprecations


##### Alfresco Digital Workspace

Alfresco Digital Workspace is a new browser based web application built with Alfresco Application Development Framework (ADF).
The Digital Workspace provides an alternative, streamlined user interface for end users, making simple tasks such as uploading,
downloading, searching for content, and collaborating easier than ever.

Alfresco Content Services automatically deploys the application when using Helm charts or a Docker Compose file.
Administrators can also manually install Alfresco Content Services using standard WAR files, and then configure the
installation to include the Digital Workspace.

The Digital Workspace provides comprehensive extensibility features for developers, using the ADF, and allows them to easily
and quickly create custom solutions for specific use cases. See the developer documentation for details.

See Alfresco Digital Workspace documentation for more.

##### Alfresco Identity Service

Single Sign-On (SSO) using the new Alfresco Identity Service 1.0 is supported by the Alfresco Content Services v1 REST APIs. Other components in Alfresco Content Services, such as Alfresco Share and protocol access, do not support the Alfresco Identity Service at this time.

See Alfresco Identity Service documentation for more.

##### ActiveMQ

Previously, this was optional so this is a change from earlier releases. ActiveMQ is now bundled with the repository (in containerized deployments only) to handle raw events.

See Alfresco ActiveMQ Docker images: GitHub Repo and DockerHub Repo

ActiveMQ is required when manually installing Alfresco Content Services 6.1 onwards.

##### Transform Service

The Transform Service performs transformations for Alfresco Content Services in scalable containers. It is enabled by default for Docker Compose and Helm deployments. It is included, but disabled by default, in the zip distribution.

See Alfresco Transform Service documentation for more.

##### Cloud deployment templates

Alfresco Content Services can now be deployed on AWS EKS using Helm charts. This project is in ongoing development and is not designed for production use, although it can be used as a template to get started in quickly orchestrating your Alfresco Content Services infrastructure.

This can be done using the Alfresco Content Services on AWS deployment project in GitHub.

See Deploying Alfresco Content Services using AWS CloudFormation documentation for more.

##### Java 11 support

Alfresco Content Services now supports OpenJDK 11.0.1 and OracleJDK 11.0.1, upgrading from OracleJDK 8.