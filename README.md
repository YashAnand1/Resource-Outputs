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



_______

## Ingres:
![img](https://i.imgur.com/4xIbDXw.png)

| SL | PROJECT    | HOSTNAME | IP            | APP_NAME | HAPROXY_RUNNING | HAPROXY_PORT | HLB_IP         | PUBLIC_IP    | PUBLIC_URL                  |
|----|------------|----------|---------------|----------|-----------------|--------------|----------------|--------------|-----------------------------|
| 1  | eTransport | machine1 | 10.249.221.21 | App1     | Yes             | 80           | 10.249.221.116 | 164.100.69.3 | checkpost.parivahan.gov.in/ |
| 2  | eTransport | machine2 | 10.249.221.22 | App2     | Yes             | 80           | 10.249.221.116 | 164.100.69.3 | checkpost.parivahan.gov.in/ |


_____________

## PV:
![img](https://i.imgur.com/lIMTEtt.png)



_____________

## PVC:
![img](https://i.imgur.com/UImuooM.png)

| SL | PROJECT    | HOSTNAME | IP            | APP_NAME | WWNN       | OBJECT_STORAGE        | BUCKET_NAME | VG                        | NFS                 | LVM                                    |
|----|------------|----------|---------------|----------|------------|-----------------------|-------------|---------------------------|---------------------|----------------------------------------|
| 1  | eTransport | machine1 | 10.249.221.21 | App1     | 32j1wxc231 | objectstorage.nic.com | Check_Post  | /dev/mapper/vg0-lv0:500GB | IP:foldername /u01/ | home, opt, root, swap, tmp, usr, var, var_log_audit, lv0 |
| 2  | eTransport | machine2 | 10.249.221.22 | App2     | 45a8abc456 | objectstorage.nic.com | Check_Post  | /dev/mapper/vg0-lv0:500GB | IP:foldername /u01/ | home, opt, root, swap, tmp, usr, var, var_log_audit, lv0 |


____________

## Images:
![img](https://i.imgur.com/1Z7UMvP.png)

| SL | PROJECT    | HOSTNAME | IP            | APP_NAME | APP_PLATFORM  | PROGRAMMING_LANGUAGE | PROGRAMMING_LANGUAGE_VERSION | DEPLOYMENT_DEPENDENCIES                             |
|----|------------|----------|---------------|----------|---------------|-----------------------|-----------------------------|-----------------------------------------------------|
| 1  | eTransport | machine2 | 10.249.221.22 | App2     | containerised | php                   | 7.2                         | Java, Tomcat, CheckpostApp1                           |
| 2  | eTransport | machine1 | 10.249.221.21 | App1     | systemd       | Java                  | 1.8                         | Java, Tomcat, CheckpostApp2                           |


_________________

## CONTAINER:
![img](https://i.imgur.com/eckzqUC.png)

| SL | PROJECT    | HOSTNAME | IP            | APP_NAME | INTERPRETER_NAME | INSTANCE_NAME                                           | INSTANCE_PORT           | NAME_OF_DEPLOYMENT_FILE | DEPLOYED_FILE_PATH                                               | LOG_PATH                                                      |
|----|------------|----------|---------------|----------|------------------|---------------------------------------------------------|-------------------------|-------------------------|------------------------------------------------------------------|---------------------------------------------------------------|
| 1  | eTransport | machine1 | 10.249.221.21 | App1     | Tomcat           | tcat_checkpost_8083<br>tcat_checkpost_8084<br>tcat_checkpost_8085 | 8083<br>8084<br>8085    | CheckpostApp1.war       | /u01/tcat_checkpost_8083/webapps/<br>/u01/tcat_checkpost_8084/webapps/<br>/u01/tcat_checkpost_8085/webapps/ | /u01/tcat_checkpost_8083/logs/<br>/u01/tcat_checkpost_8084/logs/<br>/u01/tcat_checkpost_8085/logs/ |
| 2  | eTransport | machine2 | 10.249.221.22 | App2     | PHP              | tcat_checkpost_8083<br>tcat_checkpost_8084<br>tcat_checkpost_8085 | 8083<br>8084<br>8085    | CheckpostApp2.war       | /u01/tcat_checkpost_8083/webapps<br>/u01/tcat_checkpost_8084/webapps<br>/u01/tcat_checkpost_8085/webapps | /u01/tcat_checkpost_8083/logs<br>/u01/tcat_checkpost_8084/logs<br>/u01/tcat_checkpost_8085/logs |

________________________________

## service:
![img](https://i.imgur.com/yYgEF6u.png)

| SL | PROJECT    | HOSTNAME | IP            | APP_NAME | API_WEBSERVICE_NAME | DATABASE | DB_SERVER_READ     | DB_SERVER_WRITE    | LOCAL_DB_NAME | LOCAL_DB_IP | LISTENING_PORT_LOCAL_DB | OS_SERVICE                                           |
|----|------------|----------|---------------|----------|---------------------|----------|---------------------|---------------------|---------------|-------------|-------------------------|------------------------------------------------------|
| 1  | eTransport | machine1 | 10.249.221.21 | App1     | CheckpostWebService | Postgres | 10.246.40.186:5433 | 10.246.40.186:5433 | vow4          | 127.0.0.1   | 5439                    | master, cvd, nimbus(contro, spoole, hdb, proces, cdm), cam, nimbus(logmon |
| 2  | eTransport | machine2 | 10.249.221.22 | App2     | Checkpost_API       | Postgres | 10.246.40.182:5432 | 10.246.40.186:5433 | vow4          | 127.0.0.1   | 31                      | Master, cvd, nimbus(contro, spoole, cvfwd, zabbix_agentd, logmon, proces, cvfwd, cdm), cam |

___________________________________
