# Whaleal Changelog



### Whaleal-Platform 1.0.0:

1. **Login Methods**: Supports login via account, email, or phone number.
2. **Password Reset**: Allows password reset through a verification code.
3. **Host and MongoDB Statistics**: Displays host and MongoDB-related statistics.
4. **Host Visualization**: Includes a visual representation of the host list, statistics, and status.
5. **Host Management**: Add and manage new hosts by following the operation guide.
6. **Host Monitoring**: View host details such as basic information, monitoring, logs, commands, and alert statuses.
7. **MongoDB Cluster Management**:
    - View MongoDB cluster information, including nodes, events, logs, and operations.
    - Perform cluster operations: create new clusters, manage, upgrade/downgrade, switch primary and secondary nodes, convert standalone instances to replica sets, enable/disable authentication, view monitoring data, and node logs.
8. **Account Information**: Displays account details and supports password reset.



### Whaleal-Platform 2.0.0:

1. **Bug Fixes**: Resolved known issues, removed redundant files, and optimized agent execution efficiency.
2. **Cluster Optimization**:
    - Standardized cluster display and creation process, ensuring port availability before creation.
    - Added cluster operation locks and the concept of projects, allowing you to organize cluster members.
    - Added support for index creation, read/write preferences, and features like explain and aggregation.
3. **Enhanced Monitoring**: Added more monitoring metrics, improved quantification and home page displays, and added metric comparison capabilities.
4. **Log Optimization**: Resolved abnormal event terminations, added event statuses and waiting information, included operation event group logs, and archived alert information.
5. **Diagnostic Features**:
    - Introduced a new diagnostic function for clusters or individual nodes, displaying results in batches based on the date.
    - Supports periodic inspections, comparing results against reference values, and allows diagnostic log downloads.
6. **Settings Module**: Added a new settings module, including media package management, email configuration, log retention settings, host and MongoDB data collection granularity, and scheduled inspection intervals.
7. **Account Management**: Introduced administrator role permissions, allowing admin control over user permissions, deletion, and password resets.
8. **Notification Feature**: Moved notifications to the left sidebar, enabling filtering and viewing of message information.



### Whaleal-Platform 3.0.0:

1. **New Features**:
    - Added backup functionality, supporting sharded backups.
    - Supports online upgrades and host quota settings.
    - Added data query functionality.
2. **Optimizations**:
    - Improved MongoDB log collection and the alert module.
    - Full internationalization, switching all interfaces to English.
3. **Bug Fixes**: Fixed several known issues, improving system stability.



### Whaleal-Platform 3.0.5:

#### Optimizations:
1. **Operation Confirmation Prompt**: A confirmation dialog appears when clicking restore.
2. **Version Info Display**: AgentJar version info is displayed in host details.
3. **Alert Message Format Improvement**: Alerts now use card format in Lark, Markdown in DingTalk, and HTML in email.
4. **Backup Strategy Optimization**: Displays the `57019` oplog time range in the backup strategy.
5. **Backup Task Continuity**: Backup tasks will automatically resume after a server restart.
6. **Enhanced MongoDB Alerts**: Added alerts for MongoDB cluster node downtime, restarts, and delays.
7. **Audit Enhancement**: Optimized the audit functionality in the MongoDB community edition, expanding its content.
8. **Log Diagnostics Optimization**: Analyzes the top 50,000 slow query entries and regularly deletes outdated data.
9. **Performance Optimization**: Reduced code size and cleared idle states, significantly lowering CPU usage.
10. **New Monitoring Metrics**: Added monitoring and alert configuration for MongoDB replication lag and open cursors.
11. **Maven Dependency Cleanup**: Removed unnecessary Maven dependencies.
12. **Mount Disk Reminder**: Prompt users to mount disks under `/data` when creating MongoDB nodes.
13. **Information Refresh**: MongoDB cluster security-related information can now be refreshed partially.

#### Bug Fixes:
1. **Memory Limit Parameter Fix**: Fixed the issue where modifying the memory limit parameter in backup strategies would fail.
2. **Oplog Data Issue Fix**: Resolved the issue where `57019` oplog data was mistakenly sent to the wrong cluster.
3. **Monitoring Data Fix**: Corrected the absence of monitoring data for `57019` and `47019` nodes.
4. **Task Time Fix**: When the current time exceeds the backup task trigger time by more than a day, the trigger time is automatically adjusted to the next scheduled time.

