# 모각코 Day 2 7/14
## 유데미 강의 6,7강
6강 들을때는 따로 필기를 안해서 추후에 추가 예정.

7강은 주사위 돌리는 앱을 만드는 강의이다.
### 51. Expanded class
main axis에서 빈 자리를 채운다. (이미지의 경우 화면을 꽉 채우는 느낌)
row의 경우에는 가로로 꽉 채우고, column의 경우에는 세로로 꽉 채우려 한다.
오로지 하나의 child만 가질 수 있다.

여려 element가 있을 경우 flex:를 통해 비율을 정할 수 있다.
왼쪽 image에 flex:2, 오른쪽 image에 flex:1 을 한다면 2:1의 비율로 화면을 꽉 채우게 된다.
(default로 flex:1을 가진다.)
child: Image.asset("image.png")를 통해 바로 이미지를 넣을 수도 있다.


### 52. Intention Actions
VScode에서 이미 있는 element를 center나 widget 등으로 감싸고 싶다면 element에 커서를 두고 ctrl + . 을 하면 선택지가 나온다!
Android studio에서는 Intention Actions을 통해서 할 수 있다.

padding을 더할 때도 원하는 ele에 padding을 감쌀 수 있다.


### 53. Flutter Button Widges
FlatButton을 통해 버튼을 만들 수 있다.
onPressed:(){} 라는 property가 없으면 에러가 걸린다. 함수?인듯


### 54. Dart - Functions 1
void funcName(){
    //do sth
}
처럼 작성하면 됨
void funcName을 비우면 Anonymous function이 된다.
위의 onPressed가 Anonymous function인 것.


### 55. Making Image Change Reactively
var로 정한 int를 이용해서 img를 바꿀 수 있다.
dice1, dice2 등등이 images 파일 안에 있을 때, var diceNum을 widget 안에 선언해두고, 이미지를 넣을 때
"images/dice$diceNum"처럼 하면 diceNum을 바꿀 때마다 dice1, dice2 등등이 튀어나온다.
신기함


### 56. Dart - variables, 57. Dart - data types
$ 를 이용한 방법을 String Interpolation 이라고 한다.

Dart는 기본적으로는 statically typed language이다.
var a = 'string';으로 선언한 후
a = 123; 처럼 하려 하면 오류가 뜬다.

var a; 처럼 데이터를 선언하면 dynamic 데이터 타입이 된다.
그러나 dynamic이든 var이든 가능한 사용 안하는게 좋다. 나중에 문제가 생길 수도 있기 때문.


### 58. Stateful widgets vs. stateless widgets
State of Stateless widgets are not meant to change.
state = 상태.
stful이라고 치면 자동으로 flutter에서 class를 완성시켜준다.
지금까지 사용했던 widget부분과, state의 변화를 track, update하는 부분이 있다.
그리고 앞으로는 hot reload는 사용 못하고 hot restart를 해야한다.
setState 안에 바뀔 것을 넣어줘야 한다.
So that when it updates, we want to call build again, sot that it'll build our user interface and look to see where that change has affected.

setState()안에서 변화가 감지되면, 이것이 어디에 영향을 끼칠것인지 체크를 한 뒤에 build를 처음부터 다시 하는 것이라고 생각하면 될듯.
build 바로 다음에 var a = 6; 같은걸 써뒀더니 아무리 setState()에서 a를 바꿔도 6만 나와서 고생했다.


### 59. Randomising
import 'dart:math'; 
Random().nextInt(max)
0부터 max-1의 숫자 중 하나가 랜덤으로 나온다.


