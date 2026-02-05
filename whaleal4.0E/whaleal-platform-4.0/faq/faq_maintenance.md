# Whaleal Platform (WAP) FAQ – Operations & Cluster Issues

**WAP Version**: 4.0
**Document Type**: Operations FAQ
**Description**: This document summarizes common operational and cluster issues in WAP, including network, node, and cluster runtime problems, with recommended solutions for daily operations and troubleshooting.

---

> **Severity / Impact Scope Definitions**
>
> - **Severity Levels**: Critical, Major, Minor
> - **Impact Scope**: Single Node, Cluster, Full Platform

---

## Q3: VPC Unreachable – MongoDB Nodes Cannot Communicate

**Severity**: Critical
**Impact Scope**: Cluster

**Possible Causes:**

- Incorrect VPC/Subnet configuration
- Security Group not allowing required ports
- Peering not established between different Regions/VPCs

**Recommended Solutions:**

- Ensure MongoDB nodes are in the same VPC or VPC Peering is established
- Verify Security Group rules:
  - MongoDB port (e.g., 27017)
  - Internal communication ports between nodes
- Test connectivity using `telnet` or `nc` between nodes

---

## Q4: Agent Registration Fails

**Severity**: Major
**Impact Scope**: Single Node

**Possible Causes:**

- Agent cannot reach the WAP Server
- Registration port blocked by firewall or Security Group
- Server address configured incorrectly in Agent

**Recommended Solutions:**

- Check the Agent configuration file for correct Server address and port
- Test network connectivity from the Agent node
- Review Agent logs for authentication or network errors

---

## Q5: MongoDB Connection Failure

**Severity**: Critical
**Impact Scope**: Cluster

**Possible Causes:**

- MongoDB service not running
- Incorrect username or password
- Wrong authentication database (`authSource`)
- Network or port not open

**Recommended Solutions:**

* Check MongoDB process status
* ps -ef | grep mongo
* Test connection manually using mongosh
* mongosh "mongodb://{username}:{password}@{host}:{port}/?authSource=admin"
* Verify authentication method and authSource configuration
