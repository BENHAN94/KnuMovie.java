
# Team12-Phase3

# 제작환경
  - Ubuntu 64-bit 20.04.1
  - Linux x86_64
  - DB using psql(PostgreSQL) 12.4  
  - JDBC 42.2.18 (for PostgreSQL)
  - JDK 11.0.9
가능하시다면 VSCODE를 이용해주시면 감사드리겠습니다.
  VScode for Java
  - extension Java Extension Pack
	  - extension Maven for Java
	  - Ret Hat
	  - Java Test Runner
	  - Project Manager for Java
	  - Debugger for Java
  - pom.xml dependencies->dependency <systemPath>경로 바꾸기
  

# 실행법

1. Team12-Phase3.zip 파일의 압축을 푼다.
2. Eclipse 로 압축을 푼 폴더를 불러온다.
3. KnuMoive.java 에서 11 ~ 13 번 줄을 Phase2.sql이 실행 된 psql 데이터베이스 셋팅에 맞게 수정한다.
   11    public static final String URL = "jdbc:postgresql://localhost:5432/데이터베이스 이름"; 
   12    public static final String USER = "유저 이름"; // USER
   13    public static final String USER_PWD = "해당 유저 비밀번호"; // PWD
4. 수정 후 run을 하면 터미널을 통해 앱을 이용할 수 있다

# 사옹법 및 기능


1. initial Menu
        KNU MOVIE
        ==================
        Menu
        ==================
        1. 로그인
        2. 회원가입
        3. 종료
※1.이 아닌 1을 입력해야한다

 1) 계정이 있을 시 로그인
    - DB에서 Email과 Password 입력
	Email과 Password가 일치 할 경우 
	:로그인 메뉴로 이동
	Email과 Password가 불일치 할 경우
	:에러 메세지

 * 어드민 계정
 email: knu@knu.ac.kr
 password: knu
    
 2) 계정이 없을 시 회원가입
    - DB에서 NOT NULL 속성만 기입
	Email Address(Email_add)
	: "@"의 포함 여부 확인
	First Name(Fname)
	Last Name(Lname)
	Password(Password)
※중복 입력 시 전부 다시 입력해야 한다

 3) Application 종료
    - Application을 종료한다


2. mainMenu( menu after login)
        로그인 완료!
        Knu Movie
        ==================
        MENU
        ==================
        1. 영화 검색
        2. 평가 내역 확인
        3. 회원 정보 수정
        4. 로그아웃
        5. 관리자 모드
        0. 종료
 1) 영화 검색
     - 조건에 따라 영화들을 검색할 수 있는 기능이다
     - 설정 가능한 조건: 제목, 장르, 유형, 개봉 국가, 평균 평가 점수, 개봉 년도, 종영 연도, 배우

      - 영화 검색은 여러 검색 조건을 붙여서 할 수 있다.
      - 예를들어, 장르가 action 이고 한국에서 개봉한 임의의 영화를 찾는다면
        2. 장르 선택으로 들어가 action의 번호 1을 입력한다.
        그리고 4. 개봉 국가 선택으로 들어가 KR을 입력한다.
        조건을 다 설정 하였다면 1. 제목 입력 및 검색으로 들어가 빈칸을 입력한다.

        - 검색 결과는 영상의 제목과 영상의 개봉 날짜가 출력된다.
     
 2) 평가 내역 확인
     - 로그인한 계정이 평가한 영화들의 목록을 볼 수 있다. 

 3) 회원 정보 수정
     - 로그인 한 회원의 정보 수정이 가능하도록 한다
     ※ 100자 이상이거나 형식에 맞지 않을 시 다시 입력

 4) 로그아웃
     - initialMenu로 돌아가는 기능이다

 5) 관리자 모드
     - 영상물을 수정 및 등록할 수 있는 기능이며 권한이 있는 자만 사용이 가능하다

 0) Application 종료

4. adminMenu(관리자 메뉴)
        관리자 메뉴
        ==================
        1. 영상물 등록
        2. 영상물 수정
        3. 평가 내역 확인
        4. 뒤로가기
 1) 영상물 등록
 - 새로운 영상물을 등록
 - Original title, type, 청불 여부를 입력하면 영화를 등록할 수 있다.
 - 나머지 사항은 영상물 수정 기능을 통해 등록할 수 있다.
 - addMovie
        영상물 등록
        ===========================
        Original title을 입력하세요.
        knuMovie

        type을 입력하세요.
        1. Movie
        2. Tv Series
        3. Knu Origianl

        청소년 관람불가 여부를 입력하세요.
        1. 청소년 관람 불가
        0. 청소년 관람 가능
        0
        영화가 등록되었습니다
        Enter를 눌러주세요.

 2) 영상물 수정
    - 등록된 영상물의 제목, 시작 및 종영 연도, 청불 등급, 장르 등을 수정할 수 있다.
    queryMovie -> searchResult -> afterSelectMovie -> updateMovie
 3) 평가 내역 확인
    - 영화별 또는 계정별 평가를 확인할 수 있다.

 4) 뒤로가기

5. ratingLogMenu
        평가 기록
        ====================
        1. 영화별 평가 기록
        2. 회원별 평가 기록
        3. 뒤로가기


# 유의사항
 
 1. DDL 수정 (Team12-Phase2-1.sql 파일 수정)
 : - Rating 테이블에 UNIQUE(mid, uid) 제약조건 추가.
   - 한 계정이 같은 영화를 여러번 평가하는 것을 방지하기 위하여.
   * zip파일 내에 함께 첨부.
   = > Team12-Phase2-1.sql 과 Team12-Phase2-2.sql 를 다시 실행해야 적용 됨





