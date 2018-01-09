# 그날쿠폰 어플리케이션

기획부터 유지보수까지

## #Project Manage :open_file_folder:
- 전체 일정관리
- 데일리 스크럼
- Server Project Manage
- Client Project Manage

## [__#데이터베이스(MySql)__](https://github.com/qskeksq/thedaycoupon_DB) :open_file_folder:

### 1. DB 설계
- 선행 사항
- 테일블 관계
- 테이블 설계

### 2. DB 구현(테이블, 칼럼 작성)
- code 테이블
- 버전 테이블
- 메인 데이터 테이블
- 서브 데이터 테이블
- 멤버 테이블
- 즐겨찾기 테이블
- 쿠폰 요청 테이블
- 잘못된 정보 테이블

### 3. 데이터 크롤링

### 4. SQL 쿼리

### 5. 원격 서버
- 호스팅
- CLI 사용자 생성
- CLI 권한 설정
- GUI 워크벤치 연결

## [__#서버(Nodejs)__](https://github.com/qskeksq/thedaycoupon_Server) :open_file_folder:

### 1. Project Manage
- 개발목표 & 기획목표
- 설계패턴
- 코딩원칙
- 버전관리
- 스크럼
- 테스트
- 코드정리
- 공부정리

### 2. 설계
- 어플리케이션 단위
    - 버전관리
    - 보안관리
- 설계 단위
    - 서버 설계 패턴
    - 관리, 디버깅 모듈
    - 내부 모듈화
    - server
    - REST
    - controller
    - dao/database
    - 응답설계
    - 콜백체인
    - 외부모듈
- 구현 단위

### 3. 구현 

### 관리모듈
- 코드관리모듈
- 로그 & Exception
- 자동실행

### (1) server.js / app.js
- 데이터베이스 연결
- 서버 생성 & 연결

### (2) router
- METHOD
- REST 설계

### (3) controller
- member
- version
- coupon
- detail_photo
- logo
- favorite
- wrong_info
- request_coupon

### (4) dao
- controllerDao

### (5) database
- connect
- executeRaw
- executeByValues

### (6) response
- err
- res

### (7) module
- private_module
- config
    - db_options
    - secret
    - host
    - port
- public

### 4. 원격서버
- ssh 서버 접속
- 노드 관리 NVM

## [__#클라이언트(Android)__](https://github.com/qskeksq/thedaycoupon_Android) :open_file_folder:

### 1. Project Manage
- 개발목표 & 기획목표
- 설계패턴
- 코딩원칙
- 버전관리
- 스크럼
- 테스트
- 코드정리
- 공부정리

### 2. 설계
- 어플리케이션 단위
    - manifest
    - gradle : SDK, configs, 디버깅/릴리즈
    - 보안
    - 보전관리
- 설계 단위
    - 설계 패턴
    - 패키지 관리
    - 도메인
    - 네트워크
    - 인터페이스, 추상클래스
    - 에러, Crash 설계
- 구현 단위
    - 클래스
    - 메소드
    - 비동기
    - 생명주기
    - 성능
- resource 단위
    - 언어
    - styles
    - secrets
- assets 단위

### 3. 구현
### (1) domain
- local
- server
- 영구저장소
- 임시저장소

### (2) Launcher
- WorkFlow
    - 권한체크
    - 인터넷연결
    - 인터넷타입
    - 버전체크
    - 메인데이터 받아오기
    - 이미지파일 받아오기
    - 처음 입장인지 확인
    - 넘어감
- RemoteService

### (3) 로그인/회원가입 & 회원관리 & 권한관리
- 로컬과 서버연동 WorkFlow
    - 로그인 이력 확인
    - 로컬 DB 반영
    - UI 반영
    - 서버 반영
- 로그인 WorkFlow
    - 방문자로 시작
    - 회원가입
    - searchMember
    - 로그인
    - 인증
    - 응답
    - 서비스 이용중
        - 앱 재입장
        - 인터넷 끊어짐
        - 비정기성 광고
    - 토큰인증
    - 로그아웃
- Kakao Login WorkFlow
    - 콜백 클래스 구현
    - 콜백 등록
    - SNS 모바일 앱에 요청
    - onActivityResult로 응답
    - 콜백 실행
    - 정보, 토큰 받아옴
    - searchMember
    - 로그인 WorkFlow
- Facebook Login
- Google Login
- 일반 Login
- RemoteService

### (4) Main
- CustomTabLayout
- 다중 뷰타입
- 데이터 WorkFlow
    - 임시저장소(캐싱) 생성 & 맵핑
    - 데이터 불러오기
    - 데이터 갱신
- 로그인 이력 관리
- 즐겨찾기 WorkFlow
    - 회원 권한설정
    - 아이디 확인
    - 로컬 DB 반영
    - UI 반영
    - 서버 반영
- RemoteService

### (5) Detail
- WorkaroundMapView
- GooglePlace
- RemoteService

### (6) Favorite
- 즐겨찾기 삭제
- leftOver 처리
- RemoteService

### (7) 쿠폰요청
- 이미지 요청 WorkFlow
    - 이미지 이름, 파일 만들기
    - 이미지 비트맵으로 불러오기
    - 콜백으로 비트맵에 저장
    - MultiPart 생성
- 쿠폰 정보 추가
- 영업시간
- RemoteService

### (8) Remote
- IRemoteService
- ServiceGenerator

### (9) Util
- DeviceUtil
- GeoUtil
- LogUtil
- NetworkUtil
- SignInUtil
- StringUtil

### Application 등록

