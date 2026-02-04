# Whaleal Platform (WAP) FAQ – Installation Issues

**WAP Version**: 4.0
**Document Type**: Installation FAQ
**Description**: This document summarizes common installation issues and recommended solutions for WAP. It is intended for deployment and early-stage operations reference.

---

> **Severity / Impact Scope Definitions**
>
> - **Severity Levels**: Critical, Major, Minor
> - **Impact Scope**: Single Node, Cluster, Full Platform

---

## Q1: WAP Services Fail to Start After Installation

**Severity**: Critical
**Impact Scope**: Full Platform

**Possible Causes:**

- Java environment is not installed correctly or the version is incompatible
- Dependency components (Nacos / MongoDB / Nginx) are not running properly
- Configuration file parameters are incorrect (port conflicts, path errors)

**Recommended Solutions:**

```bash

# Check Java version
java -version
# Ensure it meets WAP requirements (Java 17)

# Check service status
ps -ef | grep nacos
ps -ef | grep ops-gateway
ps -ef | grep ops-server-web
ps -ef | grep data-collection
ps -ef | grep nginx

# Review each service's startup logs to locate specific errors
Q2: Missing Dependencies or Components Not Installed

Severity: Major
Impact Scope: Full Platform

Possible Causes:

Installation environment is a clean system with necessary dependencies not pre-installed

Installation script was interrupted or did not execute completely

Recommended Solutions:

Ensure the following components are installed:

Java

sysstat (iostat)

numactl

Re-run the dependency check script or the full installation script to ensure all components are installed correctly.
```


## Q2: Missing Dependencies or Components Not Installed

**Severity**: Major
**Impact Scope**: Full Platform

**Possible Causes:**

* Installation environment is a clean system with necessary dependencies not pre-installed
* Installation script was interrupted or did not execute completely

**Recommended Solutions:**

1. Ensure the following components are installed:
   * Java
   * sysstat (iostat)
   * numactl
2. Re-run the dependency check script or the full installation script to ensure all components are installed correctly.

<pre class="overflow-visible! px-0!" data-start="1696" data-end="1699" data-is-last-node=""><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(var(--sticky-padding-top)+9*var(--spacing))]"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"></div></div></pre>
