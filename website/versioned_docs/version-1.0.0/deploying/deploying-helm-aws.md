---
id: version-1.0.0-deploying-helm-aws
title: Deploying ACS with Helm charts on AWS
sidebar_label: Deploying ACS with Helm charts on AWS
original_id: deploying-helm-aws
---

Use this information to deploy Alfresco Content Services using Helm charts by running a Kubernetes cluster on Amazon Web Services (AWS). This is a deployment template which can be used as the basis for your specific deployment needs.

The Helm charts are provided as a reference that can be used to build deployments in AWS. The Helm charts are undergoing continual development and improvement and should not be used "as-is" for a production deployment. If you're a System administrator, ensure that data persistence, backups, log storage, and other system-level functions have been configured to meet your needs.

Since we need to use private (Enterprise-only) Docker images from Quay.io, you need credentials to be able to pull those images from Quay.io. Alfresco customers can request their credentials by logging a ticket at https://support.alfresco.com/.

Here is a summary of the steps required:

1. Set up your Kubernetes cluster on AWS.
2. Install the Kubernetes Dashboard to manage your Kubernetes cluster.
3. Set up Alfresco Content Services on the Kubernetes cluster, including creating file storage.
4. To access the images in Quay.io, you'll need to generate a pull secret and apply it to your cluster.
5. Deploy Alfresco Content Services.
   Create a Route 53 record set in your hosted zone (optional)
   This is only required if you want to attach a specific DNS name to the cluster, so that applications are available across your global organization. One way to do this is to map the load balancer to your.domain.name by creating a Route 53 record that links the DNS name to the ELB. This allows you to access Share from http://<your.domain.name>/share.
6. Check the status of your deployment.

See the Alfresco/acs-deployment GitHub project documentation for the prerequisites and detailed setup:

* Deploying with Helm charts on AWS using Kops
* Deploying with Helm charts on AWS using EKS

In this project, you can use the Helm charts following the documentation for standard installations, or customize the charts to apply settings as appropriate to your specific deployment environment.