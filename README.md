# zabbix_template_mysql

| item                           | trigger                                      |
| :----------------------------: | :---------------------------------------------: |
| update operations per second   |                                                 |
| select operations per second   |                                                 |
| slow queries                   |                                                 |
| Threads connected              | MySql threads connected too high on {HOST.NAME} |
| rollback operations per second |                                                 |
| insert operations per second   |                                                 |
| bytes sent per second          |                                                 |
| bytes received per second      |                                                 |
| begin operations per second    |                                                 |
| commit operations per second   |                                                 |
| delete operations per second   |                                                 |
| MySql alive                    | MySql service is down on {HOST.NAME}            |
| Seconds Behind Master          | MySql slave delay is too high on {HOST.NAME}    |
| slave IO is Running            | Mysql Slave IO Status Error on {HOST.NAME}      |
| Slave sql is Running           | Mysql Slave SQL Status Error on {HOST.NAME}     |

适用于zabbix3.4及以上版本,可同时监控mysql status与 mysql slave status, 监控数据的采集也实现并行收集。此监控项目共包含2个文件:

1. userparameter_mysql.conf
2. mysql.xml

其中`userparameter_mysql.conf`需要分发到各个mysql服务器上，`mysql.xml`作为模版文件导入zabbix中。
