# JVM(Java Virtual Machine)
JVM은 자바 가상 머신의 약자를 따서 줄여 부르는 용어이다. (가상머신이란 프로그램을 실행하기 위해 물리적 머신과 유사한 머신을 소프트웨어로 구현한 것이다.)  
JVM의 역할은 Class Loader를 통해 자바 애플리케이션을 읽어 들여 자바 API와 함께 실행하는 것이다.  
JVM은 Java와 OS 사이에서 중개자 역할을 수행하여 Java가 OS에 구애받지 않고 사용을 가능하게 해준다. 그리고 가장 중요한 **메모리 관리, Garbage Collection**을 수행한다.  
ARM 아키텍처 같은 하드웨어는 레지스터 기반으로 동작하는데 비해 JVM은 스택기반으로 동작한다.  

### JVM을 알아야하는 이유
메모리를 효율적으로 사용하여 최고의 성능을 내기 위해서라고 할 수 있다.  
동일한 기능의 프로그램이더라도 메모리 관리에 따라 성능이 좌우된다. 메모리 관리가 되지 않는 경우 속도저하 현상이나 튕김 현상 등이 일어날 수 있다.

### 자바프로그램 실행과정
1. 프로그램이 실행되면 JVM은 OS로부터 프로그램이 필요로 하는 메모리를 할당받는다. JVM은 이 메모리를 용도에 따라 여러 영역으로 나누어 관리한다.
2. 자바 컴파일러(javac)가 자바 소스코드(.java)를 읽어들여 자바 바이트코드(.class)로 변환시킨다.
3. Class Loader를 통해 class파일들을 JVM으로 로딩한다.
4. 로딩된 class파일들은 Execution engine을 통해 해석된다.
5. 해석된 바이트코드는 Runtime Data Areas에 배치되어 실질적인 수행이 이루어진다.  

&nbsp;&nbsp; **이러한 실행과정 속에서 JVM은 필요에 따라 Thread Synchronization과 Garbage Collection같은 관리작업을 수행한다.**

### 참고자료
https://asfirstalways.tistory.com/158
