### 사용자 인증정보 설정
```
$ git config --global user.name "aldrn29"
$ git config --global user.email aldrn29@gmail.com
```

### 사용자 정보 삭제
```
git config --unset user.name                // 로컬
git config --unser user.email
git config --unset --global user.name       // 전역
git config --unset --global user.email
```

### 사용자 리스트 확인
```
git config --list 
git config --global --list
```

### remote
```
git remote add origin https://github.com/aldrn29/~.git
```

### init
```
git init
```

### clone
```
git clone https://github.com/aldrn29/~.git
```

### branch master->main
```
git branch -M main
```


```
git add .
git commit -m "message"
git push
```
