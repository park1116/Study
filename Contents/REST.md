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
### REST 의 특징
1.	Uniform (유니폼 인터페이스)  
Uniform Interface는 URI로 지정한 리소스에 대한 조작을 통일되고 한정적인 인터페이스로 수행하는 아키텍처 스타일이다.
2.	Stateless (무상태성)  
REST는 무상태성이다. 작업을 위한 상태정보를 따로 저장하고 관리하지 않는다. 세션 정보나 쿠키정보를 별도로 저장하고 관리하지 않기 때문에 API서버는 들어오는 요청만을 단순히 처리하면 된다. 그래서 서비스의 자유도가 높아지고 서버에서 불필요한 정보를 관리하지 않음으로써 구현이 단순해진다.
3.	Cacheable (캐시 가능)  
REST의 가장 큰 특징 중 하나는 HTTP라는 기존 웹표준을 그대로 사용하기 때문에, 웹에서 사용하는 기존 인프라를 그대로 활용 가능하다. 따라서 HTTP가 가진 캐싱 기능이 적용 가능하다.
4.	Self-descriptiveness (자체 표현 구조)  
REST API 메시지만 보고도 쉽게 이해 할 수 있는 자체 표현 구조이다.
5.	Client – Server 구조  
REST서버는 API 제공, 클라이언트는 사용자 인증이나 컨텍스트(세션, 로그인 정보)등을 직접 관리하는 구조로 각각의 역할이 확실히 구분되기 때문에 클라이언트와 서버에서 개발해야 할 내용이 명확해지고 서로간 의존성이 줄어든다.
6.	계층형 구조  
REST서버는 다중 계측으로 구성될 수 있으며 보안, 로드 밸런싱, 암호화 계층을 추가해 구조상의 유연성을 둘 수 있고 PROXY, 게이트웨이 같은 네트워크 기반의 중간매체를 사용할 수 있다.

REST API 설계 시 가장 중요한 항목은 아래 두 가지이다.  
**1.	URI는 정보의 자원을 표현해야 한다는 점**  
**2.	자원에 대한 행위는 HTTP Method (GET, POST, PUT, DELETE)로 표현한다는 점**  
### 참고자료
https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html  
https://devuna.tistory.com/79  
https://sookmyunglion.tistory.com/9  
https://meetup.toast.com/posts/92

