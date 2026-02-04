# WAP 4.0 User Manual (Full Version)

> This document is intended for end users and provides a complete guide to using Whaleal Platform (WAP 4.0) to build, manage, and maintain MongoDB clusters on AWS from scratch.
> Coverage: **Installation → Project → Cluster → Connection → Monitoring → Diagnostics → Scaling → Backup & Restore → Upgrade Verification**

---

## 1. Deploying WAP (Tokyo Region Example)

1.1 Manually open the following ports in the cloud server security group:

* `80`
* `8080`

1.2 Upload the latest Whaleal Platform installation package to the server directory:

* Target path: `/opt`

1.3 Execute the one-click start command:

<pre class="overflow-visible! px-0!" data-start="714" data-end="749"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(--spacing(9)+var(--header-height))] @w-xl/main:top-9"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre! language-bash"><span><span>sh start.sh <public_IP>
</span></span></code></div></div></pre>

After startup, ensure there are no errors and that the WAP platform is running normally.

---

## 2. Accessing the Platform and First Login

2.1 Open the WAP platform URL in a browser to ensure the page loads correctly.

2.2 Log in using the default administrator account:

* Username: `admin`
* Password: `password`

2.3 Upon first login, the system will require a password change:

* Example new password: `Jinmuinfi.123`

2.4 Log in again using the new password.
2.5 After a successful login, the system will automatically enter the onboarding guide.

---

## 3. Creating a Project

Projects are used to isolate different businesses or environments (e.g., Test / Production).

3.1 Click **Create AWS Project**.
3.2 Fill in the project information (example):

* Project Name: `Tokyo-WAP-Test`
* Member: `admin`
* Region: `ap-northeast-1`
* CIDR: `172.16.160.0/19`

> ⚠️ Tip: When deploying multiple WAP instances under the same AWS account, plan CIDR blocks carefully to avoid network conflicts.

3.3 Once created, go to the Project page and click **Create Cluster** to start the cluster creation process.

---

## 4. Creating a MongoDB Cluster

### 4.0 Configure AWS Credentials (Required)

Path: `Settings → AWS Credentials`

Enter the IAM user information with minimum required permissions:

* Access Key ID: `AKIAxxxx`
* Secret Access Key: `xxxxxxxx`

> If this is not configured, subsequent cluster events, backup, diagnostics, and other features will not work properly.

---

### 4.1 Cluster Creation Parameters

Fill out the creation page as follows:

* Select Project: `Tokyo-WAP-Test`
* Architecture Type: Replica Set
* Select VPC:
  * If the VPC has a Name tag, the name will be displayed
  * If not, the VPC ID will be displayed (this is normal)
* Cluster Name: `Tokyo-WAP-Cluster`

#### MongoDB Version

* Click **Upload MongoDB** to upload the MongoDB installation package
* Select the uploaded version once completed

#### Nodes and Specifications

* Number of Nodes: 3 / 5 / 7 (default: 3 nodes)
* Instance Type: 2C 4GB
* Availability Zones: Single AZ or Multi-AZ (up to 3)
* Storage Type: EBS gp3, default 100GB

#### Auto Scaling (Optional)

* Disabled by default
* When enabled:
  * Evaluates every 12 hours
  * Only supports incremental scaling up

#### MongoDB Authentication Configuration

* Username/password authentication enabled by default
* Example credentials:
  * Username: `admin`
  * Password: `yangshuai123`

Once created, the page will automatically navigate to the MongoDB cluster list.

---

## 4.14 Automated Backend Operations

After clicking **Create Cluster**, WAP automatically performs the following AWS backend operations without user intervention:

1. Automatically create a VPC (skipped if using default VPC)
2. Automatically create 3 subnets (reuse if existing)
3. Automatically create a security group: `wap-SecurityGroup-vpc-id`
   * Automatically syncs WAP Server port rules
4. Automatically generate a key pair: `wap-key-region.pem`
   * Stored on server: `/opt/wap/wap-region/`
   * Also backed up to the S3 bucket created by the platform
5. Automatically configure TGW to enable communication between the WAP Server and VPC internal network
6. Automatically create EC2 instances and deploy MongoDB services
7. Automatically configure S3 Private Endpoint

This is the core value of WAP 4.0: **users can deploy enterprise-level MongoDB without manually configuring AWS infrastructure.**

---

## 5. Connecting to MongoDB Cluster

Path: `Cluster → Operation → Connect`

Supports multiple connection methods and generates them automatically:

* Temporary external connection (quick connect)
* Shell connection
* Java / Python / other language connection strings

Users can directly copy the connection string for use in business systems.

---

## 6. Monitoring

6.1 Navigate to `Cluster → Node Information → Monitor`
6.2 View metrics for each node:

* CPU usage
* Memory usage
* Disk I/O
* Network traffic

6.3 Navigate to `Diagnose → Performance` to view:

* Real-time performance monitoring
* Slow query analysis

---

## 7. Logs and Fault Analysis

7.1 Navigate to `Cluster → Diagnose`
7.2 Open the LogVis page
7.3 Select the cluster and node, then click **Analyse**
7.4 View detailed diagnostic results after analysis

> If AWS credentials were previously configured, S3 storage and analysis environment will be automatically set up, with no additional steps required.

---

## 8. Cluster Scaling

8.1 Navigate to `Cluster → Operation → Scale Up / Scale Down`
8.2 Supports:

* Adjusting instance specifications anytime
* Disk expansion only (cannot shrink)
* Maximum one disk expansion every 6 hours

8.3 Auto Scaling can be enabled or disabled on the page.

---

## 9. Backup & Restore

### 9.1 Creating a Backup Repository

Path: `Backup → Create Repository`

Example parameters:

* Name: `test-backup`
* Cluster: Tokyo-WAP-Cluster
* Backup Frequency: Daily
* Execution Time: UTC 00:00
* Data Retention: 30 days
* Supports selecting databases/tables via regex
* Supports custom backup service memory configuration

The platform backend automatically performs:

* Creation of two backup servers:
  * Permanent node: handles incremental and oplog backups
  * Temporary node: handles full backups and restore tasks
* Each backup resource set supports up to:
  * 4 replica sets, or
  * 1 sharded cluster

Auto-scaling strategy:

* If CPU P80 > 80% during backup, scaling is triggered automatically
* Total daily backup time must not exceed 12 hours

---

### 9.2 Data Restore Capabilities

Supports:

* Restoring to a snapshot time
* Point-in-time restore (PITR)
* Restore to:
  * Original cluster
  * New target cluster

---

## 10. MongoDB Version Upgrade Verification (7.0 → 8.0)

Upgrade verification:

* Uses rolling upgrade mechanism
* Business writes continue uninterrupted
* Client experience remains seamless during upgrade

This demonstrates that WAP's upgrade capability meets production system continuity requirements.

---

## Summary

Through the above process, users can clearly see:

* No need for AWS network or security expertise
* No manual creation of EC2 / VPC / Subnets / Security Groups
* One-click enterprise-level MongoDB cluster deployment
* Built-in monitoring, diagnostics, backup, scaling, and upgrade capabilities

**The core value of WAP 4.0: standardizing, automating, and delivering MongoDB cloud deployment and operations.**
