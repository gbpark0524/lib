[ORACLE](https://github.com/gbpark0524/lib/blob/master/DB/oracle.md)
- id로 접속 및 리스너 확인
```sql
sqlplus id/pw@"service Name"
```
- 컨테이너 상태 확인
```sql
SELECT CON_ID, DBID, NAME, OPEN_MODE FROM V$CONTAINERS ORDER BY 1;
```
- 자동 실행파일 경로
```sql
$ORACLE_HOME/sqlplus/admin/glogin. sql
```
- 표출 표 정렬
```sql
set line 150 pages 5000
col NAME for a10
```
- 컨테이너 변경
```sql
alter session set container=
```
- varchar2 4000byte에서 32767byte로 확장
- Multitenant 컨테이너일 경우 scope=spfile 로 확장
```sql
SHOW PARAMETER max_string_size;
shutdown immediate;
STARTUP UPGRADE;
alter system set max_string_size=EXTENDED;
@?/rdbms/admin/utl32k.sql
```
- 칼럼 찾기
```sql
SELECT DISTINCT TABLE_NAME FROM INFORMATION_SCHEMA.COLUMNS WHERE COLUMN_NAME IN ('컬럼명');
// 오라클
SELECT * FROM ALL_TAB_COLUMNS WHERE COLUMN_NAME LIKE '%%'
```
