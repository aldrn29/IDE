## Anaconda 설치 및 환경구성
#### 1. Anaconda 설치
- 환경변수 설정
#### 2. 환경 구성
- Anaconda Navigator - Environments - Create - 환경이름 설정
#### 3. 환경 사용하기
- Anaconda Navigator에서 필요한 Package를 검색하여 설치
- 터미널에서 pip install 패키지이름  ex) pip install numpy

![](https://github.com/aldrn29/IDE/blob/master/image/anaconda_2.JPG?raw=true)

## VS code와 Anaconda 연동

#### 1. VS code에서 Extensions - Python과 Code Runner 설치 - 재실행  
![](https://github.com/aldrn29/IDE/blob/master/image/vscode_1.JPG?raw=true)

#### 2. Python 인터프리터 지정
##### 1) Command Pallete(ctrl+shift+P) - Python: Select Interpreter - Anaconda에서 생성한 환경 선택   
![](https://github.com/aldrn29/IDE/blob/master/image/vscode_2.JPG?raw=true)  

##### 2) json 파일에 삽입  
  : 'File > Preferences > Settings'(Ctrl+,) - Workspace - Command Pallete(ctrl+shift+P) - Open Settings(Json)
```
"python.pythonPath":"인터프리터 설치경로\\python.exe"
```

#### 3. conda 환경 활성화
- 터미널에서 Anaconda prompt를 시작   
  : 아래 명령으로 conda 기본 환경이 활성화되며, 이후는 activate 명령으로 환경을 변경할 수 있음  ex) conda activate 환경이름(ex: py38)
```
C:\\Anaconda 설치경로\\Scripts\\activate.bat C:\\Anaconda 설치경로
```   
- 혹은 VS code 시작할때마다 위 명령이 실행되도록 설정하기
  - json 파일에 삽입   
  : 'File > Preferences > Settings'(Ctrl+,) - terminal.integrated.shellArgs.Windows 검색 - Edit in setting.json 클릭  
  ![](https://github.com/aldrn29/IDE/blob/master/image/vscode_3.JPG?raw=true)
  
```
"terminal.integrated.shell.windows": "C:\\Windows\\System32\\cmd.exe",
"terminal.integrated.shellArgs.windows": ["/K", "C:\\Anaconda설치경로\\Scripts\\activate.bat C:\\Anaconda설치경로 & conda activate 사용할 conda env 이름"]
```   
![](https://github.com/aldrn29/IDE/blob/master/image/vscode_4.JPG?raw=true)
(특정 환경 사용시에만 뒤에 '& conda env 이름'이 추가됨)  
