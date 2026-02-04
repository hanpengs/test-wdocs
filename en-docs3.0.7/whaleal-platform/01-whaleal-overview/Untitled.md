# Quick Start On Marketplace

## Installation Requirements

Before installing Whaleal Platform (WAP), you must ensure that the Service and Agent meet the necessary software, hardware, network, and port requirements.

### Whaleal Platform

#### Hardware Requirements

**Minimum Requirements:** 8 cores, 16GB of RAM, 500GB disk space.

<table>
  <tr>
    <th>Node Number</th>
    <th>CPU</th>
    <th>Memory</th>
    <th>Disk</th>
  </tr>
  <tr>
    <td>50</td>
    <td>8+</td>
    <td>16GB+</td>
    <td>500GB+additional storage for logs</td>
  </tr>
  <tr>
    <td>200</td>
    <td>16+</td>
    <td>32GB+</td>
    <td>500GB+additional storage for logs</td>
  </tr>
  <tr>
    <td>200+</td>
    <td colspan="3">Please contact the Whaleal Team for specific requirements.</td>
  </tr>
</table>

**Operating System Requirements**

<table>
  <tr>
    <th>Operating System</th>
    <th>Version</th>
    <th>Architecture</th>
  </tr>
  <tr>
    <td>Amazon</td>
    <td>Linux</td>
    <td>2023 x86_64</td>
  </tr>
</table>


#### Software Requirements

**Java Environment Requirements**

<table>
  <tr>
    <th>JAVA</th>
    <th>Version</th>
  </tr>
  <tr>
    <td>open-jdk</td>
    <td>17.0</td>
  </tr>
</table>


#### Network Requirements

**TCP**

Ensure that all Whaleal Platform Application services can communicate effectively over TCP/IP.

* Whaleal Platform Application Database
* Whaleal Platform Application Agent Monitor MongoDB

**Hosts**

To ensure plug-and-play functionality, the Whaleal Platform Server requires the external IP to be open.

**Port**

The Whaleal Platform Application must meet the following basic requirements:

* Users and the Whaleal Platform Application Agent must be able to access via HTTP/HTTPS requests.
* The Whaleal Platform Application must be able to access the Whaleal Platform Application Database.
* All Whaleal Platform Applications and Whaleal Platform Application Agents must be able to access the monitored and managed MongoDB services.
* The Whaleal Platform Application must be able to send information to users via email, DingTalk, Feishu, Webhook.

The Whaleal Platform Application must open the following ports:

<table>
  <tr>
    <th>Service</th>
    <th>Default Port</th>
    <th>Transport</th>
    <th>Direction</th>
  </tr>
  <tr>
    <td>Whaleal Platform</td>
    <td>80</td>
    <td>TCP</td>
    <td>Inbound</td>
  </tr>
</table>



If a custom port is needed, please open the  port.

**Port at host**

The Whaleal Platform Application can complete most operations, but some processes require administrator access to the Whaleal Platform Application host. The following ports must be open:

<table>
  <tr>
    <th>Service</th>
    <th>Default Port</th>
    <th>Transport</th>
    <th>Direction</th>
  </tr>
  <tr>
    <td>ssh</td>
    <td>22</td>
    <td>TCP</td>
    <td>Inbound</td>
  </tr>
</table>


### Whaleal Platform Database

#### Hardware Requirements

Minimum requirement: 2 cores, 4GB RAM

<table>
  <tr>
    <th>Node Number</th>
    <th>CPU</th>
    <th>Memory</th>
    <th>Disk</th>
  </tr>
  <tr>
    <td>50</td>
    <td>4+</td>
    <td>8GB+</td>
    <td>200GB</td>
  </tr>
  <tr>
    <td>200</td>
    <td>8+</td>
    <td>16GB+</td>
    <td>500GB</td>
  </tr>
  <tr>
    <td>200+</td>
    <td colspan="3">Please contact the Whaleal Team for specific requirements.</td>
  </tr>
</table>



For better performance, it is recommended to use:

* SSD for the Application Database disk.
* WiredTiger Storage Engine for the Application Database.

**Operating System Requirements**

<table>
  <tr>
    <th>Operating System</th>
    <th>Version</th>
    <th>Architecture</th>
  </tr>
  <tr>
    <td>Amazon</td>
    <td>2023</td>
    <td>x86_64</td>
  </tr>
</table>


#### Software Requirements

**Java Environment Requirements**

