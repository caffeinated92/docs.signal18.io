---
title: API Client Usage
taxonomy:
    category: docs
---

## API Clusters

<details>
  <summary>/api/clusters/{clusterName}/status</summary><blockquote>
    
    method  : GET 
    summary : Returns status of cluster.
  
  request:

    url-params: 
      clusterName: string
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type    : application/json
    content	: { "alive": "running" | "errors" }
    
  </blockquote>
  </details>

  <details>
    <summary>400</summary><blockquote> 

    type      : text
    content   : "No cluster found : {clusterName}"

  </blockquote>
  </details>

  </blockquote>
</details>

# Version 2.0 & 2.1

<details>
  <summary>/clusters/{clusterName}/servers/{serverName}/master-status</summary><blockquote>
    
    method  : `GET` 
    summary : Check if server is a master.
  request:

    url-params:  
      clusterName : string 
      serverName  : string
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : text
    content   : "200 -Valid Master!"
    
  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : "No cluster!"

  </blockquote>
  </details>

  <details>
    <summary>503</summary><blockquote> 

    type      : text
    content   : "503 -Not a Valid Master!"

  </blockquote>
  </details>

  </blockquote>
</details>

<details>
  <summary>/clusters/{clusterName}/servers/{serverName}/slave-status</summary><blockquote>
    
    method  : `GET` 
    summary : Check if server is a Slave.
  request:

    url-params:  
      clusterName : string 
      serverName  : string
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : text
    content   : "200 -Valid Slave!"
    
  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : "No cluster!"

  </blockquote>
  </details>

  <details>
    <summary>503</summary><blockquote> 

    type      : text
    content   : "503 -Not a Valid Slave!"

  </blockquote>
  </details>

  </blockquote>
</details>

<details>
  <summary>/clusters/{clusterName}/servers/{serverHost}/{serverPort}/master-status</summary><blockquote>
    
    method  : `GET` 
    summary : Check if server is a master.
  request:

    url-params:  
      clusterName : string 
      serverName  : string
      serverPort  : numeric
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : text
    content   : "200 -Valid Master!"
    
  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : "No cluster!"

  </blockquote>
  </details>

  <details>
    <summary>503</summary><blockquote> 

    type      : text
    content   : "503 -Not a Valid Master!"

  </blockquote>
  </details>

  </blockquote>
</details>

<details>
  <summary>/clusters/{clusterName}/servers/{serverHost}/{serverPort}/slave-status</summary><blockquote>
    
    method  : `GET` 
    summary : Check if server is a slave.
  request:

    url-params:  
      clusterName : string 
      serverName  : string
      serverPort  : numeric
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : text
    content   : "200 -Valid Slave!"
    
  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : "No cluster!"

  </blockquote>
  </details>

  <details>
    <summary>503</summary><blockquote> 

    type      : text
    content   : "503 -Not a Valid Slave!"

  </blockquote>
  </details>

  </blockquote>
</details>

# Version	2.1

<details>
  <summary>/clusters/{clusterName}/servers/{serverName}/is-master</summary><blockquote>
    
    method  : `GET` 
    summary : Check if server is a master.
  request:

    url-params:  
      clusterName : string 
      serverName  : string
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : text
    content   : "200 -Valid Master!"
    
  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : "No cluster!"

  </blockquote>
  </details>

  <details>
    <summary>503</summary><blockquote> 

    type      : text
    content   : "503 -Not a Valid Master!"

  </blockquote>
  </details>

  </blockquote>
</details>

<details>
  <summary>/clusters/{clusterName}/servers/{serverName}/is-slave</summary><blockquote>
    
    method  : `GET` 
    summary : Check if server is a Slave.
  request:

    url-params:  
      clusterName : string 
      serverName  : string
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : text
    content   : "200 -Valid Slave!"
    
  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : "No cluster!"

  </blockquote>
  </details>

  <details>
    <summary>503</summary><blockquote> 

    type      : text
    content   : "503 -Not a Valid Slave!"

  </blockquote>
  </details>

  </blockquote>
</details>

