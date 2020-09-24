### [DB] Key

---

> Key란? : 검색, 정렬시 Tuple을 구분할 수 있는 기준이 되는 Attribute.

<br>

#### 1. Candidate Key (후보키)

> Tuple을 유일하게 식별하기 위해 사용하는 속성들의 부분 집합. (기본키로 사용할 수 있는 속성들)

2가지 조건 만족

* 유일성 : Key로 하나의 Tuple을 유일하게 식별할 수 있음
* 최소성 : 꼭 필요한 속성으로만 구성

<br>

#### 2. Primary Key (기본키)

> 후보키 중 선택한 Main Key

특징 

* Null 값을 가질 수 없음
* 동일한 값이 중복될 수 없음

<br>

#### 3. Alternate Key (대체키)

> 후보키 중 기본키를 제외한 나머지 키 = 보조키

<br>

#### 4. Super Key (슈퍼키)

> 유일성은 만족하지만, 최소성은 만족하지 못하는 키

<br>

#### Example
| year | month | date | major | minor |
|------|-------|------|-------|-------|
| 2008 | 01    | 13   | 0     | 1     |
| 2008 | 04    | 23   | 0     | 2     |
| 2009 | 11    | 05   | 1     | 0     |
| 2010 | 04    | 05   | 1     | 1     | 

* `(year, major, minor)` and `(year, month, date, major)` can be super key
* `(year, major, minor)` and `(year, month, date, major)` cannot be candidate key
    * `year` can be deleted at first
    * `major` can be deleted at second

*source: https://stackoverflow.com/questions/4519825/what-are-the-differences-between-a-superkey-and-a-candidate-key*
