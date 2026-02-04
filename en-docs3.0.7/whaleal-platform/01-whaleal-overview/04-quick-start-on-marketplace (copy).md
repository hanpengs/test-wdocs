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
    <td>2023x86_64</td>
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

### Subscribe to Whaleal Platform Server

#### Subscribe to the service

Search for Whaleal Platform in the AWS Marketplace

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/14-search-aws-marketplace-products.png)

Click "Continue to Subscribe" to subscribe to the service.

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/15-wap-mongodb-management.png)

Click "Accept Terms" to agree to the service terms.

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/16-limited-offer.png)

Click "Continue to Configuration" to proceed with the setup.

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/17-wap-mongodb-management.png)

Configure instance, version, region, and pricing-related information.

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/18-configure-this-software.png)

Click "Continue to Launch" to proceed to the next step.

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/19-wap-mongodb-management.png)

Select "Launch through EC2" and then click "Launch" to deploy the instance in EC2.

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/20-launch-this-software.png)

#### Instance deployment

Configure instance name

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/21-name-and-tags.png)

Configure instance type

Minimum instance type: 8 cores, 16GB RAM, 500GB

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/22-instance-type.png)

Configure key pair

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/23-key-pair.png)

Configure network and ports

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/24-network-settings.png)

Add storage volume

Minimum requirement: 500GB

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/25-configure-storage.png)

#### Whaleal Platform Server Deployment

Confirm that the boot services are starting on the Whaleal Platform servernginx service

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/26-linux-nginx.png)

Java Service

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/27-linux-java.png)

Enter the Whaleal Platform URL in your browser

![image-20260116152543084](/Users/jinmu/Library/Application Support/typora-user-images/image-20260116152543084.png)

初始密码是admin password

Reset password on first login

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/35-reset-password.png)

Display the home page upon successful login

![image-20260116152818678](/Users/jinmu/Library/Application Support/typora-user-images/image-20260116152818678.png)

关联AWS账号到WAP

![image-20260116153226810](/Users/jinmu/Library/Application Support/typora-user-images/image-20260116153226810.png)

按照步骤创建AWS用户,把密钥信息复制进去点击保存

![image-20260116153904749](/Users/jinmu/Library/Application Support/typora-user-images/image-20260116153904749.png)

### Deploy single-instance replica set

上传MongoDB package,需手动在mongodb官网下载二进制安装包点击*click Upload*上传,注意目前只支持amazon2023系统

![image-20260116155916109](/Users/jinmu/Library/Application Support/typora-user-images/image-20260116155916109.png)



创建Project

![image-20260116154549462](/Users/jinmu/Library/Application Support/typora-user-images/image-20260116154549462.png)



选择你要部署mongodb的地区和CIDR,点击创建

![image-20260116155603157](/Users/jinmu/Library/Application Support/typora-user-images/image-20260116155603157.png)



部署mongodb

![image-20260116154313535](/Users/jinmu/Library/Application Support/typora-user-images/image-20260116154313535.png)



选择配置

Project,选择你创建的Project

VPC,选择VPC,wap-vpc是WAP平台自动创建

Cluster Name,填写您的mongodb 集群名称

MongoDB Version,选择mongodb版本

MongoDB Node,选择集群的节点数

EC2 Type,选择集群的实例类型

Available Zone,实例可用区选择,注意一个集群只能有3个可用区如果节点数超过3个还是会有重复节点分配到一个可用区

Storage,集群存储配置,选择Size,Volume type,IOPS等配置

Auto Scaling,密码设置



![image-20260116160512156](/Users/jinmu/Library/Application Support/typora-user-images/image-20260116160512156.png)









#### Instance deployment

Create an instance in the subscribed Whaleal Platform Agent

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/37-manage-subscriptions.png)

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/38-launch-new-instance.png)



Configure instance name

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/39-name-and-tags.png)

Configure instance type

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/40-instance-type.png)

Configure key pair

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/41-key-pair.png)

Configure network and ports

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/42-network-settings.png)

Add storage volume

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/43-configure-storage.png)

#### MongoDB Service Deployment

##### Configure the Agent service

Configure "parameters.properties" in the /opt/agent directory on the Agent server

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/44-linux-pwd.png)

Modify the configuration file URL, placing the Whaleal Platform URL connection after "foreign_url=" and adding port "8080"

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/45-linux-parameters-properties.png)

Check Agent statussystemctl status whaleal_agent

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/46-linux-whaleal-agent.png)

All Agent services are stored in the public project of the Whaleal Platform after deployment

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/47-wap-project-list.png)

##### Create a custom project

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/48-wap-add-project.png)

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/49-wap-project-list.png)

Move the host from the public project to the custom project

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/50-edit-project.png)

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/51-wap-edit-project.png)

View host information

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/52-wap-host-list.png)



##### Upload the MongoDB package

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/53-wap-mongodb-package.png)

##### Deploy MongoDB Replica Set

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/54-mongodb-list.png)

Configure replica set parameters

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/55-wap-create-replica-set.png)

Monitor event log progress

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/56-wap-event-log.png)

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/57-wap-event-details.png)

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/58-wap-event-details-2.png)
Replica Set setup completed

![img](../../images/whaleal-platform/01-whaleal-overview/04-quick-start-marketplace/59-wap-cluster-information.png)