<details>
  <summary>/clusters/{clusterName}/servers/{serverHost}/{serverPort}/is-master</summary><blockquote>
    
    method  : `GET` 
    summary : Check if server is a master.
  request:

    url-params:  
      clusterName : string 
      serverName  : string
      serverPort  : numeric
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : text
    content   : "200 -Valid Master!"
    
  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : "No cluster!"

  </blockquote>
  </details>

  <details>
    <summary>503</summary><blockquote> 

    type      : text
    content   : "503 -Not a Valid Master!"

  </blockquote>
  </details>

  </blockquote>
</details>

<details>
  <summary>/clusters/{clusterName}/servers/{serverHost}/{serverPort}/is-slave</summary><blockquote>
    
    method  : `GET` 
    summary : Check if server is a slave.
  request:

    url-params:  
      clusterName : string 
      serverName  : string
      serverPort  : numeric
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : text
    content   : "200 -Valid Slave!"
    
  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : "No cluster!"

  </blockquote>
  </details>

  <details>
    <summary>503</summary><blockquote> 

    type      : text
    content   : "503 -Not a Valid Slave!"

  </blockquote>
  </details>

  </blockquote>
</details>

### API Protected Endpoints

<details>
  <summary>/api/monitor</summary><blockquote>
    
    method  : `GET` 
    summary : Get monitoring data and configs.
  request:

    url-params: none
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : application/json
    content   : 
      {
        "version"                   : string,
        "fullVersion"               : string,
        "os"                        : string,
        "arch"                      : string,
        "memprofile"                : string,
        "cpuprofile"                : string,
        "agents"                    : null,
        "uuid"                      : string,
        "hostname"                  : string,
        "status"                    : "A" | "S",
        "spitBrain"                 : bool,
        "clusters"                  : []string,
        "tests"                     : []string,
        "config"                    : {}Config,
        "logs"                      : {
                                      "buffer"  : []{
                                                    "group": string,
                                                    "level": string,
                                                    "timestamp": string("yyyy/mm/dd hh:mm:ss"),
                                                    "text": string
                                                  },
                                      "len"     : integer,
                                      "line"    : integer
                                    },
        "servicePlans"              : null,
        "serviceOrchestrators"      : []{
                                        "id": integer,
                                        "name": "opensvc" | "kube" | "slapos" | "local" | "onpremise",
                                        "available": bool,
                                        "label": string
                                      },
        "serviceAcl"                : []{
                                        "grant": string,
                                        "enable": bool
                                      },
        "serviceRepos"              : []{
                                        "name": string,
                                        "image": string,
                                        "tags": {
                                          "results" : []{ "name": string }
                                        }
                                      },
        "serviceTarballs"           : []{
                                        "name": string,
                                        "OS": string,
                                        "url": string,
                                        "flavor": string,
                                        "minimal": bool,
                                        "size": integer,
                                        "short_version": "3.0",
                                        "version": "3.0.0",
                                        "notes": string
                                      },
        "serviceFS"                 : {
                                        "aufs": bool,
                                        "ext4": bool,
                                        "nfs": bool,
                                        "xfs": bool,
                                        "zfs": bool
                                      },
        "serviceVM"                 : {
                                        "docker": bool,
                                        "kvm": bool,
                                        "lxc": bool,
                                        "oci": bool,
                                        "package": bool,
                                        "podman": bool,
                                        "zone": bool
                                      },
        "serviceDisk"               : {
                                        "directory": "directory",
                                        "loopback": "loopback",
                                        "physical": "physical",
                                        "pool": "pool",
                                        "volume": "volume"
                                      },
        "servicePool"               : {
                                        "lvm": bool,
                                        "none": bool,
                                        "zpool": bool
                                      },
        "backupLogicalList"         : {
                                        "dumpling": bool,
                                        "internal": bool,
                                        "mydumper": bool,
                                        "mysqldump": bool
                                      },
        "backupPhysicalList"        : {
                                        "mariabackup": bool,
                                        "xtrabackup": bool
                                      },
        "Confs"                     : map[{cluster}]{}Config,
      }
    
  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : string

  </blockquote>
  </details>

  </blockquote>
