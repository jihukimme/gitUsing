# gitUsing
How to using git

* * *

# 1. Git basic using

> 1. 터미널에 ```get init``` 을 먼저 해준다.  => 맨처음에 프로젝트를 올릴 때  
> 
> 1. ```git add .``` => 파일 전부 다 올릴 때 사용  
>    ```git status``` => 상태를 알려주는  
> 
> 1. ```git commit -m 'history' ``` => 커밋에 대한 history  
> 
> 1. ```git remote add origin https://github.com/계정/리포지토리``` => 연결고리 만들기  
>    ```git remote -v``` => 연결한 주소 확인  
>    ```git remote remove origin``` => 기존 레포지토리의 remote를 삭제하고자 할 때  
> 
> 
> 1. ```git push origin master```를 통해서 origin master에 push  

  



* * *  


# 2. Git으로 협업하기 

## 2.1. Create Repository
   Repository를 생성해 협업을 진행할 저장소를 생성한다.  
   만든 저장소  
   
### Or Git 클론하기 (이미 만들어져있는 저장소 함께 쓰기)
> 상대방이 만든 저장소를 함께 사용하기
> 
> 1. 상대방이 만든 저장소로 들어가서 초록색 Code 버튼을 누르고 HTTPS탭을 선택한 뒤 url을 복사해준다.
> 1. Visual Studio를 켠 뒤 shift + command + p 를 입력한다.
> 1. 그 다음 Git:Clone을 클릭한다.
> 1. 위에서 복사한 url을 붙여넣고 엔터를 쳐주고 원하는 곳에 저장한다.


  
## 2.2. 새 Branch 만들기(나만의 공간 만들기)    
   공용으로 사용하는 저장소는 함부로 바꾸면 안된다.  
   
> 클론한 저장소는 기본적으로 공용으로 사용하는 main 브랜치에 있다.  
> 그렇기 때문에 나만 코드를 바꿀 수 있는 공간(Branch)을 따로 만들어준다.  
> Git Clone 할 때와 마찬가지로 shitf + command + p 를 입력한다.  
> 그리고 Create 라고 치면 Git: Create Branch가 보일 것이다. 이를 클릭한다.  
> 원하는 이름을 적어주고 엔터를 눌러주면 브랜치가 생성된다.  




## 2.3. 나의 코드 저장하고 저장소에 올리기 (Commit & Push)  

> 나의 브랜치에서 코드를 작성하고 저장(커밋)해준다. -> 커밋 방법: 1. gitBasicUsing 참고  
> 왼쪽 탭에 가지모양(소스제어)을 눌러주고 커밋할 내용을 적은 다음 체크버튼을 눌러준다.  
> 그리고 이렇게 저장한 내용을 푸쉬를 해야 원격 저장소에 저장이 된다. ->   체크버튼 옆옆에 3개 점모양 버튼을 누르고 Push를 눌러주면 원격 저장소에 내 브랜치의 커밋이 저장된다.  
> 
> 
> ### 나의 브랜치에 코드를 커밋한 후, 공용 저장소에 내 코드를 넣어 달라 요청하기(Pull Request)
>    git의 협업 프로젝트(해당 레포지토리)로 가서 Pull Requests 탭을 눌러준다.


## 2.4. 공용 저장소와 나의 브랜치 합치기(Git Merge)
### 터미널에서 진행
> 1. ```git checkout develop```    //현재 브랜치를 'develop'으로  
> 1. ```git fetch```    //pull하지 않고 원격과 로컬을 비교  
> 1. ```git pull```    //  
> 1. ```git merge Feat/김지후```    //현재 브랜치인 'develop'과 'Feat/김지후'를 merge  
> <merge 후 커밋 진행 . .>  
> ```git add .```  
> ```git commit - 'merge 완료'```
  

#### 기타 터미널 명령
>    ```git fetch``` // pull 하지않고 원격과 로컬 비교  
>    ```git pull origin develop``` //develop 최신껄로 pull 하기  
> 
>    ```git branch Feat/컴포넌트``` // Feat/컴포넌트라는 자신이 작업할 브랜치 생성  
>    ```git switch Feat/컴포넌트``` // Feat/컴포넌트로 이동  
> 
>    ```git add .```  
>    ```git commit –m ‘컴포넌트 작업 완료’```  
>    ```get push —set-upstream origin Feat/컴포넌트``` // 세팅된 upstream(원격저장소)에 푸쉬  
>   
>    Git hub에서 Compare & pull request 클릭 후  
>    base를 업로드할 곳으로 설정 후 Creat pull request하기  


    






    
