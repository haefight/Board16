## 발견 문제점
## 1.  WriteDAO xml의 view.do의 주소

> **원인** : 파라메터가 안보내짐
```java
com.lec.spring.WriteDTO => com.lec.spring.domain.WriteDTO
```

## 2. 조회수 증가 
> **원인** : 조회수가 안올라감
```java
param0 => param1
```

## 3. /board/updateOk.do 에서 에러발생
> **원인** : uid를 잘못받아옴
```java
view.do?uid=${uid} => view.do?uid=${param.uid}
```

## 4. /board/deleteOk.do 에서 에러발생
> **원인** : 잘못된 경로
```java
WHERE uid = #{uid} => WHERE wr_uid = #{uid}
```
