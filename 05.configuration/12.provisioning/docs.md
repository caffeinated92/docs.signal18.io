---
title: Provisioning Configuration
---

## Provisioning Settings

Since version 1.1 **replication-manager** can use an agent base cluster provisioning with the OpenSVC provisioning framework.

Starting with version 2.0 provisioning is package in separate binary call **replication-manager-pro**

```
./replication-manager-pro monitor
```

The following software services can be provisioned:

| Item | Docker | Package |
| ---- | ------ | ------- |
| MariaDB | Y   | Y |
| MySQL | Y   | Y |
| Percona | Y   | Y |
| MaxScale | Y   | Y |
| ProxySQL | Y   | N  |
| HaProxy | N   | N  |
| Consul | N  | N  |


**replication-manager** is using a secure client API to an OpenSVC collector and use this collector for posting actions to a cluster of agents, fetch cluster nodes informations and uploading his own set of playbook for provisioning.

 Signal18.io SAS collector can be used for faster testing or not to have to maintain an extra peace of infrastructure, if not possible one need installing an evaluation version of the collector o It can be install colocated to **replication-manager** or install on a separate hardware

 **replication-manager** talk to the default SAS collector or can be setup to talk to on promise collector via following parameters:


 ##### `opensvc-host` (1.1)

 | Item | Value |
 | ---- | ----- |
 | Description | Address of the OpenSVC collector |
 | Type | String |
 | Default | "ci.signal18.io:9443" |
 | Example | "127.0.0.1:443" |

 ##### `opensvc-admin-user` (1.1)

 | Item | Value |
 | ---- | ----- |
 | Description | Admin credential of the OpenSVC collector |
 | Type | String |
 | Default | "root@localhost.localdomain:opensvc" |
 | Example | "root@signa18.io:secret" |

For on promise collector it is needed to make a first register on the collector to create regular  user, group, roles and compliances.

```
replication-manager-pro monitor --opensvc-register
```

For using the SAS monitor you need to login to signal18.io and request for your evaluation or licence account.yalm file. Copy it into the share/opensvc directory of  **replication-manager-pro**

## Services Options

*micro-service* are isolating a collection of resources, each service can than be used for easy management, HA policy like DR plan in agent 1.8 and placement over a cluster on agent version 1.9

  - [x] An existing disk device if none a loopback device to store service data
  - [x] An existing disk device if none a loopback device to store the docker data
  - [x] A file system type zfs|ext4|xfs|hfs|aufs
  - [x] A file system pool type lvm|zpool|none
  - [x] An IP address that need to be unused in the network

Resources choice is uniform over a full cluster.


##### `prov-db-service-type` (1.1)

| Item | Value |
| ---- | ----- |
| Description | Database type of Micro-Services deployment|
| Type | Enum |
| Values | Docker,Package |
| Example | "Docker" |

Type of Micro-Services can be docker or package not that if package it need the package install on the agent as **replication-manager** will only call the binary for bootstrapping and expect it to be present on the agent.    

##### `prov-db-agents` (1.1)

| Item | Value |
| ---- | ----- |
| Description | List of agents for Database Micro-Services placement|
| Type | List |
| Values | Docker,Package |
| Example | "Docker" |

The agent names can be found in the web interface under the agents tab.

## Disk

##### `prov-db-docker-img` (1.1)

| Item | Value |
| ---- | ----- |
| Description | The database docker image to deploy|
| Type | String |
| Example | "mariadb:latest" |


##### `prov-db-disk-fs` (1.1)

| Item | Value |
| ---- | ----- |
| Description | Database type of FS deployment|
| Type | Enum |
| Values | xfs,ext4,zfs,ufs |
| Example | "zfs" |

File system many drivers are available we do test xfs ext4 zfs . Many other drivers like ceph or drbd would need additional testing to be used as extra options may need to be added.

OpenSVC Agent drivers can provision disk resources on many SAN arrays and Cloud API, contact support if you need custom type of disk provisioning for your architecture.

##### `prov-db-disk-pool` (1.1)

| Item | Value |
| ---- | ----- |
| Description | Database disk pool type for Micro Services deployment|
| Type | Enum |
| Values | none,zpool,lvm |
| Example | "zpool" |

##### `prov-db-disk-type` (1.1)

| Item | Value |
| ---- | ----- |
| Description | Database disk pool type for Micro Services deployment|
| Type | Enum |
| Values | loopback,physical|
| Example | "loopback" |

When loopback instead of a real device the FS path is needed instead of device path

##### `prov-db-disk-device` (1.1)

| Item | Value |
| ---- | ----- |
| Description | Database disk device path for Micro Services deployment|
| Type | String |
| Example | "/srv" |

##### `prov-db-disk-size` (1.1)

| Item | Value |
| ---- | ----- |
| Description | Databse disk size in g for micro service VM . |
| Type | String |
| Default | "20g" |
| Example | "20g"  |

## network

Network please check availability of the ip before using them , also some opensvc deployemetn can manage range of dhcp ip and DNS entries   

##### `prov-db-net-iface` (1.1)

| Item | Value |
| ---- | ----- |
| Description | Database ethernet device. |
| Type | String |
| Example | "br0" |

##### `prov0-db-net-gateway` (1.1)

| Item | Value |
| ---- | ----- |
| Description | Database network gateway. |
| Type | String |
| Example | "192.168.1.254" |

##### `prov-db-net-mask` (1.1)

| Item | Value |
| ---- | ----- |
| Description | Database eth device |
| Type | String |
| Example | "255.255.255.0" |

## Resource Usage

Database bootstrap is deploying some database configurations files that are auto adapted to following cluster parameters and to tags:

##### `prov-db-memory` (1.1)

| Item | Value |
| ---- | ----- |
| Description | Database memory in M for micro service. |
| Type | String |
| Example | "256" |

##### `prov-db-disk-iops` (1.1)

| Item | Value |
| ---- | ----- |
| Description | Database Rnd IO/s in for micro service. |
| Type | String |
| Default | "300" |
| Example | "300" |


##### `prov-db-cpu-cores` (2.0)

| Item | Value |
| ---- | ----- |
| Description | Database number of cores for micro service. |
| Type | String |
| Default | "1" |
| Example | "4" |


### Database tags:

##### `prov-db-tags (1.1)`

| Item | Value |
| ---- | ----- |
| Description | Database tags for compliance configuration. |
| Type | String |
|| Example | "innodb,noquerycache,threadpool,logslow" |

Storage:
```
innodb, myrocks, tokudb, spider
```
Logs:
```
logaudit, logslow, logsqlerrors, loggeneral,
```
Features:
```
compress, noquerycache,  threadpool
```
Replication:
```
multidomains, nologslaveupdates, mysqlgtid, smallredolog, wsrep, semisync
```

## Provisioning

Micro services placement will follow a round robin mode against the agents listed for a service.  

bootstap, and unprovision command can be found in the web interface

The client can also be used to provision fully a cluster defined in the configuration.
```
replication-manager-cli bootstrap  --cluster=cluster_haproxy_masterslave --with-provisioning
Provisioning done
```