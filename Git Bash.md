## User

#### 사용자 인증정보 설정
```
$ git config user.name "aldrn29"                    // 로컬
$ git config user.email aldrn29@gmail.com
$ git config --global user.name "aldrn29"           // 전역
$ git config --global user.email aldrn29@gmail.com
```  

#### 사용자 정보 삭제
```
git config --unset user.name                        // 로컬
git config --unser user.email
git config --unset --global user.name               // 전역
git config --unset --global user.email
```   

#### 사용자 리스트 확인
```
git config --list 
git config --global --list
``` 




## Git Repository

#### 저장소 생성
기존의 디렉토리를 git repository로 설정 (프로젝트 디렉토리에 __.git__ 디렉토리가 생성)
```
git init                                            // 현재 디렉토리에 저장소 생성
git init project1                                   // 현재 디렉토리에 이름이 'project1'인 저장소 생성
```

#### 파일 추가 (Working area -> Staging area)
```
git add .                                           // 모든 파일 추가
git add comment.js                                  // 특정 comment.js 파일 추가
```

#### 파일 삭제 (Working area <- Staging area)
```
git reset
```   

#### 상태 확인 (Staging area)
```
git status
```

#### 저장소 반영 (Staging area -> Git repository)
```
git commit -m "message"
```   

#### 저장소 반영 내용 변경   
```
git commit --amend -m "message"
```

#### 저장소 반영 내역 확인
```
git log
git lot -p -2                 // -p: 각 commit의 수정 결과 확인, -s: 상위 n개의 commit만 출력
git log --stat                // 어떤 파일이 commit에서 수정되고 변경되었는지 확인
git log --pretty=online       // 각 commit을 한 줄로 출력
git log --graph               // commit간의 연결된 관계를 아스키 그래프로 출력 (Branch 상태확인 시 유용!)
git log -S tt                 // 코드에서 추가되거나 제거된 내용 중 특정 텍스트(tt)가 포함되어 있는지 검사
```




## Git Branch

#### 브랜치 확인
```
git branch
```   

#### 브랜치 생성
```
git branch test                                     // 이름이 'test'라는 브랜치 생성 
```

#### 브랜치 전환, snapshop 이동
```
git checkout test                                   // master -> test로 HEAD 포인터 이동
git checkout <snapshot hash>
```   

#### 메인 브랜치 변경
```
git branch -M main                                  // master -> main
```

#### 브랜치 병합    

```
git merge test                                      // master에 test를 병합 (현재 위치: master Branch)
```

#### 브랜치 병합 내용 확인
```
git branch --merged
```

#### 브랜치 삭제
```
git branch -d test                                  // 이름이 'test'라는 브랜치 삭제
```




## Git Remote

#### 원격 저장소 받아오기 
```
git clone https://github.com/aldrn29/~.git
```   

#### 원격 저장소를 로컬 저장소와 연결
```
git remote add origin https://github.com/aldrn29/~.git
```

#### 원격 저장소 이름 변경
```
git remote rename origin git_test                   // origin -> git_test
```

#### 원격 저장소 삭제
```
git remote rm git_test                              // 이름이 'git_test'인 원격 저장소 
```

#### 저장소 갱신

* Pull: 원격 저장소에서 데이터 가져오기 + 병합(Merge)
* Fetch: 원격 저장소에서 데이터 가져오기
```
git pull                                            // HEAD->master(로컬) + origin/master(원격)

git log origin/master
git merge origin/master
```

#### 저장소 발행
```
git push origin master                              // 로컬 저장소에서 작업한 내용을 원격 저장소에 반영
```


-----------------------
<br>
## 요약!

```
git add .
git commit -m "message"
git push origin
```

<br>  

