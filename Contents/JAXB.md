# JAXB (Java Architecture for XML Binding)
JAXB는 XML Schema를 읽어서 Java Object로 만드는 Unmarshalling과 반대로 Java Object를 XML로 변환하는 Marshalling을 가능하도록 하는 Java API이다.<br>
JAXB API를 이용하면 XML Parsing을 진행할 수 있다. 다만 JAXBContext를 초기화하고 Mashaller, Unmashaller를 생성하는 부분에서 thread-safe(스레드 안전한) JAXBContext의 경우는 생성 비용이 적지 않기 때문에 매번 생성하는 것보다 한 번 생성하고 재사용하는 것이 좋다.<br>
JAXB는 Java Object를 XML로 직렬화하고, XML을 Java Object로 역직렬화해주는 Java API이다. JDK6~9 버전은 JAXB가 내장되어 있어 라이브러리를 추가 할 필요가 없다.
### JAXB Annotation
@XmlRootElement - XML의 Root Element 명을 정의한다.<br>
@XmlElement - XML의 Element 명을 정의한다.<br>
@XmlType - XML 스키마 이름과 namespace를 정의한다. propOrder 속성을 이용해서 XML 표현 시 요소들의 표현 순서를 정의한다.<br>
@XmlElementWrapper - 다른 XML 요소들을 감싸는 역할을 한다. List 같은 컬렉션 객체들을 XML 변환할 때 사용할 수 있다.
### XSD (XML Schema Definition)
XSD는 XML 스키마 정의이다.<br>
XSD는 XML 문서의 구조와 포함할 수 있는 요소(element)와 속성(attribute)들을 명시함으로써 해당 문서가 정의한대로 잘 작성한 XML 문서인지 유효성을 검사하기 위한 것이다.
### 참고자료
- JAXB : https://tychejin.tistory.com/135<br>
https://madplay.github.io/post/jaxb-marshal-unmarshal
- XSD : https://zuyo.tistory.com/589

