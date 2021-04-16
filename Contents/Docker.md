# 도커(Docker)
Docker는 컨테이너 기반의 오픈소스 가상화 플랫폼이다.<br>
다양한 프로그램, 실행환경을 컨테이너로 추상화하고 동일한 인터페이스를 제공하여 프로그램의 배포 및 관리를 단순하게 해준다.<br>
백엔드 프로그램, 데이터베이스 서버, 메시지 큐 등 어떤 프로그램도 컨테이너로 추상화할 수 있고 조립PC, AWS, Azure, Google cloud 등 어디서든 실행할 수 있다.
### Docker의 특징
-	하드웨어의 발전으로 더 많은 효율성을 내기 위해 가상화 사용
-	게스트 OS 사용 하지않음
-	하드웨어에 의존적인 명령어 사용 하지 않음
### 가상 머신과 도커 비교
![image](https://user-images.githubusercontent.com/55124370/114989977-03902b00-9ed3-11eb-826f-d8db839a1b48.png)

왼쪽이 가상머신이고 오른쪽이 Docker이다.<br>
가상 머신은 한 컴퓨터 안에 Hypervisor가 물리 서버 자원들을 추상화하고 공간을 분할하여 독립적인 가상 환경의 서버를 이용한다.<br> 
즉, 한 컴퓨터에 있는 자원을 분배하여 사용하기 때문에 성능에 대한 이슈가 발생할 수 있다.<br>
그러나 Docker는 Hypervisor와 게스트 OS가 필요 없어서 비교적 가볍고 컨테이너 안에 실행 환경들이 독립적으로 돌아가는 것이기 때문에 좋은 성능을 발휘한다.
### 참고자료
https://subicura.com/2017/01/19/docker-guide-for-beginners-1.html<br>
https://medium.com/@darkrasid/docker%EC%99%80-vm-d95d60e56fdd

