### DBMS(데이터베이스 관리 시스템)의 등장 배경

DBMS 이전에 파일시스템으로 데이터를 관리.
##### 파일 시스템의 문제점
- 데이터 중복 시 저장 공간 낭비 및 데이터 일관성과 데이터 무결성을 
  유지하기 어려움
- 데이터 종속성 -> 사용하는 파일의 구조 변경 시 응용프로그램도 함께
  변경해야함
- 동시 공유, 보안, 회복 기능 부족
- 응용 프로그램 개발 어려움

### DBMS의 주요기능
- 정의 기능(DDL) - 구조를 정의하거나 수정
  CREATE, ALTER, DROP, TRUNCATE
- 조작 기능(DML) - 데이터 삽입, 삭제, 수정, 검색 기능
  SELECT, INSERT, UPDATE, DELETE
- 제어 기능(DCL) - 데이터를 정확하고 안전하게 유지
  GRANT, REVOKE, COMMIT, ROLLBACK

### 세대 별 DBMS
- 1세대 DBMS
  네트워크 DBMS - 그래프 형태로 구성
  계층 DBMS - 트리 형태로 구성
- 2세대 DBMS
  관계형 DBMS - 테이블 형태로 구성
		  Ex) Oracle, MySQL, Access, InfoMax
- 3세대 DBMS
  객체지향 DBMS - 객체를 이용해 구성
  객체관계 DBMS - 객체 + 관계
- 4세대 DBMS
  NO SQL , New SQL DBMS - 안정성, 일관성 유지를 위한 복잡한 기능 포기
  