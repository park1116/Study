# WebService (웹서비스)
웹서비스는 네트워크 상에서 서로 다른 종류의 컴퓨터들 간에 상호작용을 하기 위한 소프트웨어 시스템이다.<br>
웹서비스는 애플리케이션들이 플랫폼과 프로그래밍 언어와는 독립된 방식으로 통신할 수 있도록 표준 XML메시지를 통해서 네트워크로 접근될 수 있는 Operation들을 기술하는 소프트웨어 인터페이스라고 할 수 있다.<br>
웹서비스는 SOAP, WSDL, UDDI과 같은 공개 표준을 정하여 이를 근간으로 상호 작용이 이루어진다. (SOAP은 정보교환을 목적으로 하는 경량의 XML 기반 프로토콜이다.)<br>
UDDI는 저장소이고 WSDL은 저장소와 저장된 자료에 접근 형식을 적은 설명서이다. 자료를 끄집어내어 가져가 실행 프로토콜을 SOAP이라하고 이는 XML로 구성된다.<br>
### RPC (Remote Procedure Call) 방식
RPC방식의 정보 교환은 request-response 프로세스를 허용하며, 서비스 End-Point는 프로시져 중심의 메시지를 받아서 적절한 응답 메시지를 작성하여 되돌려준다.
### 메시지 기반 (Message-oriented) 방식 (=Document 방식의 교환)
메시지 기반 방식은 송신자가 서비스의 응답을 즉각적으로 요구하지 않아도 될 때 에도 사용이 가능하며, 주로 비즈니스와 여러 가지 형태의 문서 타입을 교환할 필요가 있을 때 사용된다.

# WSDL (Web Services Description Language)
WebService가 제공하는 서비스에 대한 정보를 기술하기 위한 XML 기반 마크업 언어이다. 특정 비즈니스가 제공하는 서비스를 설명한다.
 
기본적인 형태는 위와 같이 생겼고 각 엘리먼트에 작성해야 할 것들은 아래와 같다.
### types
교환될 메시지 설명, 사용될 데이터 형식 정의(스키마에 정의된 타입) 
-> 데이터 타입 재료
### message
메소드 이름 및 파라미터 정의 -> 어떤 메시지를 주고 받을 것인지 선언
### portType
message를 묶어서 하나의 operation으로 만듦 -> 일종의 함수 인터페이스를 정의
### binding
portType에 의해 정의된 작업, 메시지에 대해 메시지 형식과 프로토콜 정의 
-> 클래스 화
### service
WebService URL Endpoints를 설정

## 참고자료
https://jeong-pro.tistory.com/153<br>
https://blog.naver.com/msnayana/80172777745

