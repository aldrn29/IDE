## 디버깅(debugging)이란?
컴퓨터 프로그램이나 시스템의 정확성 또는 논리적인 오류(버그)를 검출하여 제거하는 과정

#### 디버깅 용어

- Resume: 다음 브레이크 포인트를 만날 때까지 진행
- Step into: Methode를 포함한 라인을 만나면 Mothod 안으로 진입
- Step over: 다음 라인으로 이동, Method가 있어도 안으로 진입하지 않고 다음 라인으로 이동
- Step Return: 현재 Method에서 즉시 Return
- Drop to Frame: Method를 처음부터 다시 


#### 단축키

||Visual Studio | Eclipse | IDEL |
|---|---|---|---|
|시작 |Ctrl + F5|Ctrl + F11|F5|
||
|디버깅 모드 실행 | F5 | F11 |
|디버깅 모드 중단 | Shift + F5 | Ctrl + F2 |
|중단점 설정/해제 | F9 | Ctrl + Shift + B |
|모든 중단점 해제 | Ctrl + Shift + F9 ||
||
|다음 중단점을 만날때까지 실행 | F5 | F8 |
|프로시저 단위 실행 | F10 | F6 |
|한 단계씩 코드 실행 | F11 | F5 |
|F11로 실행한 후 단계에서 빠져나오기 |Shift + F11||
||
|(오류 메시지가 출력됐을 때) 오류 메시지가 발생한 줄로 이동 |F4||