<table>
  <tr>
    <th>JAVA</th>
    <th>Version</th>
  </tr>
  <tr>
    <td>open-jdk</td>
    <td>17.0</td>
  </tr>
</table>


#### Network Requirements

**Port at host**

<table>
  <tr>
    <th>Service</th>
    <th>Default Port</th>
    <th>Transport</th>
    <th>Direction</th>
  </tr>
  <tr>
    <td>MongoDB</td>
    <td>27017</td>
    <td>TCP</td>
    <td>Inbound</td>
  </tr>
</table>


### MongoDB - Agent

#### Hardware Requirements

Minimum: 2 cores, 4GB RAM

**Operating System**

<table>
  <tr>
    <th>Operating System</th>
    <th>Version</th>
    <th>Architecture</th>
  </tr>
  <tr>
    <td>Amazon</td>
    <td>2023</td>
    <td>x86_64</td>
  </tr>
</table>


#### Software Requirements

**Java Environment Requirements**

<table>
  <tr>
    <th>JAVA</th>
    <th>Version</th>
  </tr>
  <tr>
    <td>open-jdk</td>
    <td>17.0</td>
  </tr>
</table>


#### Network Requirements

**Port**

The Whaleal Platform Application Agent must meet the following basic requirements:\

* Users and the Whaleal Platform Application must be able to access the server and MongoDB.
* Therefore, the Whaleal Platform Application must open the following ports:

<table>
  <tr>
    <th>Service</th>
    <th>Default Port</th>
    <th>Transport</th>
    <th>Direction</th>
  </tr>
  <tr>
    <td>MongoDB</td>
    <td>27017</td>
    <td>TCP</td>
    <td>Inbound、Outbound</td>
  </tr>
</table>


​    If a custom port is needed, please open the custom port.

**Port at host**

The Whaleal Platform Application Agent can complete most operations, but some processes require administrator access to the Whaleal Platform Application host. The following ports must be open:

<table>
  <tr>
    <th>Service</th>
    <th>Default Port</th>
    <th>Transport</th>
    <th>Direction</th>
  </tr>
  <tr>
    <td>ssh</td>
    <td>22</td>
    <td>TCP</td>
    <td>Inbound</td>
  </tr>
</table>


### DDT - MongoDB Backup

#### Hardware Requirements

Minimum: 4 cores, 16GB RAM

**Operating System**

<table>
  <tr>
    <th>Operating System</th>
    <th>Version</th>
    <th>Architecture</th>
  </tr>
  <tr>
    <td>Amazon</td>
    <td>2023</td>
    <td>x86_64</td>
  </tr>
</table>


#### Software Requirements

**Java Environment**

<table>
  <tr>
    <th>JAVA</th>
    <th>Version</th>
  </tr>
  <tr>
    <td>open-jdk</td>
    <td>17.0</td>
  </tr>
</table>


#### Network Requirements

**Port**

DDT must meet the following basic requirements:

* DDT service configures ports 47019 and 57019 for MongoDB backup process operation.

DDT must open the following ports:

<table>
  <tr>
    <th>Service</th>
    <th>Default Port</th>
    <th>Transport</th>
    <th>Direction</th>
  </tr>
  <tr>
    <td>MongoDB</td>
    <td>47019</td>
    <td>TCP</td>
    <td>Inbound</td>
  </tr>
  <tr>
    <td>MongoDB</td>
    <td>57019</td>
    <td>TCP</td>
    <td>Inbound</td>
  </tr>
</table>


If a custom port is needed, please open the custom port.

**Port at host**

DDT can complete most operations, but some processes require administrator access to the DDT host. The following ports must be open:

<table>
  <tr>
    <th>Service</th>
    <th>Default Port</th>
    <th>Transport</th>
    <th>Direction</th>
  </tr>
  <tr>
    <td>ssh</td>
    <td>22</td>
    <td>TCP</td>
    <td>Inbound</td>
  </tr>
</table>


## Installation Deployment

### Subscribe to Whaleal Platform Agent

#### Subscription Service

Search for Whaleal Platform Agent in the AWS Marketplace

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 520"></svg>)

Click "Continue to Subscribe" to subscribe to the service.

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/02-subscription-service.png)

Click "Accept Terms" to agree to the service terms.

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/03-subscription-service.png)

Click "Continue to Configuration" to configure.

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 505"></svg>)

Configure instance, version, region, and pricing, among other related information.

![05-configure-this-software](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 706"></svg>)

Click "Continue to Launch" to proceed to the next step.

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/06-continue-to-launch.png)

