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

---


# Chapter 10
## Class

### 기본구조

```python
class 클래스명:     // 클래스명 첫글자는 대문자로 작성
	def __init__(self, 속성1, 속성2):    // self를 첫번째 인자로 하지 않으면 문제가 발생
		self.속성1 = 속성1      // 초기화 과정
		self.속성2 = 속성2      // 초기화 과정

	def 함수명1(self, 매개변수):
```

### 인스턴스 생성

```python
class Student:
	def __init__(self, name, major, is_graduated):
		self.name = name
		self.major = major
		self.is_graduated = is_graduated
		
	# Method: 클래스 안에 구현된 함수
	def study(self):
		print(f'{self.name} 학생은 공부중입니다.')

# 인스턴스 생성
student_1 = Student('kwu', '소프트웨어학부', False)

# 각 속성 출력
print(student_1.name)

# 메소드 출력
student_1.study()
```

### 기본값 설정

```python
class Student:
	def __init__(self, name, major):
		self.name = name
		self.major = major
		self.is_graduated = False
		
	# Method: 클래스 안에 구현된 함수
	def study(self):
		print(f'{self.name} 학생은 공부중입니다.')

	def edit_major(self, new_major):
		self.major = new_major

# 인스턴스 생성
student_1 = Student('kwu1', '소프트웨어학부')

print(student_1.is_graduated)

# 인스턴스 속성을 수정. 직접적인 수정은 좋지 않은 방법 -> 함수를 만들어서 수정하는 것이 좋음
student_1.major = '전자공학과'

```

## 상속

```python
class 클래스 이름(상속할 클래스 이름)
```

### super()

- 부모 클래스의 임시적인 객체를 반환하여 부모 클래스의 메소드를 사용할 수 있게 해주는 함수
- 부모 클래스 정의한 내용을 가져옴
- super().__init__(): 자식 클래스에도 부모 클래스의 인스턴스 속성과 동일한 속성이 생성

```python
class ForeignStudent(Student):
	def __init__(self, name, major, country):
		super().__init__(name, major)
		self.country = country

foreign_student_1 = ForeignStudent('kw', '국어국문학과', '미국')
```

### 메소드 오버라이딩

- 부모 클래스에 있는 메소드를 동일한 이름으로 다시 만드는 것
- 부모 클래스의 메소드 대신 오버라이딩한 메소드가 호출된다.

```python
class ForeignStudent(Student):
	def __init__(self, name, major, country):
		super().__init__(name, major)
		self.country = country
		
	def study(self):
		print(f'{self.name} is studying.')
```

### 클래스 활용

```python
# 다른 파일에 있는 특정 클래스를 사용하고 싶을 때
import classes from Student, ForeignStudent

# 다른 파일에 있는 모든 클래스를 사용하고 싶을 때
import classes from *
```

# Chapter 11. 파일 다루기와 예외 처리

파이썬에는 FileNotFoundError, ZeroDivisionError, IndexError 등등 기본적으로 내장 예외들이 있음

## Python 에러 종류

1. ValueError: 부적절한 값을 가진 인자를 받았을 때 발생
2. IndexError: 인덱스 범위를 벗어나는 경우에 발생
3. SyntaxError: 파이썬 문법 오류가 발생하는 경우
4. NameError: 지역변수, 전역 변수 이름을 찾을 수 없는 경우
5. ZeroDivisionError: 0으로 나누려는 경우에 발생
6. FileNotFoundError: 파일이나 디렉토리에 접근하려 할 때, 해당 파일이나 디렉토리가 없는 경우 발생
7. TypeError: 잘못된 타입을 전달했을 때 발생
8. AttributeError: 클래스(모듈)의 객체에 해당하는 메서드나 속성을 잘못 호출하거나 대입했을 때 발생
9. KeyError: 딕셔너리에서 접근하려는 키 값이 없을 때 발생
10. OverFlowError: 오버플로우가 발생하는 경우

## 오류 예외 처리 기법

### try, except문

```python
# 실행할 코드
try:
	...

# 에러가 발생하였을 때 실행할 코드
# 발생 오류 종류: FileNotFoundError, ZeroDivisionError, IndexError, ...
except [발생 오류[as 오류 메시지 변수]]:
	...

# 에러가 발생하지 않았을 때 실행할 코드
else:
	...
```

### try … finally

- finally 절은 try문 수행 도중에 예외 발생 여부에 상관없이 항상 수행된다.
- 보통 finally 절은 사용한 리소스를 close해야 할 때에 많이 사용

```python
f = open('test.txt', 'w')
try:
	...
finally:
	f.close()
# try문을 수행한 후 예외 발생 여부와 상관없이 f.close()로 열린 파일을 닫는다.
```

### 여러 개의 오류 처리하기

```python
try:
	...
except 발생 오류 1:
	...
except 발생 오류 2:
	...
```

## 오류 일부러 발생시키기

- 프로그램이 작동하다가 의도하지 않게 돌아가는 것을 방지하기 위해 사용

```python
try:
    a = int(input("1~5 까지 숫자 입력 : "))

    if a < 1 or a > 5:
        raise

    print("a")
except:
    print("에러 발생")
```

```python
raise 발생 오류
```

```python
raise Exception("에러 메시지")
```

### 파일 읽기 / 쓰기

```python
파일 열기 모드: 'r', 'w', 'x'
f = open("파일 이름", '파일 열기 모드', [encoding = '인코딩 방식'])

# 파일을 더이상 사용하지 않으면 닫아주어야함
f.close()
```

with: 파일을 열고 닫는 것을 자동으로 처리해준다

```python
with open("파일 이름", '파일 열기 모드') as 파일의 별칭:
	수행할 작업
```

### 파일 읽기

```python
f = open("test.txt", 'r', encoding = 'UTF-8')

# read(): 파일의 전체 내용을 리턴
print(f.read())

# readline(): 개행 문자 전까지만 파일의 내용을 리턴
print(f.readline())

# readlines(): 파일의 모든 줄을 읽어서 각각의 줄을 요소로 갖는 리스트를 리턴
print(f.readlines())

f.close()
```

### 파일 쓰기

```python
# 'w'는 기존에 파일에 있던 내용을 전부 삭제하고 새로 씀
f = open("test.txt", 'w', encoding = 'UTF-8')

f.write("Hello")

f.close()
```

```python
# 'a'는 기존에 파일에 있던 내용에 이어서 작성(append)
f = open("test.txt", 'a', encoding = 'UTF-8')

f.write("Hello")

f.close()





