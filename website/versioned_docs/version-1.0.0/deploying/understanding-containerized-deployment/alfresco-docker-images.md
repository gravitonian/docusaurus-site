---
id: version-1.0.0-alfresco-docker-images
title: Alfresco Docker Images
sidebar_label: Alfresco Docker Images
original_id: alfresco-docker-images
---

The public Alfresco Docker images are available in the Docker Hub registry. There are also private Enterprise-only images in the Quay.io registry.

Go to Docker Hub https://hub.docker.com/u/alfresco/ to see a list of images belonging to the alfresco user similar to the following screenshot (note that not all images are visible):


There are a number of Docker images that relate to Alfresco Content Services:

* alfresco/alfresco-share - the Share web interface (i.e. share.war) running on Apache Tomcat
* alfresco/alfresco-search-services - the Solr 6 based search service running on Jetty
* alfresco/alfresco-content-repository - the repository app (i.e. alfresco.war) running on Apache Tomcat
* alfresco/alfresco-activemq - the Alfresco ActiveMQ image

There are also other supporting features available, such as Docker images for image and document transformation:

* alfresco/alfresco-imagemagick
* alfresco/alfresco-libreoffice
* alfresco/alfresco-pdf-renderer
* alfresco/alfresco-tika

To build the alfresco/alfresco-content-repository image, Alfresco uses the Alfresco/acs-packaging GitHub project. This project doesn't include any deployment templates. The Alfresco/acs-deployment GitHub project contains deployment templates and instructions. It includes a Docker Compose script that's used to launch a demo, test, or PoC of Alfresco Content Services. You can customize this script, if you like, in order to run with different versions than those set by default (which are usually the latest versions).