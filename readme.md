#소프트웨어 공학 팀플을 위한 리포지토리

###**11월 29일자 패치노트*

nodemodules 파일은 용량 문제로 x

추가된 모듈 (로그인 관련)

express-session(로그아웃 후 다시 로그인 할 수 있는 세션),
session-file-store(이메일 정보 저장), 
passport(로그인 인증용 미들웨어),
passport-google-oauth(구글 로그인 api 전용 모듈)


로그인 비로그인 구분이 가능함.

로그인 하면 db에 user email이 저장됨.

sever.js의 getEmail함수 통해서 가져올 수 있고
비로그인 시 undifined를 반환 해서
이 함수로 로그인 여부 구분 가능.

로그인이 된 상태에서 초대링크로 접속한 친구는
app.js에서 바로 채팅방 안으로 접속됨 

로그인을 안하면 로그아웃을 하도록 함.
이때 '회의에 입장하려면 로그인이 필요합니다.' 문구를 출력함

근데 구글로그인 창 갔다오면 login/callback 으로 리디렉션 되는데
그래서 이전에 친 http://localhost:4000/chat?iroomName=123&inickName=123 이런 정보를 날려먹어서
초대안받은 사람이랑 동일하게 됨.





