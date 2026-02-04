# WAP 4.0 Product Introduction

## I. Product Overview

WAP (Whaleal Platform) 4.0 is a next-generation **MongoDB management and data protection platform** designed for enterprise MongoDB database and data asset management scenarios. It provides integrated capabilities including cluster deployment, unified operations management, backup and recovery, disaster recovery protection, data archiving, and security auditing.

Through automation and visualization, WAP significantly reduces the complexity of MongoDB operations, improves system stability, and enhances data security.

Compared with previous versions, WAP 4.0 delivers comprehensive improvements in architectural flexibility, automation, multi-cloud support, and security/compliance capabilities, making it better suited for large-scale, complex production environments that require unified management.

---

## II. Product Positioning

The core positioning of WAP 4.0 is:

> **An automated database management platform for MongoDB**

This is reflected in the following aspects:

1. **Unified Management Platform**  
   Centrally manages MongoDB clusters to provide full visibility of assets, controllable system status, and governed operations.

2. **Automated Operations Platform**  
   Provides standardized deployment, automated inspections, health assessments, alerting, and assisted fault analysis, reducing reliance on individual expertise.

3. **Data Protection and Compliance Platform**  
   Covers backup and recovery, disaster recovery, data archiving, auditing, and access control to help organizations meet security and compliance requirements.

4. **Cloud and Multi-Environment Platform**  
   Supports AWS, public cloud, private cloud, and hybrid cloud environments, adapting to diverse network and architecture scenarios.

---

## III. Use Cases

### 1. Centralized Enterprise MongoDB Management

- Multiple business systems using MongoDB clusters  
- Large numbers of instances distributed across data centers or cloud environments  
- Need for unified asset management, access control, and operational entry points  

### 2. Production Backup and Recovery Assurance

- Core business MongoDB databases requiring scheduled automated backups  
- Support for full and incremental backup strategies  
- Rapid recovery required in the event of accidental deletion, failures, or disasters  

### 3. Disaster Recovery and High Availability

- High requirements for business continuity (finance, government, mission-critical systems)  
- Need for cross–data center and cross–availability zone protection  
- Requirement for regular recovery drills and disaster recovery validation  

### 4. Data Archiving and Storage Cost Optimization

- Continuous growth of MongoDB data and very large online datasets  
- Historical cold data accessed infrequently but must be retained long-term  
- Need to archive cold data to files or low-cost storage to reduce primary cluster load  

### 5. Compliance Auditing and Security Management

- Requirement to record critical MongoDB operation logs  
- Full audit trail for operational activities  
- Compliance with internal controls and regulatory requirements  

---

## IV. Target Users

### 1. Database Administrators (DBAs)

- Responsible for MongoDB deployment, operations, backup, and recovery  
- Use WAP to automate routine operations and reduce operational risk  
- Leverage monitoring and diagnostics for performance tuning and capacity planning  

### 2. Operations Engineers / SREs

- Responsible for overall system stability and availability  
- Use WAP for standardized deployment and cluster management  
- Improve operational efficiency through alerts, inspections, and automation  

### 3. IT Managers / Technical Leaders

- Focused on overall system risk, cost, and compliance  
- Use WAP to gain global visibility and reporting  
- Promote standardized, process-driven, and platform-based operations  

### 4. Development Teams

- Require stable and reliable MongoDB environments  
- Prefer reduced coupling with low-level database operations  
- Use the platform to focus more on business development  

---

## V. Value Summary

- **Cost Reduction and Efficiency Improvement**: Reduces manual operations and improves management efficiency  
- **Improved Stability**: Minimizes human error through standardization and automation  
- **Enhanced Security**: Provides auditing, access control, and data protection  
- **Supports Business Growth**: Platform capabilities support large-scale and multi-cluster expansion  

---

## VI. Key New Features in WAP 4.0 (Compared to Previous Versions)

The major upgrade in WAP 4.0 focuses on **full lifecycle automation for MongoDB in AWS environments**, freeing users from complex cloud infrastructure and database operations to deliver a true out-of-the-box experience.

### 1. One-Click Automated MongoDB Deployment on AWS

The platform can automatically complete the following in AWS environments:

- EC2 instance provisioning  
- VPC and subnet configuration  
- Security group configuration  
- MongoDB cluster deployment and initialization  

Users no longer need to manually create servers or configure complex network parameters.

---

### 2. Fully Automated Backup and Recovery

- Standardized backup policy configuration  
- Automatic provisioning of compute and network resources for backup tasks  
- One-click recovery with automatic deployment of recovery nodes and data restoration  
- Users focus on strategy and outcomes rather than infrastructure preparation  

---

### 3. Intelligent Cluster Capacity Scaling

When cluster capacity or resource utilization reaches predefined thresholds:

- The system automatically evaluates resource requirements using built-in calculation models  
- Automatically upgrades to higher instance specifications  
- Automatically expands storage capacity  

This enables elastic scaling and prevents capacity bottlenecks from impacting business stability.

---

### 4. Extremely Simplified User Experience

Compared to previous versions, WAP 4.0 delivers a significantly redesigned user experience:

- Most low-level operations are fully automated by the platform  
- Substantially fewer configuration parameters  
- Workflows aligned with business semantics (e.g., “Create Cluster”, “Configure Backup Policy”)  
- Evolves from a “professional operations tool” into a “business-friendly database platform”  

---

## VII. Product Scope and Boundary Clarification

To avoid misunderstanding, the functional scope of WAP 4.0 is clearly defined as follows:

- **WAP supports MongoDB only**  
  The platform focuses exclusively on the full lifecycle management of MongoDB, including deployment, operations, backup and recovery, scaling, inspections, and automation.

- **Supports enterprise database needs, but does not provide the database engine itself**  
  WAP provides enterprise-grade management and operational capabilities (such as high availability, data protection, automated delivery, and compliance auditing),  
  but it does not replace or include the MongoDB database engine.

- **Positioning in relation to MongoDB**  
  WAP can be understood as an **enterprise management platform for MongoDB**, designed to:
  - Improve MongoDB availability and stability in production environments  
  - Reduce the barrier to deployment and operations  
  - Provide automation and platform capabilities to support large-scale adoption  
