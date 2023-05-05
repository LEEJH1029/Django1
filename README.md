# Django1
hello world

> Django 스터디
------

## Member
> 조현호 고우석 김재윤 이정현

## Date
> 매주 월요일 오후 9시


-----

# Chapter4. Git & Github

## Git의 구조
<img width="1401" alt="git_structure" src="https://user-images.githubusercontent.com/67615226/229673845-10cf22fe-f34b-4fa4-aec3-bd5107a0874a.png">

  - working directory: 현재 작업 중이 프로젝트가 위치한 디렉토리
  - Staging: commit 할 파일의 예비 저장소
  - Local Repository: 각 컴퓨터의 git이 관리하는 로컬 저장소
  - Remote Repository: 외부에 위치한 원격 저장소
------

## Git의 사용
  ### git 저장소 만들기
<img width="824" alt="git_init" src="https://user-images.githubusercontent.com/67615226/229673870-4201bec6-48f6-4216-9764-a39cfef2384c.png">

    - 나의 프로젝트가 위치하 곳으로 이동 후 터미널에서 명령 실행
    - git init: 현재 디렉토리에서 git을 사용할 수 있도록 초기화
    - .git 디렉토리: Staging, Local Repository가 들어있음
    - .gitignore: 같은 위치에 있는 파일을 git에서 무시 ex) 데이터베이스 계정, 클라우드 시크릿 키, 각종 민감 정보
   
  ### 버전 만들기
  
   <img width="772" alt="git_status" src="https://user-images.githubusercontent.com/67615226/229673924-ffe22fbd-8c26-48a2-af71-12f2ae431266.png">

    - git status: git 상태를 확인하기 위한 명령어
      - on branch main: 현재 main 브랜치에 있음
      - No commits yet: 아직 commit한 파일이 없음
      - untracked files: 버전을 아직 한 번도 관리하지 않은 파일
    
   <img width="773" alt="git_add" src="https://user-images.githubusercontent.com/67615226/229674001-f95a064b-81b1-493e-9b8e-4bd08845b96e.png">

    - git add <file>: working directory -> staging
    - git add . : working directory에 있는 모든 파일을 staging에 이동
    - git commit -m " " : staging -> local repository

   <img width="637" alt="git_log" src="https://user-images.githubusercontent.com/67615226/229674155-2ccbd6ea-dc49-4c2b-8dc7-e504742514e3.png">

    - git log: 저장소에 저장된 버전을 확인할 때 사용
    - git pull origin main : 원격 저장소에서 commit을 pull할 때 사용하는 명령어
    - git commit -am " " : staging과 commit을 한 번에 처리, 한 번이라도 commit한 적이 있는 파일을 다시 커밋할 때만 사용 가능
 
## Github에 소스 반영
    - git remote add origin <원격저장소의 주소> : 원격 저장소에 origin(github 저장소 주소)을 추가하겠다고 git에게 알려 주는 명령어
        ex) git remote add origin https://github.com/LEEJH1029/Django1.git
     
    - git push -u origin <브랜치명> : 지역 저장소의 브랜치를 origin의 브랜치로 push하라는 명령어
      - -u: 지역 저장소의 브랜치를 원격 저장소의 브랜치에 연결하기 위한 옵션. 처음 한 번만 사용하면 됨
      ex) git push -u origin main
  
## Github로 협업하기
  <img width="700" alt="git_branch" src="https://user-images.githubusercontent.com/67615226/230717041-d5e0b3c1-0c03-4d0e-b44e-febfb9fd9718.png">
  
    - git clone <원격저장소의 주소> : 원격 저장소 -> 지역 저장소 복제
        ex) git clone https://github.com/Likelion-Kwangwoon/Django1.git
  
  <img width="764" alt="branch" src="https://user-images.githubusercontent.com/67615226/230718057-423fdfa5-631b-4fb0-bb5a-179e434f9f6d.png">
  
    - git checkout -b <브랜치명> : branch를 새로 만들고 해당 branch로 이동
    - git checkout <브랜치명> : <브랜치명>으로 이동
    - git merge <브랜치명> : 현재 있는 branch로 <브랜치명>을 병합
  
  <img width="871" alt="branch_merge" src="https://user-images.githubusercontent.com/67615226/230717634-0097e33a-ce90-40a0-b7bd-4a83e7ffabe6.png">
  
  ---
  
    - git branch <브랜치명> : branch 생성
    - git switch <브랜치명> : <브랜치명>으로 이동
## 챕터 5 - 변수와 자료형
------
- 변수 선언
    - greeting = “Hello World”
- 주의 사항
    - 변수 사이에 공백 허용되지 않음
    - 단어 사이는 _ 로 연결
    - 문자열은 숫자/특수문자로 시작이 불가
    - 예약어 변수로 선언 불가
    - 가급적 소문자 사용

