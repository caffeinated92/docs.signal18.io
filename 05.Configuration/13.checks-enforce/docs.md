---
title: Checks & Enforce
---

**replication-manager** enforce best replication and database configuration practice using the following parameters.

##### `force-slave-readonly` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically force READ ONLY on slaves. |
| Type          | Boolean |
| Default Value | true |


##### `force-sync-binlog` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically force master crash safe. |
| Type          | Boolean |
| Default Value | false |

##### `force-sync-innodb` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically force master innodb crash safe. |
| Type          | Boolean |
| Default Value | false |

##### `force-slave-semisync` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically force semi-sync usage. |
| Type          | Boolean |
| Default Value | false |

##### `force-binlog-annotate-embedded` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically activate annotate event allow to print SQL statement on slave using SHOW PROCESSLIST . |
| Type          | Boolean |
| Default Value | false |

##### `force-binlog-checksum` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically force binlog checksum, miss functioning network or inter continental networking can corrupt replication protocol. Checksum detect and repair the protocol by re-transmitting.  |
| Type          | Boolean |
| Default Value | false |

##### `force-binlog-compress` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically force on disk binlog compression on MariaDB 10.2. |
| Type          | Boolean |
| Default Value | false |

##### `force-binlog-row` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically activate binlog row format on master. |
| Type          | Boolean |
| Default Value | false |

##### `force-binlog-slowqueries` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically activate logging of slow query run from replication in slow log. |
| Type          | Boolean |
| Default Value | false |

##### `force-slave-gtid-mode` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically activate gtid mode on slave. |
| Type          | Boolean |
| Default Value | false |

##### `force-slave-no-gtid-mode` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically disable gtid mode on slave. |
| Type          | Boolean |
| Default Value | false |

##### `force-slave-heartbeat` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically activate replication heartbeat on slave. |
| Type          | Boolean |
| Default Value | true |

##### `force-slave-heartbeat-retry` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Replication heartbeat retry on slave. |
| Type          | Integer |
| Default Value | 5 |    

##### `force-slave-heartbeat-time` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Replication heartbeat time. |
| Type          | Integer |
| Default Value | 3 |   


##### `force-noslave-behind` (1.1)

| Item          | Value |
| ----          | ----- |
| Description   | Automatically force no slave behing. |
| Type          | Boolean |
| Default Value | true |