#### Development:
1. **Upgrade Agent Jar Individually**: Supports the individual upgrade of a specific agent jar.
2. **Backup Compression Package Download**: Supports downloading backup task compression packages when performing restore operations.
3. **Support DDT Log Resume**: Allows resuming DDT log transfers from a breakpoint.
4. **Diagnostic Information Collection**: Collects WAP diagnostic information, including active Host, appDB, and Server logs.
5. **Backup Completion Notification**: Sends a notification via Feishu after completing a backup snapshot.



### Whaleal-Platform 3.0.6:

#### Optimization:

1. **Backup Information Display**: Added detailed snapshot and oplog information in backup strategies with graphical representation.
2. **LogVis Page Improvements**: Enhanced with details like slow queries, error events, and connection information.
3. **Monitoring Metrics Expansion**: Added multiple new alert monitoring metrics covering critical performance indicators.
4. **Alert Information Optimization**: Differentiated between alerts and notifications, providing more detailed alert content.
5. **Enhanced Backup Strategy**: Supports backing up specific `ns` using regex rules.
6. **MongoDB Ownership Management**: Displays managed MongoDB nodes in host information.
7. **Performance Page Redesign**: Added performance data like slow query types, slow query database tables, and current connections.
8. **appDB Sensitive Data Encryption**: Encrypts sensitive information in appDB during storage and transmission.
9. **ExploreData Page Optimization**: Returns `explain` information and displays execution time for each stage.
10. **Custom Cluster Name for Single Node**: Allows custom cluster names when creating single-node clusters.
11. **Startup Script**: Optimized logic for starting WAP Service.
12. **Support Module Refactoring**: Refactored front and back ends, improving backend inspection and analysis.
13. **Setting.Diagnosis Refactoring**: Provides list services for intuitive event group displays.

#### Fixes:

1. **Node 47019 Backup Issue**: Fixed the issue where snapshots on 47019 nodes did not use the same MongoDB version as the source.
2. **Node 57019 Version Fix**: Fixed the issue where 57019 nodes failed to select the correct oplog parser based on the source version when starting DDT.
3. **Optimized ns Table Collection**: Refactored collection logic to support unlimited `ns` tables and allow single `ns` entries to store more data.

#### Development:

1. **Rapid Cluster Deployment**: Supports quick deployment of single-node, replica set, and sharded MongoDB clusters.
2. **Data Migration Support**: Migrates data to WAP's MongoDB clusters using source MongoDB URL information.
3. **ExploreData Metadata Display**: Renders metrics such as disk fragmentation rate, LatencyStats, Cache, and Dirty for `ns`.



### Whaleal Platform 3.0.7:

#### Optimization

1. **Service Information Collection**: Collect comprehensive information from the Service side, including host, JVM, MongoDB, system, and network data, enhancing real-time system monitoring capabilities.
2. **Enhanced MongoDB Audit Content**: Added detailed MongoDB operation audits, covering user actions, database operations, collection operations, and MongoD node activities, strengthening traceability of operation records.
3. **Unified External Service Port (80)**: Leveraged Nginx for service forwarding, standardizing external service access on port 80 to improve user experience.
4. **Abnormal MongoDB Secondary Node Handling**: Introduced intelligent alert mechanisms for abnormal MongoDB secondary nodes, providing timely user notifications and repair suggestions.

#### Bug Fixes

1. **Oplog Replay Frequency Issue**: When backup frequency exceeds one day, users can now customize oplog replay frequency, preventing overload on the DDT node due to excessive one-time oplog replay.
2. **MongoDB 6.0+ Data Recovery Issue**: Added operations to clean up abnormal data in the source cluster during backup recovery, ensuring data integrity and accuracy.
3. **Monitoring Page Data Query and Display Issue**: Optimized frontend and backend query logic to significantly reduce CPU usage, avoiding Service-side exceptions during large-scale data queries.
4. **DDT Log Collection**: Improved handling of abnormal log collection tasks in DDT by skipping problematic logs, ensuring subsequent data collection is unaffected.

#### Development

1. **Backup Console Information Display**: Introduced real-time display of backup tasks, including currently running tasks, tasks waiting for resource allocation, and tasks scheduled for execution in the next 24 hours.
2. **Support for Multiple Object Storage Options**: Added support for various object storage solutions, including GSC (Google Cloud Storage), Alibaba Cloud OSS, Tencent Cloud COS, and Huawei Cloud OBS, catering to diverse storage requirements.
