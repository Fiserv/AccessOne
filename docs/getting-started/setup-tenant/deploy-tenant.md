# Deploy the tenant

## Documentation Quickstart Guide

Need to deploy your application ? 

This quick start guide will provide you the necessary steps to get your Application setup, configure and deploy on Cloud Server really quick.

> Recommended : To complete following steps before proceeding to deployment process. 

* Tenant Creation
* Tenant Registeration
* Tenant Repository Setup

Now, developer is ready to deploy your tenant application. Developer can delpoy application in any open cloud server. Here we are providing example for new application deployment within IBM cloud with OpenShift Cluster. 

## Deployment checklist

    Installed and Running OpenShift cluster on cloud Server
    
## Recommended guidelines for deployment with Fiserv Dev Portal

Here are the following steps to integrate your new tenant server within OpenShift cluster. 

## Step 1: Login to IBM OpenShift cluster 

Once developer navigate to Home page of OpenShift. Please select your running cluster.

Example: \<new-running-cluster>


## Step 2: Click 'OpenShift web console' link as shown below

This link will navigate to Openshift Cluster Main page

![OpenShift webconsole](/assets/images/OpenShit_web_console.png)

## Step 3: Setting Role

Set the role to **Developer** and select **Topology**.

![OpenShift Developer Role](/assets/images/OpenShift_topology.png)

## Step 4: Create New Project

Select **Create Project** from 'Project' dropdown menu.

![OpenShift Create Project](/assets/images/OpenShift_project_drop_down.png)

## Step 5: Enter Project details

Enter Project Name as **\<sample-name>-workshop** and click **Create**. developer can also set 'Display Name' and 'Description' same as your 'Project Name'. 

Now, developer is ready to create new project in this workspace. 

![OpenShift Create Project](/assets/images/OpenShift_create_project.png)

## Step 6: Setting up Project

Select your project from the 'Project dropdown' and add your private SSH key under **Secrets** by following below steps:

* Click **Secrets** menu from left menu bar:

* Select **Create** dropdown present in Top Right Corner and select **Source Secret**. Developer have to set following details such as

    * **Secret Name** :  \<your-name>-SSH-Private-Key
    * **Authentication type** : SSH
    * **SSH Private Key** : Develpor can browse the SSH private key from local machine or developer can paste it directly into Text Box.

## Step 7: Select **+Add** option

Select **+Add** option from menu to create new application. Developer have '4' different options to configure application from 

*   From GIT
*   Container Image
*   From Dockerfile
*   YAML

Here, we are creating an application using option **'From Docker'**


## Step 8: Repository Setup

Developer needs to provide repository URL to add into application. For example we are adding repository from BitBucket(Ex:git@bitbucket.org:fiserv-digital-tech/dev-portal-ui.git

![Bitbucket Repo](/assets/images/Bitbucket_git_repo.png)

Now add the Git URL in **Git Repo URL** option on Import from Dockerfile page. Click **Show Advance Git Options**. 

> Note: Developer can configure with custom settings, as these configuration are setup for sample project. 

![Bitbucket Repo](/assets/images/Openshift_git_project.png)

## Step 9: Developer needs to fill following information for the setup:

*   **Git Reference** : 'develop'

*   **Context Directory** : If 'Dockerfile' is at root level you can leave this option blank, Otherwise developer needs provide path of the Docker Files.

    Example: /\<sub-directory>

*   **Source Secret** : Select your SSH-Private-Key added from Step 6.

![Bitbucket Repo](/assets/images/Openshift_git_project_setup.png)


## Step 10: Update General section

*   **Application**: Select Create Application and enter \<application-name>. This is used for grouping your application created under your project. If developer want to create any Tenant Application state as 'Tenants'

*   **Name** : Name of the application, developer want to configure.Ex: dev-portal-ui

*   **Resources** : Please Select **Deployment Config** option.

![Bitbucket Repo](/assets/images/Openshift_create_application_start.png)


## Step 11: Select **Create**

Click **Create** button to generate the application resource.

![Bitbucket Repo](/assets/images/Openshift_create_application_completed.png)

## Step 12: Generating Application

Now developer should able to see application icon in your Topology view.

![Bitbucket Repo](/assets/images/Openshift_app_icon.png)

Please wait until Build and Deployment is completed. Once completed icon should display like below.

![Bitbucket Repo](/assets/images/Openshift_app_ready.png)

### Step 14: Launching your application

Final step is to launch your application by clicking on Open URL.

![Bitbucket Repo](/assets/images/Openshift_app_launch.png)