</details>

## Cluster Protected Endpoint

### 2.0

<details>
  <summary>/api/clusters/{clusterName}</summary><blockquote>
    
    method  : `GET` 
    summary : Get single cluster data.
  request:

    url-params:  
      clusterName : string
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : application/json
    content   : 
    {
      "name"                          : string,
      "tenant"                        : string,
      "workingDir"                    : string,
      "dbServers"                     : []string,
      "dbServersCrashes"              : null,
      "proxyServers"                  : []string,
      "failoverCounter"               : integer,
      "failoverLastTime"              : integer,
      "activePassiveStatus"           : "A" | "S",
      "isSplitBrain"                  : bool,
      "isFailedArbitrator"            : bool,
      "isLostMajority"                : bool,
      "isDown"                        : bool,
      "isClusterDown"                 : bool,
      "isAllDbUp"                     : bool,
      "isFailable"                    : bool,
      "isPostgres"                    : bool,
      "isProvision"                   : bool,
      "isNeedProxyRestart"            : bool,
      "isNeedProxiesRestart"          : bool,
      "isNeedDatabasesRestart"        : bool,
      "isNeedDatabasesRollingRestart" : bool,
      "isNeedDatabasesRollingReprov"  : bool,
      "isNeedDatabasesReprov"         : bool,
      "isValidBackup"                 : bool,
      "isNotMonitoring"               : bool,
      "isCapturing"                   : bool,
      "isGitPull"                     : bool,
      "isAlertDisable"                : bool,
      "config"                        : {}Config,
      "cleanReplication"              : bool,
      "topology"                      : string,
      "uptime"                        : number,
      "uptimeFailable"                : number,
      "uptimeSemisync"                : number,
      "monitorSpin"                   : numeric,
      "workLoad"                      : {
                                          "dbTableSize": integer,
                                          "dbIndexSize": integer,
                                          "connections": integer,
                                          "qps": integer,
                                          "cpuThreadPool": integer,
                                          "cpuUserStats": integer,
                                          "BusyTime": string
                                        },
      "log"                           : {
                                          "buffer"  : []{
                                                        "group": string,
                                                        "level": string,
                                                        "timestamp": string("yyyy/mm/dd hh:mm:ss"),
                                                        "text": string
                                                      },
                                          "len"     : integer,
                                          "line"    : integer
                                        },
      "jobResults"                    : {},
      "sqlGeneralLog"                 : {
                                          "buffer": null,
                                          "len": 0,
                                          "line": 0
                                        },
      "sqlErrorLog"                   : {
                                          "buffer": null,
                                          "len": 0,
                                          "line": 0
                                        },
      "monitorType"                   : map[string]( "proxy" | "database" )
      "topologyType"                  : map[string]string,
      "fsType"                        : {
                                          "aufs": bool,
                                          "ext4": bool,
                                          "nfs": bool,
                                          "xfs": bool,
                                          "zfs": bool
                                        },
      "diskType"                      : {
                                          "directory": "directory",
                                          "loopback": "loopback",
                                          "physical": "physical",
                                          "pool": "pool",
                                          "volume": "volume"
                                        },
      "vmType"                        : {
                                          "docker": bool,
                                          "kvm": bool,
                                          "lxc": bool,
                                          "oci": bool,
                                          "package": bool,
                                          "podman": bool,
                                          "zone": bool
                                        },
      "agents"                        : null,
      "stateMachine"                  : {
                                          "discovered": true,
                                          "inFailover": false,
                                          "inSchemaMonitor": false
                                        },
      "haveDBTLSCert"                 : false,
      "haveDBTLSOldCert"              : false,
      "slaHistory"                    : null,
      "apiUsers"                      : map[string]{
                                          "user": string,
                                          "grants": map[string]bool
                                        },
      "waitingRejoin"                 : 0,
      "waitingSwitchover"             : 0,
      "waitingFailover"               : 0,
      "configurator"                  : {
                                          "configTags": []{
                                              "id": integer,
                                              "name": string,
                                              "category": string
                                            },
                                          "configPrxTags": []{
                                              "id": integer,
                                              "name": string
                                            },
                                          "dbServersTags": []string,
                                          "proxyServersTags": []string
                                        },
      "diffVariables"                 : []{
                                          "variableName": string,
                                          "diffValues": []{
                                              "serverName": string,
                                              "variableValue": string
                                            },
                                        },
      "canInitNodes"                  : bool,
      "canConnectVault"               : bool,
      "sstAvailablePorts"             : map[string]string,
      "LastDelayStatPrint"            : datetime,
      "SlavesOldestMasterFile"        : {
                                          "Prefix": string,
                                          "Suffix": integer,
                                          "OldestTimestamp": datetime
                                        },
      "SlavesConnected"               : integer
    }
    
  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : string

  </blockquote>
  </details>

  </blockquote>
