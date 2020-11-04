## Shell

- [sqlplus](https://github.com/gbpark0524/lib/blob/master/DB/sqlplus.md)

- [awk(텍스트 데이터 조작, 검사, 출력)](https://recipes4dev.tistory.com/171)

- [ssd(특정 문자열 찾아서 수정)](https://linuxstory1.tistory.com/entry/SED-%EB%AA%85%EB%A0%B9%EC%96%B4-%EC%82%AC%EC%9A%A9%EB%B2%95)

- [lsof(열려있는, 포트사용하고 있는 파일조회)](https://www.lesstif.com/system-admin/lsof-20776078.html)

- 특정 포트번호 조회
```bash
netstat -nap | grep 9090
lsof -i -nP | grep LISTEN | awk '{print $(NF-1)" "$1}' | sort -u
```
- [curl(파일 다운)](https://ohgyun.com/397)

- [curl](https://m.blog.naver.com/javaking75/220776461230)
- - -

- [정규표현식](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/%EC%A0%95%EA%B7%9C%EC%8B%9D)

- [CentOS에서 부팅시 rc.local실행 안될때](https://stdout.tistory.com/33) - # chmod +x rc.local

- 칼럼찾기
```sql
SELECT DISTINCT TABLE_NAME FROM INFORMATION_SCHEMA.COLUMNS WHERE COLUMN_NAME IN ('컬럼명');
```

