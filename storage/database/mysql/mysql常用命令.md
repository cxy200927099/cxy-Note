[TOC]

## mysql常用命令

### 导出数据到文本
```
mysql -u<user> -p<passwd> -h <host> <database> -e "<要执行的sql>" > page_url.txt
```

```
#!/bin/bash

USERNAME="xlFpWriter"
PASSWORD="HyG1TLdut7zH"
DBNAME="XL_VideoDB"
HOST="10.33.16.227"

MYSQL=/usr/bin/mysql

RUN_SQL="$MYSQL -u${USERNAME} -p${PASSWORD} -h ${HOST} ${DBNAME} -e"

echo "=========================show tables"

echo "========================= cnt query_cache_xl"
SQL_STR="select count(1) from query_cache_xl;"
${RUN_SQL} "${SQL_STR}"
echo "========================= cnt query_result"
SQL_STR="select count(1) from query_result;"
${RUN_SQL} "${SQL_STR}"
echo "========================= cnt request_add"
SQL_STR="select count(1) from request_add;"
${RUN_SQL} "${SQL_STR}"
echo "========================= cnt request_query"
SQL_STR="select count(1) from request_query;"
${RUN_SQL} "${SQL_STR}"
echo "========================= cnt request_statics"
SQL_STR="select count(1) from request_statics;"
${RUN_SQL} "${SQL_STR}"
echo "========================= cnt video_fp_xl"
SQL_STR="select count(1) from video_fp_xl;"
${RUN_SQL} "${SQL_STR}"
echo "========================= cnt query_cache_xl"
SQL_STR="select count(1) from video_info_xl;"
${RUN_SQL} "${SQL_STR}"
```



最新解析出来的视频地址一共有97500个，这其中包括一些