</details>

<details>
  <summary>/api/clusters/{clusterName}/settings</summary><blockquote>
    
    method  : `GET` 
    summary : Get cluster configuration.
  request:

    url-params:  
      clusterName : string
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : application/json
    content   : {}Config
    
  </blockquote>
  </details>

  <details>
    <summary>403</summary><blockquote> 

    type      : text
    content   : "No valid ACL"

  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : string

  </blockquote>
  </details>

  </blockquote>
</details>

<details>
  <summary>/api/clusters/{clusterName}/actions/switchover</summary><blockquote>
    
    method      : `GET` 
    summary     : Initiate switchover to the most suitable slave for new master.
    description : Will only send http-200 code. If no valid acl will return 403 and 400 if master in failed status.
  request:

    url-params:  
      clusterName : string
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : 
    content   : 
    
  </blockquote>
  </details>

  <details>
    <summary>400</summary><blockquote> 

    type      : text
    content   : "Master failed"

  </blockquote>
  </details>

  <details>
    <summary>403</summary><blockquote> 

    type      : text
    content   : "No valid ACL"

  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : "No Cluster"

  </blockquote>
  </details>

  </blockquote>
</details>

<details>
  <summary>/api/clusters/{clusterName}/actions/failover</summary><blockquote>
    
    method      : `GET` 
    summary     : Initiate manual failover to the most suitable slave for new master.
    description : Will only send http-200 code. If no valid acl will return 403 and 500 if cluster not found.

  request:

    url-params:  
      clusterName : string
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : 
    content   : 
    
  </blockquote>
  </details>

  <details>
    <summary>403</summary><blockquote> 

    type      : text
    content   : "No valid ACL"

  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : "No Cluster"

  </blockquote>
  </details>

  </blockquote>
</details>



<details>
  <summary>/api/clusters/{clusterName}/actions/replication/bootstrap/{topology}</summary><blockquote>
  
  #### WARNING! THIS API WILL REMOVE YOUR CURRENT REPLICATION AND RESET MASTER BINARY LOG!
    
    method      : `GET` 
    summary     : Initiate replication bootstrap based on topology list.

  request:

    url-params:  
      clusterName : string
      topology : string
    
  responses:
  <details>
    <summary>200</summary><blockquote>
      
    type      : 
    content   : 
    
  </blockquote>
  </details>

  <details>
    <summary>403</summary><blockquote> 

    type      : text
    content   : "No valid ACL"

  </blockquote>
  </details>

  <details>
    <summary>500</summary><blockquote> 

    type      : text
    content   : "No Cluster"

  </blockquote>
  </details>

  </blockquote>
</details>


/api/clusters/{clusterName}/actions/replication/cleanup

/api/clusters/{clusterName}/actions/services todo
List agents services resources

/api/clusters/{clusterName}/actions/services/provision

/api/clusters/{clusterName}/actions/services/bootstrap

/api/clusters/{clusterName}/actions/start-traffic

/api/clusters/{clusterName}/actions/stop-traffic


/api/clusters/{clusterName}/actions/addserver/{host}/{port}

/api/clusters/{clusterName}/topology/servers

