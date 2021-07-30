# 모각코 Day 6 7/28

## 유데미 강의 13강 이어서

Climate app

### API

: Application Programming Interfaces
소프트웨어를 만들거나 외부 시스템과 연결하기 위해 이용하는 것.
API를 사용하는 예시) 은행에 가서 막무가내로 돈을 달라고 하면 안됨. 나의 계좌를 알려주고 비밀번호를 입력하며 계좌에서 돈을 뽑아달라고 해야함. 돈을 입금할때도 마찬가지.
내 앱에서 다른 시스템에 키를 보내며 나에게 필요한 데이터를 받아내는 것.
이번 앱에서는 Open Weather Map api를 이용할 것이다.
근데 나는 아직 appID가 없어서 따라서 하질 못함..

### JSON

api는 xml 형태나 JSON 형태로 데이터를 준다.
xml: html이랑 비슷하게 생김. <key>value</key>
JSON: JS랑 비슷하게 생김. {key:value}

jsonDecode(data)를 통해 JSON에서 data를 가져올 수 있는데 이 결과는 dynamic하기 때문에 변수를 선언할 때 var을 이용한다.
혹은 각 데이터의 타입을 확인해서 각각 double, int 등등으로 선언해도 된다.

### OWP에서 ID 만들고 api 사용하기

1. 회원가입
2. API keys 에서 나의 key 확인하기
3. const apiKey에 내 키를 저장해둔다!

강좌대로 진행하다가 http.get가 안되는 현상 발생.
알고보니 이제는
http.Response response = await http.get(Uri.parse('url'))을 해야함.

await를 사용하려면 Future을 함께 사용해야하는것 잊지말기

### 로딩중 표시 만들기

pub.dev/packages/flutter_spinkit/ 참고
다양한 로딩 이미지? 사용 가능.

150. passing data to a state object 복습 필요.
     하란대로 따라하긴 했지만 제대로 이해는 못한 기분..

### Textfield widget

유저에게 입력창을 제공하는 위젯.
기본적으로 글씨색이 하얀색이니 색 바꾸기 필요.
onChanged:(value) 를 하면 사용자가 입력한대로 value에 저장됨.
cityName = value로 하면 끝!

현재 위치 지정이 안되고 디버깅창에 뭔가 많이 올라오는데... 모범답안 보면서 확인해야할듯
