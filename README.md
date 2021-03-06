### 개발환경   
     스프링 부트 버전 2.3.2  
     자바 버전 8  
     템플릿 엔진 JSP  
     bootstrap  
     의존성  
       -lombok  
       -spring Data JPA  
     DB
       -mysql
     Json통신  
       -query이용(ajax요청)   
### 구현 내용 
#### DB
<img src="https://user-images.githubusercontent.com/61040284/99908604-ee014580-2d26-11eb-8a84-8fef386f6e16.png" width="500" height="350">   

#### 1. 로그인, 회원가입, 회원정보변경   
#### 2. 게시판
      -CRUD
      -본인 글만 삭제,수정
      -댓글, 페이징 처리
#### 3. 스프링 시큐리티 로그인   
     -로그인 안되면 글쓰기 기능 X 로그인 페이지로 이동
     -비밀번호 암호화
     -회원수정 시 강제 세션 부여 
#### 4. 카카오 로그인 Oauth(라이브러리 사용 안하고 직접 구현)  
     -카카오 로그인인지 db에 표시
     -최초로그인 후 로그인 누르면 자동로그인
     1. 웹서버주소
     2. 클라이언트 키 
     3. 카카오 로그인 요청 주소 
     4. 카카오 로그아웃 요청 주소 
     5. 카카오 동의 구성
     User 오브젝트 : id(번호), username, password, email
     카카오로부터 받을 정보 : profile정보(필수), email(선택)
     6. 로그인 요청 주소(GET방식) 
     7. 응답받은 코드  
     8. 토큰 발급 요청 주소(POST방식) - http body에 데이터를 전달 (4가지 데이터)
     9. 토큰을 통한 사용자 정보 조회 (POST)
     
#### 메인화면
<img src="https://user-images.githubusercontent.com/61040284/97426184-71ad5980-1956-11eb-99c1-5bae8296b3be.png">   

#### 로그인, 카카오로그인, 회원가입
<img src="https://user-images.githubusercontent.com/61040284/97847956-be68aa00-1d33-11eb-8840-ccfed98c57cb.png" width="400" height="150">
<img src="https://user-images.githubusercontent.com/61040284/97848130-f7a11a00-1d33-11eb-8b35-63162888c14e.png" width="400" height="400">
<img src="https://user-images.githubusercontent.com/61040284/97427498-fcdb1f00-1957-11eb-9f2a-e31c4dd5ad7b.png" width="400" height="150">   

#### 회원정보수정, 카카오회원정보수정
<img src="https://user-images.githubusercontent.com/61040284/97848808-fc1a0280-1d34-11eb-8bdd-226516b461d7.png" >
<img src="https://user-images.githubusercontent.com/61040284/97848813-fd4b2f80-1d34-11eb-8dda-77155f651a62.png" >   

#### 게시판(댓글)
<img src="https://user-images.githubusercontent.com/61040284/98092365-ed188900-1ec9-11eb-8831-bd4527cca5c5.png">   

#### 글수정
<img src="https://user-images.githubusercontent.com/61040284/97426208-770aa400-1956-11eb-8329-8f8f263095ed.png">
