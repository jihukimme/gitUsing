# gitUsing
How to using git  

  1. Basic Git using
  2. Cooperation With Git
  3. How to use Markdown

* * *

# 1. Basic Git using

## 1.1 새 repository를 생성했을 때, 맨처음 git에 올릴 때
> 1. 터미널에 ```git init``` 을 먼저 해준다.  => 맨처음에 프로젝트를 올릴 때      
>   
>     
> 1. ```git add .``` => 파일 전부 다 올릴 때 사용
>    ```git add README.md``` => MarkDown파일 생성할 때 사용  
>    ```git status``` => 상태를 알려주는    
>    
>    
> 1. ```git commit -m 'history' ``` => 커밋에 대한 history
>     - ex:) git commit -m "first commit"    
>     
>     
> 1. ```git branch -M master``` => 기본 branch를 main으로 변경하기
>     - ex:) git branch -M main    
>    
>     
> 1. ```git remote add origin https://github.com/계정/리포지토리``` => 연결고리 만들기  
>    ```git remote -v``` => 연결한 주소 확인  
>    ```git remote remove origin``` => 기존 레포지토리의 remote를 삭제하고자 할 때     
>    
>    
> 1. ```git push origin master```를 통해서 origin master에 push


## 1.2 이미 존재하는 repository에 올릴 때
> 1. ```git remote add origin https://github.com/계정/리포지토리```  
> 2. git branch -M main  
> 3. git push -u origin main  






  



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



* * *


# 3. How to use Markdown
Markdown: 텍스트 기반의 마크업언어로 2004년 존그루버에 의해 만들어졌으며 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능하다. 특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다.  

> 1. 간결하다.
> 2. 별도의 도구없이 작성가능하다.
> 3. 다양한 형태로 변환이 가능하다.
> 4. 텍스트(Text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
> 5. 텍스트파일이기 때문에 버전관리시스템을 이용하여 변경이력을 관리할 수 있다.
> 6. 지원하는 프로그램과 플랫폼이 다양하다.  

## 3.1. Markdown 문법  

### 3.1.1. Header
- 6가지의 Header지원

```
# //This is a H1
## //This is a H2
### //This is a H3
#### //This is a H4
##### //This is a H5
###### //This is a H6
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6  




### 3.1.2. BlockQuote  

```
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.
```
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.



### 3.1.3. 목록

- 순서있는 목록(번호)

  순서있는 목록은 숫자와 점을 사용한다.  
```
1. 첫번째
2. 두번째
3. 세번째
```
1. 첫번째
2. 두번째
3. 세번째

- 순서없는 목록(글머리 기호: *, +, -)
```
* 글머리1.1
  * 글머리1.2
    * 글머리1.3

+ 글머리2.1
  + 글머리2.2
    + 글머리2.3

- 글머리3.1
  - 글머리3.2
    - 글머리3.3
```
* 글머리1.1
  * 글머리1.2
    * 글머리1.3

+ 글머리2.1
  + 글머리2.2
    + 글머리2.3

- 글머리3.1
  - 글머리3.2
    - 글머리3.3


  혼합사용 가능
```
* 글머리1
  - 글머리2
    + 글머리3
      + 글머리3.1
```
* 글머리1
  - 글머리2
    + 글머리3
      + 글머리3.1


### 3.1.4. Code Block

- 방법1  
<pre>
<code>
```
Code Block
```
</code>
</pre>

  
```
Code Block
```

<pre>
<code>
```java
public class Hello {
  public static void main(String[] args) {
    System.out.println("Hello, Jihu");
  }
}
```
</code>
</pre>

```java
public class Hello {
  public static void main(String[] args) {
    System.out.println("Hello, Jihu");
  }
}
```


- 방법2
```
<pre>
<code>
Code Block
</code>
</pre>
```

<pre>
<code>
Code Block
</code>
</pre>


### 3.1.5. 수평선

```
* * *

***

*****

- - -

---------------------------------------
```  

* * *

***

*****

- - -

---------------------------------------



### 3.1.6 링크  


[지후의 깃허브](https://github.com/jihukimme)
```
사용문법: [Title](link)
적용예: [지후의 깃허브](https://github.com/jihukimme)
```


지후의 깃 링크: <https://github.com/jihukimme>  
지후의 이메일링크: <jihu0210@naver.com>  
```
지후의 깃 링크: <https://github.com/jihukimme>
지후의 이메일링크: <jihu0210@naver.com>
```


### 3.1.7 강조

*single asterisks*  
_single underscores_  
**double asterisks**  
__double underscores__  
~~cancelline~~  

```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
~~cancelline~~
```



### 3.1.8 이미지 
```
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "Optional title")
```
![GitTestImage](Git_Test_Image.jpg "Test Image")

```
<img src="/path/to/img.jpg" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="RubberDuck"></img><br/>
<img src="/path/to/img.jpg" width="40%" height="30%" title="px(픽셀) 크기 설정" alt="RubberDuck"></img>
```

<img src="Git_Test_Image.jpg" width="40%" height="30%" title="px(픽셀) 크기 설정" alt="Cat"></img>



### 3.1.9 줄바꿈
3칸 이상 띄어쓰기( )를 하면 줄이 바뀐다.

```
* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다. 
이렇게

* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다.___\\ 띄어쓰기
이렇게
```

* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다. 
이렇게

* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다.   
이렇게



* * *
