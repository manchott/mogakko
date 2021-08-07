# 모각코 Day 8 8/7
## 유데미 강의 15강 이어서
Flash Chat


### Animated Text
https://pub.dev/packages/animated_text_kit 참고
음.. 기존의 Text 부분을 바꾸면 될 정도로 간단함.
다만 많이 달라져서 직접 Readme를 읽고 수정했음.
 

### Code Refactoring
const로 decoration 등의 틀을 만들고 그 안에서 수정을 하고 싶다면 .copywith를 사용해서 수정하면 됨. Theme을 내맘대로 수정할 때 쓰던 방법
주기적으로 refactoring해야 코드가 깔끔해진다


### Firebase
Firebase를 이용해서 유저가 로그인해서 우리 서비스를 이용할 수 있게 만들 것이다.
https://firebase.google.com/
문제가 생기면 여기를 확인해보라 함: 
https://blog.londonappbrewery.com/troubleshooting-firebase-x-flutter-a974b2645689

cloud firestore: 클라우드에 데이터를 넣는 방법.
Authentication: 유저 등록하고 로그인 할 수 있게 함

https://pub.dev/publishers/firebase.google.com/packages firebase 참조
firebase를 가지고 작업을 한다면 꼭 firebase_core를 넣어야함. 기본이 되는 토대인듯


### ID, password 입력받기

```
// Registration
TextField(
              keyboardType: TextInputType.emailAddress,   // email 전용 키보드가 나옴
              textAlign: TextAlign.center,
              onChanged: (value) {
                email = value;
              },
              decoration:
                  kTextFiedlDecoration.copyWith(hintText: 'Enter your email'),
            ),
SizedBox(
              height: 8.0,
            ),
TextField(
              obscureText: true,      // 비밀번호를 검은 동그라미로 가림
              textAlign: TextAlign.center,
              onChanged: (value) {
                password = value;
              },
              decoration: kTextFiedlDecoration.copyWith(
                  hintText: 'Enter your password'),
            ),
```          

그리고 강의에서 시키는대로 쭉 했는데 뭔가.. 어찌저찌 이메일 등록이 됨..
