# 모각코 Day 7 7/31
## 유데미 강의 14강
Flash chat

### Named Routes
이전에 했던 내용 복습. 이전에는 Navigator를 이용해서 간단히 앞뒤로 페이지를 왔다갔다 했지만 이번엔 여러 페이지를 편리하게 이동하기 위해 Named Routes를 이용한다.
NR을 이용할때는 첫 페이지를 home:이 아닌 initialRoute:로 지정한다.
또한 일일히 이름을 붙이는건 복잡하니 static String id를 각 페이지에 지정해둔다.
이전에 배운대로'/'를 이용해서 이름을 붙인다면 반드시 루트중에 하나는 '/'로만 이름을 지어야 에러가 생기지 않는다. 모든 루트가 '/home'처럼 생기면 안됨.

결과물:
```
initialRoute: WelcomeScreen.id,
      routes: {
        WelcomeScreen.id: (context) => WelcomeScreen(),
        RegistrationScreen.id: (context)=> RegistrationScreen(),
        LoginScreen.id:(context)=>LoginScreen(),
        ChatScreen.id: (context) =>ChatScreen(),
      },
```
Routes를 이용할 때는 
Navigator.pushNamed(context, LoginScreen.id);
처럼 사용하면 됨


### Static Modifier
static: 고정된, 고정적인
use static keyord to implement class-wide variables and methods
내가 이해한 바로는..
만약에 하나의 class에서 'id'라는 변수를 사용하려 하면 그 class 전체를 생성하고 그 안에서 'id'를 사용하는거임.
근데 static으로 만든다면 클래스를 생성할 필요 없이 바로 접근 가능하다는 것..??


## Flutter Animations
Flutter는 나름 최근에 나온거라서 애니메이션 지원이 잘됨.
예시) Hero: 여러 페이지에 걸쳐서 있는 같은 tag를 가진 이미지?가 이어져서 보이게 만들어줌.

Flutter Animation의 3가지 요소
- Ticker: for every time the ticker ticks, it triggers a new set state so that we can render someting differenton screen
- Animation Controller: tells the animation when to start, to stop, to go forwards, to loop back, how long to animate for ...
- Animation Value: the thing that actually does the animating. From value 0 to 1, it changes things such as the height or the size of a component or the color ...

custom flutter animation을 하려면 일단 initState()에 AnimationController를 생성해야한다.
AnimationController는 ticker를 제공하는 vsync를 사용한다.
이후의 말은 그냥 스크립트에서 긁어옴
The ticker provider is going to be our state object, so in this case, it's our welcome screen state. And you can see that the welcome screen state inherits or extends its parent class which is a state widget. And to be able to turn this welcome screen state objects into something that can act as a ticker, we have to use the keyword 'with' and specify that this class welcome screen state can act as a single ticker provider.
이때 mixin이라는게 사용되는데 it enable your class with different types of capability.

animation은 0부터 1까지 커지면서 진행됨. animation.value를 이용해서 다양한 애니메이션을 만들 수 있다.


### mixin
mixins are a way of reusing a class's code in multiple class hierarchies.
mixin class를 만들면 with 키워드를 이용해서 여러 클래스를 활용할 수 있게 된다.
extends를 이용하면 하나의 클래스만을 상속받을 수 있지만 mixin으로 만들어진 키워드는 여러개를 받아올 수 있음