**문자열**
- upper, lower, strip 함수
- removeprefix 함수 : 특정 문자열 변수에서 없애고 싶은 부분을 지울 수 있음
- replace 함수 : replace(”A”, “B”)를 통해 A를 B로 변경할 수 있음
- f string : 변수와 문자열을 혼합해서 사용하기 위함
    - Ex) print(f”{변수})

**숫자**
- 정수, 실수 기억할 것
- +, -, *, / 와 같이 사칙 연산 가능
- 문자열 - 숫자 간 변환 기억할 것
    - str(), int(), float()

**논리형**
- True, False

**명령 프롬프트**
- text = input(”설치 진행하겠습니까 ? ”)
------
## 챕터 6 - 조건문과 반복문
------
**조건문**
- If 문

![image](https://user-images.githubusercontent.com/87240205/230898896-cefbb653-f4e0-4fc2-9382-591bd83b8edc.png)

**반복문**
- for 문
- while 문
------

## 챕터 7 - 자료구조
------
### 목차: 리스트,튜플,딕셔너리
------
## 리스트
*선언

 list=[]
숫자,문자형 상관없음 (자료형 신경 쓸 필요가 없음)


``` python
lst=[]
```

*추가 ,
리스트 맨 뒤에 추가
``` python
lst.append(value)
```


*추가 2,원하는 위치에 삽입	

``` python
lst.insert(index,value)
```

*제거(데이터 삭제)
``` python
del lst[index]
```

*제거 2(데이터 삭제 ~> 반환)


index를 넣는 경우도 있지만 잘 사용 x
``` python
lst.pop(index)
```


*제거 3(리스트에서 직접 값을 찾아서 삭제)
``` python
lst.remove(value)
```

*정렬 (c++ 정렬과 동일)(원본이 정렬됨)
``` python
lst.sort()
```

*정렬2(원본은 유지한 채 정렬된 새로운 리스트 만들고 싶을 때) 
``` python
new=sorted(lst)
```

*역순정렬 
``` python
lst.sort(reverse=True)
```

*슬라이싱(리스트 함수 중 제일 중요하다고 생각함)
(start<= <end,jump는 몇 칸씩 이동할지)

``` python
lst[start:end:jump]
```

(0<= <4)
``` python
lst[:4]
```

(1<= <=end)
``` python
lst[1:]
```

(리스트 제일 뒤에서 하나 출력도 가능)
``` python
lst[-1]
```

(역순으로도 필요한 만큼 출력도 가능)

3번 인덱스 부터 0번 인덱스까지 역순으로(3,2,1,0) 
``` python
lst[3::-1]
```
* [deep copy,shallow copy] (https://wikidocs.net/16038)

* 반복문 
``` python
for i in lst:
     print(i) #기본이 출력후 줄바꿈
```
* 최대,최소,합
``` python
max(lst)  
min(lst)
sum(lst)
```



------
## 튜플
* 선언
``` python
tup=()
```
* 리스트로 변환법
``` python
list(tup)
```

* 함수
``` python
tuple(lst).index(5)#튜플 안에 5 값을 찾아서 그 인덱스를 반환
tuple(lst).count(2)#lst안에 값이 몇 개 있는 지 출력
```
------
## 딕셔너리(key:values)
* 선언
``` python
student={'student num':'12345','major':'CS'}
```
``` python
student['major']#'CS' 출력
```
* 추가
 ``` python
student['성적']=4.0 # {'student num': '12345', 'major': 'CS', '성적': 4.0}
```
* 수정
``` python
student[value]=new value
```

* 삭제
``` python
del student[value]#키값을 찾아서 key:values 모두 삭제
```

* 함수 
``` python
student.get('student num')#key 를 넣으면 value'12345' 출력
```
``` python
a = {'name': 'pey', 'phone': '010-9999-1234', 'birth': '1118'}
a.keys()#출력 dict_keys(['name', 'phone', 'birth'])
```
``` python
a.values()#dict_values(['pey', '010-9999-1234', '1118'])

```

``` python
a.items()#dict_items([('name', 'pey'), ('phone', '010-9999-1234'), ('birth', '1118')])
```

``` python
 a.clear()# 딕셔너리 안에 있는 모든 값 삭제
```
## 보통 그대로 사용하기 보다는 list(a.함수()) 이런 방식으로 리스트로 바꿔서 사용

* 딕셔너리에서의 반복문 
``` python
for key,value in student.items():#key값과 value 모두 출력됨
       print(key,value)
for i in student:#key 값만 출력됨
    print(i)
```

## chapter 12
  ### web의 등장

웹 1.0 :web이 탄생한 1990년부터 웹 2.0 전인 2004년 정도까지의 기간을 우리는 웹 1.0이라고 부릅니다 
*  웹 1.0의 특징으로는 사용자와 생산자가 구분되어 사용자들이 정보를 단순히 소비하는 것입니다.




