#Windows Azure Active Directory Java Library Sample Application


This Java web application has been written to provide you with a quick and easy way to set up your first app that connects to Windows Azure Active Directory. This demonstration application, written to run in on any platform, will provide you with the libraries requierd to build your own java applications. We've released all of the source code for this running example in GitHub under an Apache 2.0 license, so feel free to clone (or even better, fork!) and provide feedback on the forums.

## Quick Start

Getting started with the sample is easy. The walkthrough relies on various prerequisites being met by the software environment offered by the target machine.Note that an expert Java developer should be able to easily apply the techniques shown here to any other application server. 

### Step 1: Register a Windows Azure AD Tenant

To use this sample you will need an Azure Active Directory Tenant. Not sure what a tenant is or how you would get one? We recommend that you read [What is a Windows Azure AD tenant](http://technet.microsoft.com/library/jj573650.aspx)? or [Sign up for Windows Azure as an organization](http://www.windowsazure.com/en-us/manage/services/identity/organizational-account/) to get you started on your way to using Windows Azure AD.

### Step 2: Generate A Service Principal for your Windows Azure AD Tenant

After you get your Windows Azure AD tenant, you will need to add this sample as an pplication to your tenant so that this application can access your tenant information.  In order to do this, we recommend you read: [Learn how to register and integrate an application with Windows Azure AD](http://msdn.microsoft.com/en-us/library/windowsazure/dn151122.aspx) and [Adding, Updating, and Removing an App](http://msdn.microsoft.com/en-us/library/windowsazure/dn132599.aspx). 

***NOTE:***

For this sample to work you will need to specify an **APP URL** of **http://localhost:3000/login/callback** when setting up your applicaiton on the Windows Azure AD Portal.

### Step 3: Download Pre-Requisites for your platform

Java-specific Requisites
* [Java Runtime Environment 7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)* [JBoss 7.1.1.Final](http://www.jboss.org/jbossas/downloads/)* [JBoss Studio 7](https://devstudio.jboss.com/earlyaccess/)
### Step 4: Download the Sample application and update dependencies

From your shell or command line:

* `$ git clone git@github.com:brandwe/azure-sdk-for-java-samples.git`
* `maven install`

### Step 5: Edit web.config and run application


The configuration values you'll need to edit are found in ```web.config ``` and documented in the code. As much as possible they will match the fields in the Azure Management Portal as discussed in [Adding, Updating, and Removing an App](http://msdn.microsoft.com/en-us/library/windowsazure/dn132599.aspx).

After you have configured the correct values, use the process you have established to deploy WAR files in JBoss to run the sample application. If you are unfamilar with JBoss, ***you should use the Java walkthrough here***.

For those familiar with JBoss, here is a refresher to load a client side WAR file:

* Open a new Terminal window
* Copy in the Download folder the WAR from the sample application
* Go to the server folder: `cd ~/Downloads/jboss-as-7.1.1.Final/bin`
* Run the JBoss client to deploy the application: `./jboss-cli.sh`
* Connect to the server: `connect`
* Deploy the application using the the WAR from the sample application in the second step
* Example: `deploy ~/Downloads/sample.war --force`
* Open a browser and navigate [https://localhost:8443/sample/](https://localhost:8443/sample/)