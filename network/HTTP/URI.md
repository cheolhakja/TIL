# URI
* URI : (resoure identifier) 리소스의 이름과 리소스의 위치를 모두 포함하는 말이다
* URN : (resource name) 리소스의 이름. 그러나 이름으로 리소스를 찾기가 어렵다는 단점이 있다.
* URL : (resource locator) 리소스가 있는 위치를 지정한다.
* URL의 구조 : [프로토콜]://[사용자이름][호스트명]:[포트]/[패스][?쿼리][#fragment]
    * 프로토콜 : http, https 등 어떤 통신 프로토콜을 쓰는지 나타낸다
    * 사용자 이름 : 인증을 위해 사용자 정보를 넘김
    * 호스트명 : ex) www.google.com
    * 포트 : 접속할 포트 번호. 생략하는 경우가 많음. 80,443 등..
    * 패스 : 계층적 구조를 이룸 ex) /home/file1.jpg, play/movie/HarryPotter 
    * 쿼리 : ?로 시작. &로 구분함. 키-값 구조를 이룸. 웹서버에 넘기는 파라미터이며 문자열로 넘어감
    * fragment : html 내부에서 북마크에 사용됨
* 포트 80은 웹 서버의 보안되지 않은 수신 포트임.