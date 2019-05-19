# Software Engineering Homework 3
---

## **개요**
 수정된 온라인 티켓 매매시스템에 대해 `Detailed Design`과 `Implementation`을 수행한다. 

---

## **수정된 Requirements**

### 1.1 회원가입 기능
> 사용자는 온라인 티켓 매매시스템을 사용하기 위한 권한을 얻기 위해서 회원가입을 해야 한다. 자신의 ID, password, 이름, 주민번호 및 사용자 유형(판매자 또는 구매자)를 입력해야 한다. (입력 내용은 옳다고 가정한다. 즉, 유효성 검사는불필요하다.) 회원가입을 하면 판매자 혹은 구매자로서 시스템을 사용할 수 있다.

### 1.2. 회원탈퇴 기능
> 회원은 이 시스템에서 탈퇴할 수 있다. 탈퇴와 동시에 시스템 사용 권한은소멸한다. 단, 판매자는 등록 중인 미판매 티켓이 없을 경우에만 탈퇴할 수 있다.

---

### 2.1. 로그인 기능
> 회원은 ID와 password를 입력하여 로그인할 수 있다.

### 2.2. 로그아웃 기능
> 로그인 중인 회원은 로그아웃 할 수 있다.

---

### 3.1 판매티켓 등록 기능
> 판매자 회원은 팔려는 티켓을 경기시작 이틀 전까지 등록할 수 있다. 등록할때에는 희망판매가격 및 경기정보를 입력해야 한다. 경기정보는 야구경기날짜, 시각, 홈팀, 어웨이팀,좌석위치(1~100행 및 1~100열로 표현)으로 구성된다. 또한, 등록 시 limited-time auction1) 여부를 선택할 수 있다.

### 3.2. 등록한 티켓 조회 기능
> 판매자 회원은 자신이 등록한 티켓을 조회할 수 있다. 조회 결과는 희망판매가격, 야구경기날짜, 시각, 홈팀, 어웨이팀, 좌석위치, limited-time auction 선택여부 및 판매여부를 포함하고, 경기날짜 및 시각이 빠른 티켓부터 정렬해서 보여준다. 등록한 지 1년이 지난 숙소는 자동 삭제된다.

---

### 4.1. 티켓 검색 기능
> 구매자 회원은 홈팀을 선택해서 예약 가능한 티켓을 검색할 수 있다. 검색결과는 희망판매가격, 야구경기날짜, 시각, 홈팀, 어웨이팀, 좌석위치를 포함하고, 경기날짜 및 시각이 빠른 티켓부터 정렬해서 보여준다.
### 4.2. 티켓 예약 기능
> 티켓 검색 이후, 선택적으로, 구매자 회원은 원하는 티켓을 예약할 수 있다.
### 4.3. Limited-time auction 중인 티켓 검색 기능
> 구매자 회원은 홈팀을 선택해서 경매 중인 티켓을 검색할 수 있다. 검색 결과는 야구경기날짜, 시각, 홈팀, 어웨이팀, 좌석위치 및 마감까지 남은 시간을 포함한다. 경기날짜 및 시각이 빠른 티켓부터 정렬해서 보여준다.
### 4.4. Limited-time auction 참여 기능
> 경매 중인 티켓 검색 이후, 선택적으로, 구매자 회원은 원하는 티켓에 대해 입찰금액을 입력하여 입찰에 참여할 수 있다. (낙찰 및 유찰: 경매대상으로 등록된 티켓의 경매종료시점에 입찰액이 높은 순서로 낙찰된다. 입찰에 참여한 회원이 없는 경우에는 유찰이 된다.)
### 4.5. 예약 정보 조회 기능
> 구매자 회원은 자신이 예약한 티켓의 정보(구매가격, 야구경기날짜, 시각, 홈팀, 어웨이팀,좌석위치)를 조회할 수 있다. 경기날짜 및 시각이 빠른 티켓부터 정렬해서 보여준다.

---

## **제출 결과물**

### (1) 보고서 내용
- Use case diagram 및 Use case description
- Sequence diagram
- Design class diagram (그림 A5.7 참고) Ÿ attribute type Ÿ operation signature
- visibility (+, ‐, #, ~) Ÿ association (collection class 등)
- Source code (2 column으로 프린트할 것) Ÿ 첨부된 coding convention 파일을 참고해서 각 file, class, operation, attribute의 naming & comment 형식에 따르고 추가적인 부분은 팀 내에서 협의할 것
- 보고서 첫 부분에 팀 내 역할 분담 및 각 팀원이 실제 수행한 내용을 상세히 명시할
것

### (2) 제출 마감 시간 및 장소
- 제출 마감 시간 : 6월 7일 (금요일) 오후 2시
- 장소 : 파일은 클래스넷에 upload (개인별 upload) hard copy는 수업시간에 제출 (팀당 한 copy)

---

## 유의 사항
### (1) 채점 기준
- 기능이 모두 구현될 수 있도록 modeling되었고 구현이 modeling과 일치하는가? 50 %
- 프로그램이 데모 시나리오를 만족하는가? 30 %
- Source code가 convention에 따라 작성되었는가? 10 %
- 팀원 간에 역할 분담이 적절히 되었는가? 10 %
### (2) 감점 사항
- 일정상 마감 시간 이후에는 제출 받지 않음
- 부정행위 발견 시 관련 학생 모두 F 학점 처리함
### (3) 질문은 클래스넷 게시판 및 교수 면담시간을 이용하기 바람