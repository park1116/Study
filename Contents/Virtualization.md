# 가상화(Virtualization)
하나의 물리적 하드웨어를 여러 가상 하드웨어(가상 머신)으로 만드는 기술이다.  
가상 머신은 각각의 CPU, 메모리, 네트워크 인터페이스, 스토리로 구성되고 서로 격리시킨다.  
가상화에 필요한 소프트웨어를 하이퍼바이저(Hypervisor)라 한다.  
  
![image](https://user-images.githubusercontent.com/55124370/115981807-961a8380-a5d1-11eb-8909-305f35fae876.png)
### Hypervisor 구분
**1.	Type 1(Native, Bare Metal)**  
- 호스트 하드웨어에 직접 설치된다.  
- Hypervisor는 OS역할과 VM들을 관리하는 역할을 모두 한다.  
- 아무것도 설치되어 있지 않은 컴퓨터에 Hypervisor가 바로 설치된다.  
- OS처럼 설치해야 하기 때문에 하드웨어 설정 등이 어려운 편이다.  
- Type2에 비해 성능이 좋다.  
- ex) Xen, KVM, MS Hyper-V  
![image](https://user-images.githubusercontent.com/55124370/115981950-76d02600-a5d2-11eb-9b8b-5cbb2ca093bb.png)

**2.	Type2(Hosted)**  
- 호스트 OS 위에 설치되는 방식의 Hypervisor 이다.  
- 어플리케이션으로 설치하기 때문에 설치 및 구성이 쉽다.  
- 하드웨어 전체를 에뮬레이트 하는 방식이기 때문에 성능이 안좋다.  
- ex) VMWare, Workstation, Oracle VirtualBox  
![image](https://user-images.githubusercontent.com/55124370/115981953-7c2d7080-a5d2-11eb-965b-05699b583e3f.png)

### Type1 Hypervisor의 분류
#### 전가상화(Full Virtualization, HVM)
-	하드웨어를 완전히 가상화 하기 때문에 게스트 OS가 자신이 가상화 환경인지 모른다.  
-	모든 하드웨어 명령을 직접 요청하는 것처럼 작동한다.  
-	게스트 OS에 별다른 수정이 없기 때문에 다양한 OS 사용이 가능하다.  
-	CPU의 Intel-VT나 AMD-V들의 물리적인 가상화 자원이 필요  
-	모든 하드웨어 명령을 가상화 하기 때문에 느리다.  
-	Vmware, KVM, MS Hyper-V  
#### 반가상화(Para Virtualization, PVM)
-	하드웨어를 완전히 가상화 하지 않기 때문에 게스트 OS는 가상화된 환경인지 안다.  
-	모든 하드웨어 명령을 가상화 하지 않는다.  
-	가상화가 필요한 명령만 하이퍼바이저에게 요청한다. (Hyper Call)  
-	OS의 커널을 수정해야 한다.  
-	호스트의 CPU가 가상화 기술을 지원하지 않아도 가능하다.  
-	전가상화 보다 빠르다  
-	Xen
### 참고자료
“AWS웹개발” 강의자료
