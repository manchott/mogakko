# [모각코] TIL 정리

### 모각코에서의 목표
https://www.udemy.com/ 에서 Angela Yu의 Flutter 강의를 듣고 따라가고 최종적으로는 서비스를 할 수 있는 수준의 앱 만들기

2달의 기간동안 학습과 앱 만들기를 다 완료하기는 힘들었기에 2달동안 수업 수강을 목표로 바꿈

결과적으로 앱 초기설정부터 firebase cloud를 이용한 채팅 앱 만들기까지 총 15강 수업을 수강함


### 1일차 : Flutter 개발 환경 설정, 첫 앱 만들기
https://flutter.dev/docs/get-started/install/windows 참고

강의에서는 android studio를 기반으로 진행했지만 VScode가 더 손에 익어서 VScode에 맞춰서 개발 환경을 설정

또한 flutter의 기본 기능을 이용해 첫 앱을 만들어봄

특별한 기능 없이 그냥 명함과 비슷한 앱이었지만 container, Layout, widget 등등 flutter의 기초를 배울 수 있었음

약간 html과 비슷하다는 느낌을 많이 받았음

![image](https://user-images.githubusercontent.com/63185396/131211344-0ca01b14-a836-4a75-ad15-b61d8a3b2bc2.png)



### 2일차: 주사위 돌리기 앱
Stateful widget을 이용해 주사위를 누르면 주사위를 누르면 눈이 바뀌는 기능을 만듦

클릭 등의 외부 입력으로 인해 변화하는 state를 감지하고 이를 이용하는 stateful widget에 대해 배움

expand 등 앱의 layout을 설정하는 방법을 익힘

![image](https://user-images.githubusercontent.com/63185396/131211782-606a46f2-7a3a-4e1d-b0e9-9f94ace5a4d2.png)



### 3일차: 퀴즈 앱
퀴즈에 대해 true/false 버튼을 누를 수 있고 정답에 따라 하단에 체크 혹은 엑스 표시가 나타나는 앱을 만듦

이전의 앱들보다는 살짝 복잡해지며 프로젝트 관리가 필요해짐

abstraction, encapsulation 을 통해 코드를 관리하는 법을 배움

![image](https://user-images.githubusercontent.com/63185396/131212525-95b51f78-7ace-473a-bb32-23b4ff4ddb7e.png)



### 4일차: BMI 계산기
성별, 나이, 키, 체중 등을 입력하면 자동으로 BMI를 계산해주는 앱

지금까지는 widget을 그대로 이용했으나 custom을 통해 widget을 마음대로 바꾸는 법을 익힘

slider와 버튼을 통해 수치를 마음대로 정하고, Routes, Navigator를 이용해 두 페이지 사이를 오고가는 앱을 만듦

또한 자주 사용되는 상수와 style 등을 하나의 const 파일에 정리해서 한눈에 보기 편리하도록 함

![image](https://user-images.githubusercontent.com/63185396/131213076-278114b2-7766-45ce-84e6-461c08e3622c.png)



### 5-6일차: 날씨 앱
사용자의 위치에 따라 날씨를 알려주는 앱

강의자료를 보며 따라하다가 잘 안될때는 구글링이 최고의 무기라는 것을 깨달음

geoloacation 패키지를 이용해 사용자의 허락을 받고 위치정보를 받아온 뒤 날씨에 따라 나오는 이모티콘과 코멘트가 달라지도록 설정

날씨를 가져오는 과정처럼 시간이 걸리는 기능을 할 때 async, await을 사용하고, 로딩중 표시를 이용하는 법을 배움

![image](https://user-images.githubusercontent.com/63185396/131214647-ddecf74f-5d3d-4e00-b32d-b51a5f48a3ba.png)



### 7-9일차: 채팅 앱
firebase cloud를 이용한 채팅 앱

회원가입, 로그인, 채팅 기능 있고 채팅 내역, 회원 정보 등은 firebase를 통해 관리 가능

flutter의 장점중 하나인 애니메이션을 hero animation으로 구현

![image](https://user-images.githubusercontent.com/63185396/131214874-977a750a-adcf-4c41-a958-997896f308f7.png)



### 모각코를 마치며
- 좋았던 점
   - 혼자 시작했다면 끝마치지 못했을 강의를 목표까지 수강함
   - 강의에서 어려웠던 부분, 막혔던 부분을 팀원과 함께 논의함
   - 무언가 만들어냈다는 성취감

- 아쉬웠던 점
   - 나만의 앱을 직접 만들어보진 못함
   - 강의를 따라잡느라 급급함
   - 기간 지난 강의자료





