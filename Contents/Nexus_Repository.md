# Nexus Repository
Maven에서 사용할 수 있는 Repository이다.
### Nexus Repository의 장점 
1. 외부에서 dependency를 끌어오는 수고를 덜 수 있다.
2. local nexus를 proxy(cache)로 사용함으로써 빠르게 라이브러리를 끌어 올 수 있다.
3. 개발팀에서 사용하는 공용 라이브러리를 local nexus에 배포해서 팀 간에 공유할 수 있다.
4. 사용자 계정을 통해서 repository에 대한 접근 정책을 정의할 수 있다.
### Nexus Repository의 종류
Repository는 용도와 목적에 따라 몇가지로 나눌 수 있다.  
Nexus는 다수의 central repository들을 관리할 수 있으며 Proxy 개념을 통해 개발자들에게 보다 쉬운 repository 연동 편의성을 제공한다.
- **Snapshots (snapshot은 같은 버전으로 여러 번 배포 가능)**  
빌드 등 수시로 릴리즈 되는 바이너리를 배포하는 저장소이다.
- **Release (release는 같은 버전으로 한번 밖에 배포할 수 없음 (다시 배포하려면 서버에서 지우고 배포))**  
정식 릴리즈를 통해 배포되는 바이너리를 저장하는 저장소이다.
- **3rd Party**  
벤더들이 배포하는 바이너리를 저장해 놓은 저장소로 특정 솔루션들을 사용할 때, 딸려오는 라이브러리 등을 여기에 놓고 사용한다.
- **Proxy Repository**  
프록시 저장소는 외부에 있는 메이븐 공개 저장소에 대한 프록시 역할을 하는 저장소이다.  
Central이라는 이름으로 메이븐 중앙 저장소가 이미 추가되어 있다. 원격에 원본 repository가 있는 경우, Local에 캐쉬 용도로 사용한다.
- **Virtual Repository**  
넥서스에 이미 설정되어 있는 저장소에 대하여 다른 URL로 접근 할 수 있도록 지원하기 위한 논리적인 저장소이다.  
Repository Group은 몇 개의 repository를 하나의 repository로 묶어서 단일 접근 URL을 제공한다.  
(Repository Group : 넥서스에 설정한 저장소 그룹이다.  
프로젝트가 진행되면서 의존관계에 있는 라이브러리가 증가하면서, 외부 저장소도 증가하는데, 이 저장소 그룹에 추가되는 외부 저장소를 추가하면 메이븐의 설정파일 변경 없이 의존 관계를 확장할 수 있다.)
### 참고자료
https://kimseunghyun76.tistory.com/390
