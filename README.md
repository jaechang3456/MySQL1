# MySQL
### 1. MySQL Workbench를 통해, AWS RDS에 접속환경 설정하는 방법
#### AWS RDS에 접속하기 위해서는 아래의 MySQL Workbench 화면에서 더하기 버튼을 클릭합니다.

![1](https://user-images.githubusercontent.com/78472987/111127480-3f279480-85b7-11eb-829e-c1595fc6cf71.PNG)

#### 그 다음 아래화면에서 컨넥션 이름을 지어주고, 호스트네임은 AWS에 오픈한 데이터 베이스 서버에서 가져옵니다.
#### 유저네임도 AWS서버와 동일하게 설정하며, Store in keychain...부분을 눌러 비밀번호를 저장하면, MySQL 사용시 자동 로그인 할수 있습니다.

![image](https://user-images.githubusercontent.com/78472987/111127593-59617280-85b7-11eb-8be7-dd4b7d8cefab.png)

#### 마지막으로, 연결에 성공하면 아래 그림처럼 나오는데, 비밀번호를 저장한 경우 자동으로 실행되고, 아닌경우 AWS에서 만든 RDS서버 보안 비밀번호를 입력하시면 됩니다.

![image](https://user-images.githubusercontent.com/78472987/111127990-c248ea80-85b7-11eb-8784-f78bbfbfabb1.png)
