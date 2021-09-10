## 발견 문제점
## 1. DDL WriteDAO.xml

>**원인** : 60번째 행
```SQL
-- 수정
DELETE FROM test_write WHERE uid = #{uid} == > 
DELETE FROM test_write WHERE wr_uid = #{uid}
```

## 2. updateOk.jsp
>**원인** : 15번째 행
```
-- 수정
location.href = "view.do?uid=${uid}"; ==>
location.href = "view.do?uid=${param.uid}";
```