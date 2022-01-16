### MySQL 



##### SQL : 

##### Structured  구조화된 

##### Query 요청 

##### language  언어



Mysql 설치 해보기 



- 스키마(schema)=데이터베이스 (database)

  서로 연관된 테이블 (표)를 한 곳에 묶으면 그것이 스키마 =데이터베이스라고도 부름 

  (semiproject, finalproject 생각하면 된다)

  서로 연관된 데이터들을 그룹핑해준다. 

  

- 이 모든 것을 그룹핑해주는 것은 데이터베이스 서버 

  마리아DB, 오라클등등이 데이터베이스 서버 (database server)

  

- 데이터베이스 서버 >>>>> 스키마=데이터베이스 >>>>> 테이블(표)

-----

#### 데이터베이스 서버 진입하기

- -uroot           user/root 라는 사용자로 접속하겠다는 뜻 (root 관리자)

- -uroot -p       루트 계정으로 진입 

  비밀번호 치고 들어가면 데이터베이스 서버를 통과한 것 



-------------------------------

#### 데이터베이스 

- CREATE DATABASE 데이터베이스이름;                  데이터베이스 생성
- DROP DATABASE 데이터베이스이름;                     데이터베이스 삭제 



이전 작업 명령어를 호출하고 싶다면 윗쪽 방향키를 누르면 이전에 작성했던 명령어들이 역순으로 나온다. 



- SHOW DATABASES;                             생성된 데이터베이스 조회 



- USE 데이터베이스이름;                       해당 데이터베이스를 사용하기 위해 진입 



----------

#### 표 (table)

- row           행  (데이터의 정보 각 테이블 안에 삽입되는 내부 정보)
- column     열  (데이터의 타입, 타이틀이라 생각하면 쉽다 세로줄의 맨 윗 정보)

| column | column | column |
| :----: | :----: | :----: |
|  row   |  row   |  row   |
|  row   |  row   |  row   |
|  row   |  row   |  row   |



8.1  5:00

---------

#### 테이블의 생성  8.2 

- create table topic (

  no INT(11) not null auto_increment,

  title varchar(100) not null, 

  description text null,

  created datetime not null, 

  author varchar(30) null,

  profile varchar(100) null,

  primary key(no)

  );

mysql이 excel 이랑 다른 점은 컬럼의 데이터 타입을 강제할 수 있다는데 있다. 

- INT vs BIGiNT (빅인트 안 쓰는 이유는 거기까지 쓸 필요가 없기 때문 INT 는 42억까지 커버 가능)
- NOT NULL 은 (값이 없는것을 허용하지 않겠다는 뜻) 
- auto_increment (자동증가: 자동으로 수가 올라가게끔 하는 명령어 )

- varchar 은 (255개의 문자까지만 허용)

- text 는 (6만5천개의 문자까지 허용)

- datetime 은 (날짜와 시간까지 표시됨 2021-12-24 14:15:66)

- primary key 는 (중복되어선 안되는 고유해야하는 값을 지정할때 쓰는 명령어

  예를 들어 순번 ex, no (1,2,3,4))



----------------

#### CRUD  

- 어떠한 컬럼의 값을 보고 싶을때 DESC topic;  이런식으로 치면 해당 정보가 출력된다 



##### create

- insert into topic (title,description) values ('MySQL', 'MySQL is ...', );

  이런식으로 주제등은 , 로  값은 ' ' 로 

  값에서 현재시간 표시는 now() 

- select * from topic;  (topic 테이블의 정보를 불러오는법)



#### read

- select id,title from topic; 특정 주제 추출 코드 

- select id,title,author from topic ` where author='egoing';  `  특정 정보 안 특정 내용 추출 코드 

- select id,title,author from topic ` where author='egoing'` order by id desc;  역순으로 뽑는 코드 

  descending = 큰 숫자가 먼저 나온다 

- select id,title,author from topic ` where author='egoing'` order by id desc `limit 2;` 

  제약을 걸어 전부 말고 몇 가지 정보만 나오게끔하는 코드 



#### update

