# Whaleal Platform (WAP) FAQ – Backup & Restore Issues

**WAP Version**: 4.0
**Document Type**: Backup FAQ
**Description**: This document summarizes common issues and recommended solutions related to WAP backup and restore operations, suitable for backup management and data recovery reference.

---

> **Severity / Impact Scope Definitions**
>
> - **Severity Levels**: Critical, Major, Minor
> - **Impact Scope**: Single Node, Cluster, Full Platform

---

## Q7: Backup Task Failure

**Severity**: Major
**Impact Scope**: Cluster

**Possible Causes:**

- Insufficient resources on the DDT Server
- MongoDB account does not have sufficient privileges
- Network interruptions causing data fetch failures

**Recommended Solutions:**

- Review backup task logs to identify the failure stage
- Check DDT Server CPU, memory, and disk utilization
- Ensure the MongoDB user has the required backup privileges

---

## Q8: Restore Task Failure or Incomplete Data

**Severity**: Critical
**Impact Scope**: Cluster

**Possible Causes:**

- Improper selection of restore point
- Missing or non-continuous oplog
- Target cluster does not meet resource requirements

**Recommended Solutions:**

- Verify that both full backups and oplog backups are complete
- Ensure the oplog time range covers the target restore point
- Avoid write operations on the target cluster during the restore task
