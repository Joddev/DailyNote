### explain

- `id` : 실행 순서
- `select_type` : select type
- `table` : 사용된 table
- `type` : join type
  - `system` : 테이블에 단 하나의 행만 존재
  - `const` : unique key와 상수를 비교할때
  - `ref` : 이전 테이블과의 조인에 사용될 매치되는 인덱스의 모든행이 이 테이블에서 읽혀질 때
  - `range` : 인덱스를 이용하여 주어진 범위 내의 행들만 추출
  - `index` : 인덱스가 스캔
  - `ALL` : 풀 스캔
- `possible_keys` : 사용가능한 index
- `key` : 실제 사용한 index
- `key_len` : 사용한 인덱스의 길이
- `ref` : 행을 추출하는데 사용된 컬림이나 상수값
- `rows` : 예상되는 검색해야할 행수
- `Extra` : 추가 정보
  - `Using filesort` : 추가적인 정렬 필요
  - `range checked for each record` : 마땅한 index가 없음
  - `Using index` : table이 아닌 index tree에서 추출
  - `Using temporary` : 임시 테이블 사용

##### References

- http://greenhappy.tistory.com/entry/MySQL-Explain%EC%8B%A4%ED%96%89%EA%B3%84%ED%9A%8D

### *Union all* VS *Union* VS *Union distinct*

- `union all`과 `union`은 동일한 기능을 수행
- `union distinct`는 동일한 row를 제거 &rarr; unique 과정에서 성능 문제 발생 가능

### where절의 date사용

```mysql
# event_time :=> datetime

/* Duration  / Fetch 
   0.016 sec / 3.375 sec */
SELECT *
FROM 
	customer_event A 
	JOIN customer B ON A.meter_no = B.meter_no
	JOIN meter_log C ON A.meter_no = C.meterNumber AND A.event_time = C.MeteringTime 
WHERE event_type = 5 AND (DATE(event_time) BETWEEN '2018-03-01' AND '2018-03-31')

/* Duration  / Fetch 
   0.016 sec / 0.156 sec */
SELECT *
FROM 
	customer_event A 
	JOIN customer B ON A.meter_no = B.meter_no
	JOIN meter_log C ON A.meter_no = C.meterNumber AND A.event_time = C.MeteringTime 
WHERE event_type = 5 AND (event_time BETWEEN '2018-03-01' AND '2018-03-31')
```

where절에서 데이터 변형에 주의할 것