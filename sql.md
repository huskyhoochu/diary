# SQL 언어 배우기

### SQL 이란?

> Structured Query Language

SQL은 데이터베이스에 접근하고 처리하게 해주는 언어다.

### SQL의 기능

- 쿼리에 접근하기
- 레코드 삽입하기
- 레코드 업데이트하기
- 레코드 삭제하기
- 새로운 데이터베이스 만들기
- 새로운 데이터베이스 테이블 만들기
- 진행 과정을 저장해두기
- 데이터베이스 뷰를 만들기
- 테이블, 과정, 뷰에 접근하기

SQL은 ANSI(미국 국립 표준 협회) 표준을 따르지만, 언어에 따라 약간의 차이를 보이기도 한다. 하지만 주요 명령어는 모두 동일하다.

- SELECT
- UPDATE
- DELETE
- INSERT
- WHERE

### RDBMS 란?

> Relational Database Management System

RDBM은 관계형 데이터베이스 시스템이다. 오라클, MySQL 등등이 여기 속한다.

RDBM의 데이터는 테이블이라 불리는 데이터베이스 객체에 저장된다. 테이블은 관계형 데이터의 모음이며 이는 열(column)과 행(row)으로 조직된다.

모든 테이블은 필드라고 불리는 엔트리로 쪼개진다. 예를 들어 보여준 "Customer" 테이블은 "CustomerID, CustomerName, ContactName, Address, City, PostalCode, Country"로 나뉜다. 필드는 테이블 안에 있는 하나의 열을 말한다.

하나의 행은 레코드라고 불리는데, 테이블 안에 있는 하나의 개체를 뜻한다. 예시로 든 "Customer" 테이블에는 모두 91개의 레코드가 담겨 있다.

# SQL 문법

### 데이터베이스 테이블

데이터베이스는 하나 이상의 테이블을 갖는다. 각 테이블은 이름으로 구분된다. 테이블은 레코드와 데이터를 갖는다.

### SQL 구문

SQL 구문은 이런 식으로 쓴다.

```
명령어 + FROM <테이블 이름>
```

### 가장 중요한 SQL 명령어

> - SELECT: 데이터베이스에서 데이터를 선택
> - UPDATE: 데이터를 업데이트
> - DELETE: 데이터를 삭제
> - INSERT INTO: 새로운 데이터 삽입
> - CREATE DATABASE: 새로운 데이터베이스 만들기
> - ALTER DATABASE: 데이터베이스 수정
> - CREATE TABLE: 새로운 테이블 만들기
> - ALTER TABLE: 테이블 수정
> - DROP TABLE: 테이블 삭제
> - CREATE INDEX: 인덱스 만들기
> - DROP INDEX: 인덱스 삭제

### SELECT 구문

SELECT 구문은 데이터베이스에서 데이터를 선택할 때 사용한다.

```
SELECT column1, column2, ...
(선택하려는 컬럼)
FROM table_name;
(선택하려는 테이블)
```

만일 전체 컬럼을 선택하려면 `*`를 사용하면 된다.

```
SELECT * FROM table_name;
```

### SELECT DISTINCT 구문

SELECT DISTINCT는 컬럼 안에서 중복되지 않는 값만을 리턴한다.

```
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

SELECT COUNT를 사용하면 컬럼 안에 있는 값을 셀 수 있다. 이를 응용해 보자.

```
SELECT COUNT(DISTINCT Country) FROM Customers;
```
이렇게 하면 Country 컬럼의 중복되지 않는 값의 갯수를 셀 수 있다.

### WHERE 구문

WHERE 구문은 레코드를 필터링할 때 사용한다.

```
SELECT column1, column2, ...
FROM table_name
WHERE <조건문>;
```

예를 들어, Customer 테이블에서 국가가 멕시코인 레코드만 선택해보자.

```
SELECT * FROM Customers
(Customer 테이블에서 전체 컬럼 선택)
WHERE Country='Mexico';
(조건문: 국가= '멕시코'인 레코드만)
```
### WHERE 구문의 연산자

> = : 같다
> <> : 같지 않다 (어떤 SQL에서는 !=으로 쓰기도 한다)
> '>':  크다
> < : 작다
> '>=': 크거나 같다
> <=: 작거나 같다
> BETWEEN: 어떤 범위 사이
> LIKE: 패턴 찾기
> IN: 여러 값을 지정할 때

### 



