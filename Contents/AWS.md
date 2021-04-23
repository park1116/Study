# 아마존 웹 서비스(Amazon Web Service)
서비스 또는 기업용 애플리케이션이 실행되고 많은 양의 데이터를 관리하기 위한 컴퓨팅, 스토리지, 네트워크, 플랫폼, 소프트웨어 등의 다양한 자원을 제공하는 클라우드 서비스
### AWS 장점
1.	**자동화** : 인프라 자원의 구축과 종속성 등의 문제를 코드로 자동화하여 신뢰성과 효율을 높인다.
2.	**확장성** : 인프라 확장과 축소에 시간과 제한을 두지 않으며 스스로 용량에 따라 조절된다.
3.	**신뢰성** : 대부분의 AWS 서비스는 장애 허용 또는 고가용성 서비스이다.
4.	**시간단축** : 인프라 자원 요청에서 구축까지 시간이 얼마 걸리지 않는다. 빠르게 새로운 요구사항을 인프라에 적용가능하다.
5.	**규모의 경제** : 출범 이후, 여러 차례 가격 인하를 해오면서 시작 가격보다 현재 비용은 45배 이상 감소했다.
6.	**국제화** : AWS는 전 세계에 데이터센터(IDC)를 두고 있기 때문에 전 세계를 대상으로 비즈니스를 구현, 실행할 수 있다.
7.	**표준화** : ISO 27001, FedRAMP 및 DoD CSM, PCI DSS 레벨1, ISO 9001등 보안과 품질 표준을 준수한다.
### AWS 용어
- **리전**  
AWS의 서비스가 위치하고 있는 물리적 위치. 전세계 주요 지역에 위치하고 있으며 현재(2020년 기준) 25개가 있다.<br>
리전에는 가용 영역(Availability Zone, AZ)이 여러 개 있고 가용 영역의 클러스터(Cluster)가 리전이다.
- **가용영역**  
우리가 흔히 말하는 데이터센터(IDC)이다.<br>
리전에 위치하는 서비스의 높은 가용성(High Availability)을 위해 여러 논리적 클러스터 그룹으로 구성된다. 현재(2020년) AWS는 80개 가용 영역을 두고 있다.
- **에지 로케이션**  
AWS CDN(Content Delivery Network)서비스인 CloudFront를 위한 캐시 서버이다. AWS도 CloudFront 서비스의 캐시를 위해 전 세계 주요 도시에 Edge Location을 구축해 놓고 있다.
### 활용 사례 및 사용한 AWS 서비스
- **화성 탐사 로버 큐리오시티(Mars Curiosity Rover)**  
단기간에 많은 서버가 필요하고 이벤트 이후에는 필요가 없는 경우<br>
EC2, Route53, CloudFront, CloudFormation, ELB(Auto Scaling)
- **넷플릭스(Netflix)**  
자체 IT 인프라를 직접 구축하지 않고 비즈니스와 서비스 개발/운영에 집중한 경우<br>
AWS 컴퓨팅을 비롯하여 데이터 베이스, 분석/권장 엔진, 비디오 트랜스 코딩, 스토리지 등
- **애니모토(Animoto)**  
며칠 만에 사용자가 폭증하는 경우 (스타트업)<br>
최대 2500개의 EC2 인스턴스 사용
- **아모레 퍼시픽(Amore Pacific)**  
급격히 증가하는 글로벌 사용자에 대응 (국내 대기업)<br>
EC2, Route53, S3, CloudFront 등
- **쿠키런 모바일 게임**  
사용자 수를 예측하기 어렵고 하루동안 사용량의 변화가 급변하는 경우 (국내 스타트업)<br>
EC2, CloudFront, S3, ELB(Auto Scaling)
## AWS 서비스
AWS 클라우드 서비스는 하단의 하드웨어와 그 위에서 동작하는 소프트웨어 서비스로 구성되어 있다.<br>
웹 기반의 API는 AWS 서비스와 애플리케이션 사이의 인터페이스 역할을 한다. AWS의 모든 서비스는 API 호출로만 관리할 수 있다.<br>
가상 서버와 다른 서비스와의 차이는 가상 서버가 시작되면 SSH를 통해 접속하여 여러 소프트웨어 설치 및 서버 관리가 가능하다는 것이다.
### AWS Service 분류
- **Compute(컴퓨팅 서비스)**  
가상 서버(EC2)
- **App(애플리케이션 서비스)**  
메시지 큐(SQS), 검색(Cloud Search), 동영상 인코딩(Elastic Transcoder), 푸시 알림(SNS)
- **Enreprise(기업용 애플리케이션을 위한 서비스)**  
이메일 서비스(SES), 디렉토리 서비스(Directory Service)
- **Deployment(배포 서비스)**  
인프라 구성과 배포(CloudFormation), 애플리케이션 배포 플랫폼(Elastic Beanstalk), 다중 계층 애플리케이션 배포(OpsWorks)
-	**Management(모니터링)**  
인프라 자원 감시(CloudWatch)
-	**Security / Identity / Compliance(보안 / 자격 / 접근통제 서비스)**  
IAM(Identity Access Management)
-	**Storage(데이터 저장 서비스)**  
인터넷 스토리지(S3), 아카이브(Archive) / 백업(Backup), 스토리지(S3 Gracier)
-	**Database(데이터베이스 서비스)**  
rhksrPgud 데이터베이스(RDS), NoSQL(DynamoDB), In-Memory Cache(ElasticCache)
-	**Networking(네트워킹 서비스)**  
고정 IP(Elastic IP), CDN(CloudFront) 가상 네트워크(VPC), DNS(Route53)
### AWS 서비스 API 호출을 위한 도구
1.	**관리 콘솔**  
웹 기반 관리 콘솔(https://console.aws.amazon.com)로 거의 모든 브라우저에서 사용 가능하다.  
편리한 GUI 환경에서 AWS 서비스들의 제어가 가능하다.
2.	**CLI(Command Line Interface)**  
명령줄에서 aws라는 명령어로 AWS 서비스들의 모든 것을 제어 할 수 있다.  
스크립트(Shell Script)에 일련의 CLI 명령어들을 모아 인프라 자동화에 사용될 수 있다.  
Unix(Linux)계열 OS뿐만 아니라 윈도우 Power Shell도 지원한다.
3.	**SDK**  
개발 중인 애플리케이션과 AWS 서비스를 통합할 때 사용한다.  
Android, JavaScript, IOS, Java, .Net, C++, PHP, Python, Ruby, Go Lang 등 인기 있는 개발 언어들을 지원한다.
4.	**블루프린트(Blueprint, Tenplate)**  
클라우드 인프라 구성 자동화에 사용된다.  
인프라의 구성 요소들 간의 종속성에 큰 신경을 쓰지 않고 복잡한 인프라 구축을 자동화 할 수 있다.
### 참고자료
“AWS웹개발” 강의자료