Select "Launch through EC2" and then click "Launch" to deploy the instance in EC2.

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 1056"></svg>)

#### Instance deployment

Configure instance name

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/08-name-and-tags.png)

Configure instance typeMinimum instance type: 2 cores, 4GB RAM

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1500 382"></svg>)

Configure Key pair

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1490 380"></svg>)

Configure network and ports

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1500 1088"></svg>)

Add storage volume

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1518 344"></svg>)



#### Deploy Appdb MongoDB service (optional)

**The Appdb MongoDB service can be configured manually. If you opt for manual configuration, you can ignore the following steps.**

Automated deployment

Navigate to /opt/ and execute “QuickStart_MongoDB.sh” to quickly start the Appdb MongoDB single-instance service.

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/13-mongo-sh.png)

Record the server IP and MongoDB username and password.

### Subscribe to Whaleal Platform Server

#### Subscribe to the service

Search for Whaleal Platform in the AWS Marketplace

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 589"></svg>)

Click "Continue to Subscribe" to subscribe to the service.

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/15-wap-mongodb-management.png)

Click "Accept Terms" to agree to the service terms.

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/16-limited-offer.png)

Click "Continue to Configuration" to proceed with the setup.

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/17-wap-mongodb-management.png)

Configure instance, version, region, and pricing-related information.

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 698"></svg>)

Click "Continue to Launch" to proceed to the next step.

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/19-wap-mongodb-management.png)

Select "Launch through EC2" and then click "Launch" to deploy the instance in EC2.

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 1044"></svg>)

#### Instance deployment

Configure instance name

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/21-name-and-tags.png)

Configure instance type

Minimum instance type: 8 cores, 16GB RAM, 500GB

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1522 398"></svg>)

Configure key pair

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1490 380"></svg>)

Configure network and ports

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1526 1082"></svg>)

Add storage volume

Minimum requirement: 500GB

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1518 358"></svg>)

#### Whaleal Platform Server Deployment

Confirm that the boot services are starting on the Whaleal Platform servernginx service

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/26-linux-nginx.png)

Java Service

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/27-linux-java.png)

Enter the Whaleal Platform URL in your browser

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1919 990"></svg>)

Click "Next Step" to proceed to the next step
Check whether the server hardware specifications meet the requirements of the Whaleal Platform

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 732"></svg>)

Configure the MongoDB service as outlined in "Appdb MongoDB service deployment"

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 671"></svg>)

Configure the connection for accessing the Whaleal Platform, which can be an IP address or domain name.

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 654"></svg>)

Click "Launch" to deploy the Whaleal Platform service.

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 718"></svg>)

Once the startup is successful, generate the connection URL and display the initial username and password.

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 701"></svg>)

Initial login

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 727"></svg>)

Reset password on first login

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 666"></svg>)

Display the home page upon successful login

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 679"></svg>)

### Deploy single-instance replica set

#### Instance deployment

Create an instance in the subscribed Whaleal Platform Agent

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 780"></svg>)

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 671"></svg>)



Configure instance name

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/39-name-and-tags.png)

Configure instance type

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1482 370"></svg>)

Configure key pair

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1490 380"></svg>)

Configure network and ports

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1508 1076"></svg>)

Add storage volume

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1536 346"></svg>)

#### MongoDB Service Deployment

##### Configure the Agent service

Configure "parameters.properties" in the /opt/agent directory on the Agent server

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/44-linux-pwd.png)

Modify the configuration file URL, placing the Whaleal Platform URL connection after "foreign_url=" and adding port "8080"

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/45-linux-parameters-properties.png)

Check Agent statussystemctl status whaleal_agent

![img](/Users/jinmu/Desktop/whaleal.io文档/whaleal.github.io/en-docs/images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/46-linux-whaleal-agent.png)

All Agent services are stored in the public project of the Whaleal Platform after deployment

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 521"></svg>)

##### Create a custom project

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1002 560"></svg>)

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 459"></svg>)

Move the host from the public project to the custom project

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1434 1508"></svg>)

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1428 1502"></svg>)

View host information

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 462"></svg>)



##### Upload the MongoDB package

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 738"></svg>)

##### Deploy MongoDB Replica Set

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 727"></svg>)

Configure replica set parameters

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 516"></svg>)

Monitor event log progress

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 534"></svg>)

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 579"></svg>)

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 602"></svg>)
Replica Set setup completed

![img](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 493"></svg>)