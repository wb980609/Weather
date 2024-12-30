# 📝 날씨 일기 프로젝트

### 프로젝트 소개
- 외부 API를 이용하여 날씨 데이터를 가져와 일기를 작성하는 프로젝트입니다.

### Tech Stack
- Language : `Java`
- Build : `gradle`
- DataBase : `MySQL`
- Library : `Lombok`, `spring-web`, `swagger`, `logback`

### 프로젝트 구현 내용
✅ DB와 관련된 함수들을 트랜잭션 처리

✅ 매일 새벽 1시에 날씨 데이터를 외부 API 에서 받아다 DB에 저장해두는 로직을 구현

✅ logback 을 이용하여 프로젝트에 로그 생성

✅ ExceptionHandler 을 이용한 예외처리

✅ swagger 을 이용한 API documentation

### 최종 구현 API 리스트  
 ✅ POST / create / diary
- date parameter (date 형식 : yyyy-MM-dd)
- text parameter = 일기 글(text)
- 외부 API 에서 받아온 날씨 데이터와 함께 DB에 저장

✅ GET / read / diary
- date parameter 날짜 조회
- 해당 날짜의 일기를 List 형태로 반환

✅ GET / read / diaries
- startDate, endDate parameter 로 조회할 날짜 기간의 시작일/종료일 선택
- 해당 기간의 일기를 List 형태로 반환

✅ PUT / update / diary
- date parameter = 수정할 날짜
- text parameter = 수정할 새 일기 text
- 해당 날짜의 첫번째 일기 글을 새로 받아온 일기글로 수정

✅ DELETE / delete / diary
- date parameter 로 삭제할 날짜를 받아주세요.
- 해당 날짜의 모든 일기를 지워주세요.
