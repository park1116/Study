# JSON
JSON은 JavaScript Object Notation의 약자로써, 의미 그대로 해석하면 JavaScript에서 객체를 만들 때 사용하는 표기법을 의미한다.<br>
JSON은 클라이언트와 서버간의 데이터를 주고받을 때 사용할 수 있는 표현의 하나이다.<br>
JSON의 두 가지 기본구조는 JSONObject와 JSONArray가 있다.
### JSONObject
기본 구조 : {Name : Value, Name2 : Value2 …}<br>
JSONObject는 ‘{‘ 로 시작하고 ‘}’로 끝내어 표현한다.<br>
{} 안에는 String으로 된 Name과 Value의 쌍을 ‘:’로 구분하여 사용한다.<br>
Name과 Value의 구분은 ‘,’으로 한다.<br>
순서화되지 않은 SET이다.<br>
Ex) {"name" : "park", "age" : 27, "sex" : "male"}
### JSONArray
기본 구조 : [{Name : Value}, {Name2 : Value2} …]<br>
JSONArray는 ‘[‘로 시작하고 ‘]’ 로 끝내어 표현한다.<br>
[] 안에는 JSONObject나 String 값 등을 담을 수 있다.<br>
각 Object나 String의 구분은 ‘,’로 한다.<br>
순서화된 SET이다.<br>
Ex) [{"name" : "park", "age" : 27}, {"sex" : "male"}]<br>
### 참고자료
https://aljjabaegi.tistory.com/40

