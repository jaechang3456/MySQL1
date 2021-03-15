# MySQL
### 1. MySQL Workbench를 통해, AWS RDS에 접속환경 설정하는 방법
#### AWS RDS에 접속하기 위해서는 아래의 MySQL Workbench 화면에서 더하기 버튼을 클릭합니다.

![1](https://user-images.githubusercontent.com/78472987/111127480-3f279480-85b7-11eb-829e-c1595fc6cf71.PNG)

#### 그 다음 아래화면에서 컨넥션 이름을 지어주고, 호스트네임은 AWS에 오픈한 데이터 베이스 서버에서 가져옵니다.
#### 유저네임도 AWS서버와 동일하게 설정하며, Store in keychain...부분을 눌러 비밀번호를 저장하면, MySQL 사용시 자동 로그인 할수 있습니다.

![image](https://user-images.githubusercontent.com/78472987/111127593-59617280-85b7-11eb-8be7-dd4b7d8cefab.png)

#### 마지막으로, 연결에 성공하면 아래 그림처럼 나오는데, 비밀번호를 저장한 경우 자동으로 실행되고, 아닌경우 AWS에서 만든 RDS서버 보안 비밀번호를 입력하시면 됩니다.

![image](https://user-images.githubusercontent.com/78472987/111127990-c248ea80-85b7-11eb-8784-f78bbfbfabb1.png)

### 2. MySQL 테이블 생성문 
#### MySQL 테이블 생성문은 간단합니다. 아래와 같이 작성한 후 실행 하면 테이블이 생성됩니다.
create table 테이블 명 (
    컬럼명 데이터 타입,
    컬럼명 데이터 타입,
    ...
    );

### 3. MySQL 테이블에 데이터 insert 하기
#### 데이터 테이블에 값을 넣어주는 insert 또한 간단합니다. 아래와 같이 작성한 후 실행하면, 테이블에 데이터가 들어갑니다.
insert into 테이블명 (컬럼명, 컬럼명) values (값 , 값);

#### 한번에 여러 데이터를 넣고 싶은경우는 아래와 같이 실행 하시면 됩니다.
-- Multiple insert
insert into 테이블명 (컬럼명, 컬럼명) values (값, 값),
									  (컬럼명, 컬럼명) values (값, 값),
									  ... ;
                  
### 4. MySQL 테이블 Select하기
#### 내가 원하는 데이터를 가져오는 방법 : select 컬럼명 from 테이블명 (원하는 테이블의 원하는 컬럼만 가져옴)
#### * : All Columns  ex) select * from 테이블명; 
#### , : 여러개의 컬럼 선택시 사용  ex) select 컬럼명, 컬럼명 from 테이블명;
#### 한개의 컬럼 select 할 시에는 select name(컬럼명) from 테이블명; 처럼 작성합니다.
#### 만약 원하는 조건을 만족하는 값을 가져오고 싶으면 where 컬럼명=값; 을 select 구문 아래 작성시, where 조건에 만족하는 값만 가져옵니다.

### 5. MySQL 테이블에 데이터 update하기
#### update 테이블명 set 컬럼명 = 값
#### where 컬럼명 = 값 ;
#### 위와 같이 작성시, where 조건문 값을 만족하는 컬럼들이, set뒤에 컬럼과 값으로 변환됩니다.

### 6. MySQL 테이블에 데이터 delete 하기
#### delete from 테이블명
#### where 컬럼명 = 값;
위와 같이 작성시, where 조건문을 만족하는 컬럼의 값을 가진 데이터는 삭제 됩니다.