/api/clusters/{clusterName}/topology/master

/api/clusters/{clusterName}/topology/slaves

/api/clusters/{clusterName}/topology/proxies

/api/clusters/{clusterName}/topology/logs

/api/clusters/{clusterName}/topology/alerts

/api/clusters/{clusterName}/topology/crashes

/api/clusters/{clusterName}/tests

/api/clusters/{clusterName}/tests/actions/run/{testName}

/api/clusters/{clusterName}/settings

/api/clusters/{clusterName}/settings/reload

/api/clusters/{clusterName}/settings/switch/{parmaterName}

## 2.1

/api/clusters/{clusterName}/actions/master-physical-backup

## Database Server Protected Endpoint

### 2.0

/api/clusters/{clusterName}/servers/{serverName}/actions/start

/api/clusters/{clusterName}/servers/{serverName}/actions/stop

/api/clusters/{clusterName}/servers/{serverName}/actions/backup

/api/clusters/{clusterName}/servers/{serverName}/actions/maintenance

/api/clusters/{clusterName}/servers/{serverName}/actions/unprovision

/api/clusters/{clusterName}/servers/{serverName}/actions/provision

### 2.1

/api/clusters/{clusterName}/servers/{serverName}/actions/optimize

/api/clusters/{clusterName}/servers/{serverName}/actions/backup-physical
Post an event into replication_manager_schema.jobs for cron processing

/api/clusters/{clusterName}/servers/{serverName}/actions/backup-logical
Post an event into replication_manager_schema.jobs for cron processing

/api/clusters/{clusterName}/servers/{serverName}/actions/backup-error-log
Post an event into replication_manager_schema.jobs for cron processing

/api/clusters/{clusterName}/servers/{serverName}/actions/backup-slow-query-log
Post an event into replication_manager_schema.jobs for cron processing

/api/clusters/{clusterName}/servers/{serverName}/actions/reseed/{backupMethod}

/api/clusters/{clusterName}/servers/{serverName}/actions/toogle-innodb-monitor

/api/clusters/{clusterName}/servers/{serverName}/actions/toogle-slow-query

/api/clusters/{clusterName}/servers/{serverName}/actions/toogle-slow-query-capture

/api/clusters/{clusterName}/servers/{serverName}/actions/toogle-slow-query

/api/clusters/{clusterName}/servers/{serverName}/actions/toogle-read-only

/api/clusters/{clusterName}/servers/{serverName}/actions/reset-master

/api/clusters/{clusterName}/servers/{serverName}/actions/start-slave

/api/clusters/{clusterName}/servers/{serverName}/actionsskip-replication-event

/api/clusters/{clusterName}/servers/{serverName}/processlist

/api/clusters/{clusterName}/servers/{serverName}/variables

/api/clusters/{clusterName}/servers/{serverName}/status

/api/clusters/{clusterName}/servers/{serverName}/status-delta

/api/clusters/{clusterName}/servers/{serverName}/status-innodb

/api/clusters/{clusterName}/servers/{serverName}/errorlog

/api/clusters/{clusterName}/servers/{serverName}/slowlog

/api/clusters/{clusterName}/servers/{serverName}/tables

/api/clusters/{clusterName}/servers/{serverName}/vtables

/api/clusters/{clusterName}/servers/{serverName}/schemas

/api/clusters/{clusterName}/servers/{serverName}/all-slaves-status

/api/clusters/{clusterName}/servers/{serverName}/master-status

/api/clusters/{clusterName}/servers/{serverName}/is-master

/api/clusters/{clusterName}/servers/{serverName}/is-slave

/api/clusters/{clusterName}/servers/{serverName}/{serverPort}/is-master

/api/clusters/{clusterName}/servers/{serverName}/{serverPort}/is-slave

/api/clusters/{clusterName}/servers/{serverName}/service-opensvc


## Proxy Protected Endpoint

/api/clusters/{clusterName}/proxies/{proxyName}/actions/unprovision

/api/clusters/{clusterName}/proxies/{proxyName}/actions/provision
