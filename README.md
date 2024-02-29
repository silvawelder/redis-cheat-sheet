# Redis-cheat-sheet

## Redis Server Commands

### Config commands

List all configurations

```
CONFIG GET *
```
### Users commands

List all users

```
ACL LIST
```
List user current connection

```
ACL WHOAMI
```
## Sentinel commands 

Return the ip and port number of the master with that name. If a failover is in progress or terminated successfully for this master it returns the address and port of the promoted slave..

```
redis-cli -h <pod-dns>.<namespace> -p 26379 --user default --pass '<password>' sentinel get-master-addr-by-name mymaster
```

[1]Redis commands documentation: https://redis.io/commands/

[2]Sentinel documentation:  https://cndoc.github.io/redis-doc-cn/cn/topics/sentinel.html

[3]Redis Server Configuration File: https://redis.io/docs/management/config-file/

[4]Sentinel Configuration File: https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://download.redis.io/redis-stable/sentinel.conf&ved=2ahUKEwj--q7I5MOEAxXHIbkGHSmrA_kQFnoECEsQAQ&usg=AOvVaw0csNhBAzDQSc2pwUoeBVsq
