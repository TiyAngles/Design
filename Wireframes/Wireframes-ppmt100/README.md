# 프로세스 설계

mypage와 editpage의 프로세스 설계와 플로우차트 입니다.

---

## 마이페이지

### 공통사항

- 모든 마이페이지 관련 접속은 로그인 권한 필요(인증)
- 로그인한 유저 본인의 마이페이지만 방문 가능

### 하단

- 활동로그와 위시리스트는 tab으로 작동
- db에서 가져와서 보여줌

### 팔로워, 플레이스, 팔로잉

- 플레이스 클릭 시 방문 여행지역 리스트 상세 확인
- 팔로워 클릭 시 팔로워 리스트 상세 확인
- 팔로잉 클릭시 팔로잉 리스트 상세 확인

### 메인

- 프로필 사진 클릭시 파일 시스템이 열림으로서 프로필 사진 변경 가능
- 닉네임, 간단소개.상태메시지는 버튼 상태로 존재했다가 클릭시 input으로 변하면서 내용 변경 가능
- 위 두 가지 모두 입력만으로 자동 저장
- 단 hover등으로 사용자가 클릭으로 개별 변경이 가능함을 알 수 있도록 해야함
- 편집 버튼 클릭시 edit page로 이동

---

## 에딧페이지

### 공통사항

- 모든 에딧페이지 관련 접속은 로그인 권한 필요(인증)
- 로그인한 유저 본인의 에딧페이지만 방문 가능

### 메인

- 프로필 사진 클릭시 파일 시스템이 열림으로서 프로필 사진 변경 가능
- 모든 input은 변경 가능 하도록 열려 있음.
- 변경 확정 버튼은 현재 비밀번호가 db와 일치해야 하며 input validation이 성립해야 함
- input이 비어있다면 원래 입력된 정보를 유지하지만 한 글자라도 input 내 입력이 되어있는 경우 input validation 성립 확인

### input validation

- 이메일에 @가 포함 되어 있음(input type="email"), email의 형식 확인
- 현재 비밀번호가 db의 비밀번호와 일치
- 비밀번호는 8자 이상(필요시 추가적으로 대문자 및 특수문자 포함)
- 비밀번호 확인과 비밀번호의 텍스트가 일치
- 생년월일 클릭시 달력이 열리며 yyyy-mm-dd 등의 형식

---

## 변경 및 추가

- 간단 소개/상태 메시지는 클릭시 새로운 창이 열림 (input type text가 아닌 textarea)
- 에딧 페이지에 뒤로가기 버튼 필요

---

### Flow chart

[Flowchart](https://www.figma.com/file/arsuF0r1TMdt9YDs0dFLhF/Flowchart?node-id=0%3A1)

---

### 수정 및 건의 사항 언제든지 카톡으로 말씀해주세요~ 플로우 차트 혹시 안열리면 말씀해주시면 바로 수정하겠습니다.
