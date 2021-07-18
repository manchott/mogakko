# 모각코 Day 3 7/17
## 유데미 강의 10강
Making Quiz app

### Dart List
이용자의 Quiz 정답 현황을 보이는 Score Keeper를 만들기 위해 List를 이용한다. 
Dart에서 특정 데이터타입의 리스트를 만들 때는 하면 된다
Listname.indexOf('ele') 는 ele의 인덱스 번호를 return한다
Listname.add('ele')를 통해 list의 맨 뒤에 ele를 넣고, Listname.insert(n, 'ele')를 하면 n번째 인덱스에 ele를 넣는다
    

### Class
새로운 파일을 만들어 Question 이라고 이름을 짓는다.(class 이름은 대문자로 시작, camel case 사용)
class Question 안에 질문과 답을 넣을 것이다.
class 안에 constructor를 만들고 질문과 답을 할당한다
```
Question({String q, bool a}) {
    questionText = q;
    questionAnswer = a;
}
```
Import 'Question';을 한 뒤에 Question class가 사용 가능해진다.


class 안의 function은 method라고 부른다.
후에 class를 이용해 object를 만들 수 있다.
```
void main(){
    Human jenny = Human(160);  // Object
    print(jenny.height);    // 160
    jenny.talk("Hello World!");
}

class Human{
    double height;
    int age;
    
    Human(double startingHeight){
        height = startingHeight;
    }   // constructer
    
    void talk(String Say){
        print(Say);
    }   // method
}
```



### Abstraction
Being able to bulid more complex systems by creating smaller peices that have a defined job or defined role
프로젝트가 커질수록, 코드가 복잡해질수록 정리를 하라는 것인듯.

