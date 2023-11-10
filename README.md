# Resource Outputs

**Note To Harsh Sir**: For visibility of the screenshots, kindly consider opening them in a new tab.

## Namespace:
![img](https://i.imgur.com/muvBhpd.png)

| SL | PROJECT    | CLIENT | PROJECT    | APPLICATION_ENVIRONMENT | DATA_CENTER | SETUP_ENVIRONMENT |
|----|------------|--------|------------|--------------------------|-------------|-------------------|
| 1  | eTransport | NIC    | eTransport | checkpost                | dc-Delhi    | Staging           |
| 2  | eTransport | NIC    | eTransport | checkpost                | dc-Delhi    | Staging           |

__________________

## Deployments:
![img](https://i.imgur.com/YLuemH3.png)

| SL | PROJECT    | APP_NAME | OWNER_CONCTACT_DETAIL                | APP_DESCRIPTION            | DEPLOYMENT_DOCUMENT | DOCUMENT_PATH                               | DEPLOYMENT_DOCUMENT_TESTED | PUBLIC_URL                  | BACKUP | BACKUP_URL                              | LAST_BACKUP_DATE | BACKUP_TESTED | BACKUP_TESTED_DATE |
|----|------------|----------|--------------------------------------|-----------------------------|----------------------|---------------------------------------------|-----------------------------|-----------------------------|--------|-----------------------------------------|-------------------|----------------|---------------------|
| 1  | eTransport | App2     | Mr. Avnish avnish@NIC.com 9124233323 | For vehicle tax collection | Yes                  | [Readme.md](https://gitlab.com/checkpostApp2/Readme.md/) | No                          | [checkpost.parivahan.gov.in/](https://gitlab.com/checkpostApp2/backup) | Yes    | [backup](https://gitlab.com/checkpostApp2/backup) | 25-09-2023        | Yes            | 23-09-2023          |
| 2  | eTransport | App1     | Mr. Avnish avnish@NIC.com 9124233323 | For vehicle tax collection | Yes                  | [Readme.md](https://gitlab.com/checkpostApp1/Readme.md/) | No                          | [checkpost.parivahan.gov.in/](https://gitlab.com/checkpostApp1/backup) | Yes    | [backup](https://gitlab.com/checkpostApp1/backup) | 22-09-2023        | No             | N/A                 |

_______________

## Pods:
![img](https://i.imgur.com/On0jj66.png)

| SL | PROJECT    | HOSTNAME  | IP            | APP_NAME | APP_LAUNCH_DATE | LAST_APP_VERSION | GIT_REPO_URL                                | APP_PLATFORM  | PROGRAMMING_LANGUAGE | DEPLOYMENT_DEPENDENCIES | DATABASE | LOCAL_DB_NAME |
|----|------------|-----------|---------------|----------|------------------|------------------|---------------------------------------------|---------------|----------------------|-------------------------|----------|---------------|
| 1  | eTransport | machine1  | 10.249.221.21 | App1     | 03-01-2019       | Version_1        | [checkpostApp1](https://gitlab.com/checkpostApp1) | systemd       | Java                 | Tomcat                  | Postgres | vow4          |
| 2  | eTransport | machine2  | 10.249.221.22 | App2     | 03-01-2019       | Version_2        | [checkpostApp2](https://gitlab.com/checkpostApp2) | containerised | php                  | Tomcat                  | Postgres | vow4          |

__________________________


## Pods -a:
![img](https://i.imgur.com/h3ofiOd.png)

| SL | PROJECT    | HOSTNAME  | IP            | APP_NAME | APP_LAUNCH_DATE | LAST_APP_VERSION | GIT_REPO_URL                                | GIT_ENVIRONMENT | DOCUMENT_TYPE | APP_PLATFORM  | PROGRAMMING_LANGUAGE | PROGRAMMING_LANGUAGE_VERSION | DATABASE | DB_SERVER_READ     | DB_SERVER_WRITE    | LOCAL_DB | LOCAL_DB_NAME | LOCAL_DB_IP | LISTENING_PORT_LOCAL_DB | DEPLOYMENT_DEPENDENCIES |
|----|------------|-----------|---------------|----------|------------------|------------------|---------------------------------------------|-----------------|---------------|---------------|----------------------|-----------------------------|----------|---------------------|---------------------|----------|---------------|-------------|-------------------------|-------------------------|
| 1  | eTransport | machine1  | 10.249.221.21 | App1     | 03-01-2019       | Version_1        | [checkpostApp1](https://gitlab.com/checkpostApp1) | Yes             | Automated     | systemd       | Java                 | 1.8                         | Postgres | 10.246.40.186:5433 | 10.246.40.186:5433 | Yes      | vow4          | 127.0.0.1   | 5439                    | Java                    |
|    |            |           |               |          |                  |                  |                                             |                 |               |               |                      |                             |          | 10.246.40.182:5432 |                     |          |               |             |                         | Tomcat                  |
|    |            |           |               |          |                  |                  |                                             |                 |               |               |                      |                             |          | 10.242.36.129:5432 |                     |          |               |             |                         | CheckpostApp2           |
|    |            |           |               |          |                  |                  |                                             |                 |               |               |                      |                             |          | 10.242.36.130:5432 |                     |          |               |             |                         |                         |
| 2  | eTransport | machine2  | 10.249.221.22 | App2     | 03-01-2019       | Version_2        | [checkpostApp2](https://gitlab.com/checkpostApp2) | Yes             | Manual        | containerised | php                  | 7.2                         | Postgres | 10.246.40.182:5432 | 10.246.40.186:5433 | Yes      | vow4          | 127.0.0.1   | 31                      | Java                    |
|    |            |           |               |          |                  |                  |                                             |                 |               |               |                      |                             |          | 10.242.36.129:5432 |                     |          |               |             |                         | Tomcat                  |
|    |            |           |               |          |                  |                  |                                             |                 |               |               |                      |                             |          | 10.242.36.130:5432 |                     |          |               |             |                         | CheckpostApp1           |

_________________

## Replicaset:
![img](https://i.imgur.com/kBE9Uke.png)

| SL | PROJECT    | HOSTNAME  | IP            | APP_NAME | HAPROXY_RUNNING | HAPROXY_PORT | HLB_IP         | PUBLIC_IP    | PUBLIC_URL                  |
|----|------------|-----------|---------------|----------|-----------------|--------------|----------------|--------------|-----------------------------|
| 1  | eTransport | machine1  | 10.249.221.21 | App1     | Yes             | 80           | 10.249.221.116 | 164.100.69.3 | [checkpost.parivahan.gov.in/](#) |
| 2  | eTransport | machine2  | 10.249.221.22 | App2     | Yes             | 80           | 10.249.221.116 | 164.100.69.3 | [checkpost.parivahan.gov.in/](#) |

_________

## Nodes:
![img](https://i.imgur.com/KmHLIeS.png)

| SL | PROJECT    | HOSTNAME  | IP            | APP_NAME | CPU | RAM  | TYPE     | MAC_ADD           | NETMASK         | OS   | OS_VERSION | KERNEL_VERSION      | OS_SERVICE | GATEWAY         | OS_LAST_PATCHED | NTP_SERVER | VM_HYPERVISOR |
|----|------------|-----------|---------------|----------|-----|------|----------|-------------------|-----------------|------|------------|---------------------|------------|-----------------|------------------|------------|---------------|
| 1  | eTransport | machine1  | 10.249.221.21 | App1     | 8   | 32GB | Physical | 00:00:5e:00:53:af | 255.255.255.128 | RHEL | 7.1        | 4.15.0-46-generic   | master     | 10.249.221.1    | 22-09-2023       | Yes        | N/A           |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | nimbus(contro |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | nimbus(spoole |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | ClMgrS      |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | zabbix_agentd |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | cvd         |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | nimbus(hdb) |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | nimbus(proces |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | nimbus(cdm) |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | cam         |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | nimbus(logmon |                 |                  |            |               |
| 2  | eTransport | machine2  | 10.249.221.22 | App2     | 8   | 64GB | VM       | 00:00:5e:00:53:ac | 255.255.255.128 | RHEL | 7.1        | 5.19.0-46-generic   | Master     | 10.249.221.2    | 25-09-2023       | Yes        | N/A           |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | cvd         |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | nimbus(contro |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | nimbus(spoole |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | cvfwd       |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | zabbix_agentd |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | cvd         |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | nimbus(logmon |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | nimbus(proces |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | cvfwd       |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | nimbus(cdm) |                 |                  |            |               |
|    |            |           |               |          |     |      |          |                   |                 |      |            |                     | cam         |                 |                  |            |               |

_______

## Ingres:
![img](https://i.imgur.com/4xIbDXw.png)

| SL | PROJECT    | HOSTNAME  | IP            | APP_NAME | HAPROXY_RUNNING | HAPROXY_PORT | HLB_IP         | PUBLIC_IP    | PUBLIC_URL                  |
|----|------------|-----------|---------------|----------|-----------------|--------------|----------------|--------------|-----------------------------|
| 1  | eTransport | machine1  | 10.249.221.21 | App1     | Yes             | 80           | 10.249.221.116 | 164.100.69.3 | [checkpost.parivahan.gov.in/](#) |
| 2  | eTransport | machine2  | 10.249.221.22 |

_____________

## PV:
![img](https://i.imgur.com/lIMTEtt.png)

| SL | PROJECT    | HOSTNAME  | IP            | APP_NAME | SAN_DISK  | SAN_PARTITION | LOCAL_DISK | LOCAL_DISK_PARTITION | PV                |
|----|------------|-----------|---------------|----------|-----------|---------------|------------|----------------------|-------------------|
| 1  | eTransport | machine1  | 10.249.221.21 | App1     | sdb:500GB | /u01:322GB    |            | /:20GB               | PV Name=/dev/sda3 |
|    |            |           |               |          |           |               | sda:105GB  | /var:9GB             | PV Size=101.00g   |
|    |            |           |               |          |           |               |            | /home:10GB           | PV Name=/dev/sdb  |
|    |            |           |               |          |           |               |            | /opt:6GB             | PV Size=500.00g   |
|    |            |           |               |          |           |               |            | /tmp:10GB            |                   |
|    |            |           |               |          |           |               |            | /boot:2GB            |                   |
|    |            |           |               |          |           |               |            | /boot/efi:1GB        |                   |
| 2  | eTransport | machine2  | 10.249.221.22 | App2     | sdb:250GB | /u01:322GB    | sda:105GB  | /:20GB               | PV Name=/dev/sda3 |
|    |            |           |               |          |           |               |            | /var:9GB             | PV Size=101.00g   |
|    |            |           |               |          |           |               |            | /home:10GB           | PV Name=/dev/sdb  |
|    |            |           |               |          |           |               |            | /opt:6GB             | PV Size=500.00g   |
|    |            |           |               |          |           |               |            | /tmp:10GB            |                   |
|    |            |           |               |          |           |               |            | /boot:2GB            |                   |
|    |            |           |               |          |           |               |            | /boot/efi:1GB        |                   |

_____________

## PVC:
![img](https://i.imgur.com/UImuooM.png)

| SL | PROJECT    | HOSTNAME  | IP            | APP_NAME | WWNN       | OBJECT_STORAGE        | BUCKET_NAME | VG                        | NFS                 | LVM           |
|----|------------|-----------|---------------|----------|------------|-----------------------|-------------|---------------------------|---------------------|---------------|
| 1  | eTransport | machine1  | 10.249.221.21 | App1     | 32j1wxc231 | objectstorage.nic.com | Check_Post  | /dev/mapper/vg0-lv0:500GB | IP:foldername /u01/ | home          |
|    |            |           |               |          |            |                       |             |                           | nfsstorage          | opt           |
|    |            |           |               |          |            |                       |             |                           |                     | root          |
|    |            |           |               |          |            |                       |             |                           |                     | swap          |
|    |            |           |               |          |            |                       |             |                           |                     | tmp           |
|    |            |           |               |          |            |                       |             |                           |                     | usr           |
|    |            |           |               |          |            |                       |             |                           |                     | var           |
|    |            |           |               |          |            |                       |             |                           |                     | var_log_audit |
|    |            |           |               |          |            |                       |             |                           |                     | lv0           |
| 2  | eTransport | machine2  | 10.249.221.22 | App2     | 45a8abc456 | objectstorage.nic.com | Check_Post  | /dev/mapper/vg0-lv0:500GB | IP:foldername /u01/ | home          |
|    |            |           |               |          |            |                       |             |                           | nfsstorage          | opt           |
|    |            |           |               |          |            |                       |             |                           |                     | root          |
|    |            |           |               |          |            |                       |             |                           |                     | swap          |
|    |            |           |               |          |            |                       |             |                           |                     | tmp           |
|    |            |           |               |          |            |                       |             |                           |                     | usr           |
|    |            |           |               |          |            |                       |             |                           |                     | var           |
|    |            |           |               |          |            |                       |             |                           |                     | var_log_audit |
|    |            |           |               |          |            |                       |             |                           |                     | lv0           |

____________

## Images:
![img](https://i.imgur.com/1Z7UMvP.png)

| SL | PROJECT    | HOSTNAME  | IP            | APP_NAME | APP_PLATFORM  | PROGRAMMING_LANGUAGE | PROGRAMMING_LANGUAGE_VERSION | DEPLOYMENT_DEPENDENCIES |
|----|------------|-----------|---------------|----------|---------------|----------------------|------------------------------|-------------------------|
| 1  | eTransport | machine2  | 10.249.221.22 | App2     | containerised | php                  | 7.2                          | Java                    |
|    |            |           |               |          |               |                      |                              | Tomcat                  |
|    |            |           |               |          |               |                      |                              | CheckpostApp1           |
| 2  | eTransport | machine1  | 10.249.221.21 | App1     | systemd       | Java                 | 1.8                          | Java                    |
|    |            |           |               |          |               |                      |                              | Tomcat                  |
|    |            |           |               |          |               |                      |                              | CheckpostApp2           |

_________________

## CONTAINER:
![img](https://i.imgur.com/eckzqUC.png)

| SL | PROJECT    | HOSTNAME  | IP            | APP_NAME | INTERPRETER_NAME | INSTANCE_NAME       | INSTANCE_PORT | NAME_OF_DEPLOYMENT_FILE | DEPLOYED_FILE_PATH                         | LOG_PATH                            |
|----|------------|-----------|---------------|----------|-------------------|---------------------|---------------|-------------------------|--------------------------------------------|-------------------------------------|
| 1  | eTransport | machine1  | 10.249.221.21 | App1     | Tomcat            | tcat_checkpost_8083 | 8083          | CheckpostApp1.war       | /u01/tcat_checkpost_8083/webapps/           | /u01/tcat_checkpost_8083/logs/      |
|    |            |           |               |          |                   | tcat_checkpost_8084 | 8084          |                         | /u01/tcat_checkpost_8084/webapps/           | /u01/tcat_checkpost_8084/logs/      |
|    |            |           |               |          |                   | tcat_checkpost_8085 | 8085          |                         | /u01/tcat_checkpost_8085/webapps/           | /u01/tcat_checkpost_8085/logs/      |
| 2  | eTransport | machine2  | 10.249.221.22 | App2     | PHP               | tcat_checkpost_8083 | 8083          | CheckpostApp2.war       | /u01/tcat_checkpost_8083/webapps            | /u01/tcat_checkpost_8083/logs            |
|    |            |           |               |          |                   | tcat_checkpost_8084 | 8084          |                         | /u01/tcat_checkpost_8084/webapps            | /u01/tcat_checkpost_8084/logs            |
|    |            |           |               |          |                   | tcat_checkpost_8085 | 8085          |                         | /u01/tcat_checkpost_8085/webapps            | /u01/tcat_checkpost_8085/logs            |

________________________________

## service:
![img](https://i.imgur.com/yYgEF6u.png)

| SL | PROJECT    | HOSTNAME  | IP            | APP_NAME | API_WEBSERVICE_NAME | DATABASE | DB_SERVER_READ     | DB_SERVER_WRITE    | LOCAL_DB_NAME | LOCAL_DB_IP | LISTENING_PORT_LOCAL_DB | OS_SERVICE    |
|----|------------|-----------|---------------|----------|---------------------|----------|--------------------|--------------------|---------------|-------------|-------------------------|---------------|
| 1  | eTransport | machine1  | 10.249.221.21 | App1     | CheckpostWebService | Postgres | 10.246.40.186:5433 | 10.246.40.186:5433 | vow4          | 127.0.0.1   | 5439                    | master        |
|    |            |           |               |          |                     |          | 10.246.40.182:5432 |                    |               |             |                         | cvd           |
|    |            |           |               |          |                     |          | 10.242.36.129:5432 |                    |               |             |                         | nimbus(contro |
|    |            |           |               |          |                     |          | 10.242.36.130:5432 |                    |               |             |                         | nimbus(spoole |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | ClMgrS        |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | zabbix_agentd |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | cvd           |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | nimbus(hdb)   |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | nimbus(proces |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | nimbus(cdm)   |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | cam           |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | nimbus(logmon |
| 2  | eTransport | machine2  | 10.249.221.22 | App2     | Checkpost_API       | Postgres | 10.246.40.182:5432 | 10.246.40.186:5433 | vow4          | 127.0.0.1   | 31                      | Master        |
|    |            |           |               |          |                     |          | 10.242.36.129:5432 |                    |               |             |                         | cvd           |
|    |            |           |               |          |                     |          | 10.242.36.130:5432 |                    |               |             |                         | nimbus(contro |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | nimbus(spoole |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | cvfwd         |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | zabbix_agentd |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | cvd           |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | nimbus(logmon |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | nimbus(proces |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | cvfwd         |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | nimbus(cdm)   |
|    |            |           |               |          |                     |          |                    |                    |               |             |                         | cam           |
___________________________________
