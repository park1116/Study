# TCP (Transmission Control Protocol)
TCP(Transmission Control Protocol)란 소켓 프로그래밍 중의 하나로 Stream 통신 프로토콜이라고 부르며, 양쪽의 소켓이 연결된 상태여야만 통신이 가능하기 때문에 연결지향 프로토콜이라고 한다.
### TCP의 특징
- 인터넷 상에서 데이터를 메세지의 형태(세그먼트라는 블록단위)로 보내기 위해 IP와 함께 사용하는 프로토콜이다.
- IP가 데이터의 배달을 처리하고 TCP는 패킷을 추적 및 관리한다.
- 흐름제어 및 혼잡제어를 제공한다.
   -  흐름제어 
      - 데이터를 송신하는 곳과 수신하는 곳의 데이터 처리 속도를 조절하여 수신자의 버퍼 오버플로우를 방지한다.
      - 송신하는 곳에서 감당이 안되게 많은 데이터를 빠르게 보내 수신하는 곳에서 문제가 일어나는 것을 막는다.
   - 혼잡제어
      - 네트워크 내의 패킷 수가 넘치게 증가하지 않도록 방지한다.
      - 정보의 소통량이 과다하면 패킷을 조금만 전송하여 혼잡 붕괴 현상이 일어나는 것을 막는다.
- 높은 신뢰성을 보장한다. 
- UDP보다 속도가 느리다.
- Full-Duplex(전이중), Point to Point(점대점) 방식이다.
  - Full-Duplex : 전송이 양방향으로 동시에 일어날 수 있다.
  - Point to Point : 각 연결이 정확히 2개의 종단점을 가지고 있다.
- 연속성보다 신뢰성있는 전송이 중요할 때에 사용된다.
# UDP (User Datagram Protocol)
UDP(User Datagram Protocol)는 전송계층의 비연결 지향적 프로토콜이다. 비연결 지향적이란 데이터를 주고 받을 때 연결 절차를 거치지 않고 발신자가 일방적으로 데이터를 발신하는 방식을 의미한다.
### UDP의 특징
- 데이터를 데이터그램 단위로 처리하는 프로토콜이다.
- 비연결형 서비스로 데이터그램 방식을 제공한다.
  - 연결을 위해 할당되는 논리적인 경로가 없다.
  - 각각의 패킥은 다른 경로로 전송되고, 각각의 패킷은 독립적인 관계를 지니게 된다.
- 정보를 주고 받을 대 정보를 보내거나 받는다는 신호절차를 거치지 않는다. 
- 신뢰성이 낮다.
- TCP보다 속도가 빠르다.
- 신뢰성보다 연속성이 중요한 서비스(ex> 실시간 서비스(Streaming))에 사용된다.
### 참고
- UDP와 TCP는 각각 별도의 포트 주소 공간을 관리하므로 같은 포트 번호를 사용해도 무방하다. 즉, 두 프로토콜에서 동일한 포트 번호를 할당해도 서로 다른 포트로 간주한다.
- 같은 모듈내에서도 클라이언트 프로그램에서 동시에 여러 커넥션을 확립한 경우에는 서로 다른 포트 번호를 동적으로 할당한다. (동적할당에 사용되는 포트번호는 49,152 ~ 65,535 이다.)
### 참고자료
- https://coding-factory.tistory.com/270  
- https://www.joinc.co.kr/w/Site/Network_Programing/Documents/IntroTCPIP
- https://github.com/WeareSoft/tech-interview/blob/master/contents/network.md#tcp%EC%99%80-udp
- https://coding-factory.tistory.com/614
