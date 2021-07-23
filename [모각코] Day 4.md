# 모각코 Day 4 7/21
## 유데미 강의 12강
BMI Calculator

### 앱 내에서 이동하기
Navigator.push 를 통해 다른 페이지로 가고
Navigator.pop 을 통해 이전 페이지로 돌아간다.
혹은 main.dart에 routes를 map으로 만들어서 Navigator.pushNamed를 통해 페이지를 이동할 수도 있다.
앱을 개발할 때 필수적인 기능.
    
### Map
파이썬의 dictionary와 비슷한 기능
key와 value가 짝으로 맺어져 있다.
선언할 때
```
Map<String, int> phonebook = {
    'a' : 1234567,
    'b' : 9876543,
};
```
처럼 하면 됨.
리스트와 달리 순서가 없음. 부를 때 phonebook['a']처럼 하면 됨.


### 앱 마무리 단계
const들을 하나의 파일에 모아두는 것이 좋다.
특히 TestStyle의 경우, 이름 앞에 k를 붙여둬서 나중에 서치에 용이하도록 만들자.
폴더를 만들어서 파일 정리해두는것도 중요
