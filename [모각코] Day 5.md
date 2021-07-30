# 모각코 Day 5 7/24
## 유데미 강의 13강
Climate app

### Get user's location
geolocation 이라는 패키지를 사용한다. https://pub.dev/packages/geolocator 참고
accuracy가 높을수록 사용자의 핸드폰이 무리를 하게 되므로 간단한 날씨 앱에서는 low 정도도 충분하다.
사용자에게 위치정보 사용에 관련해서 허락을 받고 위치정보를 받아내면 된다.

~~그런데 아무리 해도 위치정보가 콘솔에 print되지 않아서 이것저것 뒤져보니
getCurrentPosition을 할 때 강제로 실행시키초록 한마디 추가하면 되는것이었다. (forceAndroidLocationManager: true, 부분 추가함)
Position position = await Geolocator.getCurrentPosition(forceAndroidLocationManager: true, desiredAccuracy: LocationAccuracy.low);~~
또 안되어서 계속 찾아보다가 위에 적었던거 지우니 다시 됨.. 뭐가 문제였던건지 모르겠다


###  Async & Await
synchronous: 동시에 발생하는
asynchronous: 동시에 존재하지 않는
async를 사용하면 이미지 로딩처럼 오래 걸리는 기능은 백그라운드에서 진행되게 두고 나머지 기능을 돌아가게 하는 것
async: Be able to carry out time consuming tasks such as getting the GPS location form the phone. Can make time consuming tasks to happen in the background instead of happening in the foreground
async, await, Future 사용 예시

```
import 'dart:io';

void main() {
  performTasks();
}

void performTasks() async {
  task1();
  String task2Result = await task2();
  task3(task2Result);
}

void task1() {
  String result = 'task 1 data';
  print('Task 1 complete');
}

Future<String> task2() async {
  String result;
  Duration threeSeconds = Duration(seconds: 3);


  await Future.delayed(threeSeconds, () {
    result = 'task 2 data';
    print('Task 2 complete');
  });

  return result;
}

void task3(String task2Data) {
  String result = 'task 3 data';
  print('Task 3 complete with $task2Data');
}

```
결과:
Task 1 complete
Task 2 complete
Task 3 complete with task 2 data

Task 1이 완료된 뒤 Task 2는 Future.delayed로 인해 3초동안 잠시 멈추었다가 실행된다. Task 3은 Task 2를 기다렸다가 Task 2의 결과를 print하게 된다.
