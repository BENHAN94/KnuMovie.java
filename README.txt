# 제작환경
  - DB using psql(PostgreSQL) 12.4  
  - JDBC 42.2.18
  - JDK 11.0.9

VScode for Java
  - extension Java Extension Pack
  - extension Maven for Java
  - Ret Hat
  - Java Test Runner
  - Project Manager for Java
  - Debugger for Java
  - pom.xml dependencies->dependency <systemPath>경로 바꾸기

# 실행 및 사용법
※1.이 아닌 1을 입력해야한다
1. initial Menu
        KNU MOVIE
        ==================
        Menu
        ==================
        1. 로그인
        2. 회원가입
        3. 종료
 1) 계정이 있을 시 로그인
    - DB에서 Email과 Password 입력
	Email과 Password가 일치 할 경우 
	:로그인 메뉴로 이동
	Email과 Password가 불일치 할 경우
	:에러 메세지
 2) 계정이 없을 시 회원가입
    - DB에서 NOT NULL 속성만 기입
	Email Address(Email_add)
	: "@"의 포함 여부 확인
	First Name(Fname)
	Last Name(Lname)
	Password(Password)
	SID(sid)
※중복 입력 시 전부 다시 입력해야 합니다
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
       ※조건 중 평가는 최소점수 및 최대점수로 입력
 2) 회원 정보 수정
     - 로그인 한 회원의 정보 수정이 가능하도록 한다
     ※ 100자 이상이거나 형식에 맞지 않을 시 다시 입력
 3) 로그아웃
     - initialMenu로 돌아가는 기능이다
 4) Application 종료
     - initialMenu의 3)과 같다.
 5) 관리자 모드
     - 영상물을 수정 및 등록할 수 있는 기능이며 권한이 있는 자만 사용이 가능하다
     - adminMenu에 있다

3.changeAccountInfo
        회원 정보 수정
        ==================
        1. 이름
        2. 생년월일
        3. 성별
        4. 비밀번호
        5. 전화번호
        6. 주소
        7. 직업
        8. 멤버쉽
        9. 뒤로가기
        0. 회원탈퇴
 1)이름

 2)생년월일

 3)성별

 4)비밀번호

 5)전화번호
    ※정규식 사용 '000-0000-0000'
 6)주소

 7)직업

 8)멤버쉽

 9)뒤로가기

 0)회원 탈퇴

4. adminMenu(관리자 메뉴)
        관리자 메뉴
        ==================
        1. 영상물 등록
        2. 영상물 수정
        3. 평가 내역 확인
        4. 뒤로가기
 1) 영상물 등록
 - addMovie
        영상물 추가
        ===========================
        Original title을 입력하세요.
        knuMovie

        type을 입력하세요.
        1. Movie
        2. Tv Series
        3. Knu Origianl
        3

        청소년 관람불가 여부를 입력하세요.
        1. 청소년 관람 불가
        0. 청소년 관람 가능
        0
        영화가 등록되었습니다
        Enter를 눌러주세요.
 2) 영상물 수정
 queryMovie -> searchResult -> afterSelectMovie -> updateMovie

 3) 평가 확인

 4) 뒤로가기

5. queryMovie
        영상물 검색
        ==========================
        1. 제목 입력 및 검색
        2. 장르 선택
        3. 유형 선택
        4. 개봉 국가 선택
        5. 평가 점수 선택
        6. 개봉(방영 시작)년도 선택
        7. 방영 종료 년도 선택
        8. 배우 선택
        0. 뒤로가기

        searchResult
        검색 결과
        =================================
        1. Small Soldiers (1998)
        2. Swingers (1996)
        3. Heavenly Creatures (1994)
        4. Push (2007)
        5. Bom Yeoareum Gaeul Gyeoul Geurigo Bom (2005)
        6. Serendipity (2001)
        7. L.A. Confidential (1997)
        8. Candyman (1992)
        9. A Beautiful Mind (2002)
        10. The Great Debaters (2006)
        =================================
        1. 다음
        3. 선택
        0. 뒤로가기

6. afterSelectMovie
        영상 제목: Small Soldiers
        평점: 6.2
        러닝타임: 108
        개봉(방영시작)일: 1998-07-27
        영상 종류: movie
        청소년 관람 가능
        장르: Comedy, Adventure, Action
        배우: Kirsten Dunst, David Cross, Jay Mohr

        1. 평가하기(if at queryMovie)
        2. 수정하기(if at updateMovie)
        0. 뒤로가기


7. ratingLogMenu
        평가 기록
        ====================
        1. 영화별 평가 기록
        2. 회원별 평가 기록
        3. 뒤로가기

8. logByMovie
queryMovie -> searchResult -> afterSelectMovie->
        Small Soldiers 의 평가
        =======================================================
        sodales@nislQuisquefringilla.org ==> 9 점
        in.magna@orci.net ==> 4 점
        ultrices.sit.amet@libero.edu ==> 4 점
        =======================================================
        0. 뒤로가기
9. logByEmail
        검색할 이메일을 입력해주세요: 
        knu@knu.ac.kr
        ->
        knu@knu.ac.kr 님의 평가하신 영상물
        ===============================================
        1. Small Soldiers (1998) ==>  1 점
        2. Heavenly Creatures (1994) ==>  1 점
        ===============================================
        0. 뒤로가기
# 유의 사항
   - "※"로 표시 



initial - main - 