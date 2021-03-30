# REST (Representational State Transfer)
자원의 이름(자원의 표현)으로 구분하여 자원의 상태(정보)를 주고 받는 모든 것을 의미한다.<br>
HTTP URI (Uniform Resource Identifier)를 통해 자원(Resource)을 명시하고, HTTP Method (POST, GET, PUT, DELETE)를 통해 해당 자원에 대한 CRUD Operation을 적용하는 것을 의미한다.<br>
REST는 자원 기반의 구조 (ROA, Resource Oriented Architecture) 설계의 중심에 Resource가 있고 HTTP Method를 통해 Resource를 처리하도록 설계된 아키텍쳐를 의미한다.<br>
웹사이트의 이미지, 텍스트, DB 내용 등의 모든 자원에 고유한 ID인 HTTP URI를 부여한다.<br>

예를 들어, "http://news.kbs.co.kr/news/view.do?ncd=3421128" 는 Non RESTful URI로 이 URI를 보고서는 어떤 자원(resource)인지 쉽게 파악할 수 없다.<br>
하지만 "http://class.likelion.net/boards/1/posts/406" 는 RESTful URI로 URI를 통해 자원(resource)가 게시판들 중 첫번째 게시판의 글들 중 406번째 글임을 쉽게 알 수 있다.
### CRUD Operation
- Create: 생성 (POST)
- Read: 조회 (GET)
- Update: 수정 (PUT)
- Delete: 삭제 (DELETE)
<br>
REST API 설계 시 가장 중요한 항목은 아래 두 가지이다.<br>
1.	URI는 정보의 자원을 표현해야 한다는 점<br>
2.	자원에 대한 행위는 HTTP Method (GET, POST, PUT, DELETE)로 표현한다는 점

### 참고자료
https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html<br>
https://devuna.tistory.com/79<br>
https://sookmyunglion.tistory.com/9

