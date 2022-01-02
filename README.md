# CodeLion_MyPortpolio

본 레포지토리는 멋쟁이 사자처럼 10기 운영진 교육 중 코드라이언 HTML/CSS 부분의 학습 내용 정리 및 실습 목적으로 사용됩니다.

------

- HTML, CSS : 다른 언어와의 콜라보를 위해 (cf. 워드, 한글 등)

### < 나의 이력서 만들기 >
- 각 제목의 폰트는 모두 동일함
- 제목 하위의 내용 해당 부분의 폰트 및 크기는 모두 동일함 (제목과는 다름)

### < HTML과 인사하기 >
- <가방1>내용물입니다.</가방1> : 태그의 시작과 끝의 형태로 코드 구현
- H1 태그: Heading 1을 의미, H 옆 숫자는 1부터 숫자가 커질수록 글자 크기가 작아짐 - 제목을 작성할 때 주로 사용

### < 문서의 골격 >
- ``` html > head > body > title > meta > div > a > script > link > img > span > p > li > ul > h1 > i ``` : 수많은 태그가 존재
- ``` html ``` 태그 & ``` <!DOCTYPE html> ``` : html 문서에 꼭 써주는 태그
    ``` 
        <!DOCTYPE html>
        <html>
        </html>
    ```
- ``` <head> ``` 태그 : 문서의 정보를 담는 부분 -> 문서 작성자, 참고자료, 대표이미지, 키워드 검색 정보
- ``` <body> ``` 태그 : html 문서의 모든 내용
- ``` <html> ``` 태그는 크게 ```<head> <body> ``` 태그의 두 부분으로 나뉨
- 영어 기반의 html 문서로 인해 한글을 쓰기 위해서는 ```<meta charset="UTF-8">``` : characterset을 meta 태그로 추가해주어야함 (meta 태그는 />으로 닫지 않음)
- ```<title>``` 태그 : 검색결과의 상단바에 뜨는 타이틀 ex) title 태그 내부에 작성한 내용이 그 페이지의 제목이 됨 - head태그 내부에 넣어주어야 함.

### < css와 인사하기 >
- ``` <footer> ``` 태그 : 저작권 명시 등의 내용
- html: 문서의 요소를 구분하는 역할, 그 요소에 의미를 부여하는 역할
    - p : 문단 의미 
    - footer : 화면의 하단 정보 의미
- css: 화면의 적절한 위치에 배치
    - 사용하는 css 파일은 html 파일의 head 태그에 들어감 <정보를 담는 부분>
    - ``` <link rel="stylesheet" href="codelion.css">``` 와 같이 link 연결, />으로 닫지 않음
    - css파일의 속성 순서는 존재하지 않음 -> 어떻게 써도 문제 없음

### < 가독성 챙기기 >
- px : pont element의 준말, font-size의 속성 값으로 사용될 경우 px 값을 다르게 부여함으로써 글자 크기 변경 가능
- ``` class ``` 사용 : 같은 태그 내에서 다른 css를 적용시키고자 할 때 class를 다르게 주어 구별할 수 있음
    - class의 이름은 반드시 " " 또는 ' ' 으로 묶어주어야 함
    - class의 이름에 css를 적용시켜주고자 할 때에는 ```.class_name { }```으로 묶어서 작성해야함 -> .을 추가하지 않을 경우 이는 태그로 인식됨


### < 중앙에 배치하기 >
- html color code 를 통해 다양한 색상 선정 가능
- ```<div>``` 태그: 여러 태그를 묶어 하나의 영역으로 만들어줌 (division)
- border: ``` border: 두께 방식 색깔; ```
- width: 화면에 태그를 띄울 때 폭을 얼마로 할지
- text-align: 글자만을 가운데 정렬
- div 박스를 가운데로 정렬하고 싶다면 ? ``` margin-left: auto; margin-right: auto; ``` 를 추가하여 중앙 배치

### < 박스 쪼개기 >
- ```border```를 추가했을 때 내용물 자체의 크기는 변하지 않음
- 박스의 전체 크기: (width + 테두리 두께) * (height + 테두리 두께)
- ```padding```을 추가했을 때는 내용물 자체의 크기가 변함
- ```margin```을 추가했을 때는 두꺼운 옷을 입은 것과 같음

### < 그림자 표현하기 >
- ```box-shadow: 0 1px 20px 0 rgba(0,0,0,0.1); ```
    - 0 : 가로축(x축)으로 그림자가 얼만큼 뻗어나갈지 정해주는 값
    - 1px : 세로축(y축)으로 그림자가 얼만큼 뻗어나갈지 정해주는 값
    - 20px : 블러처리가 얼마나 뻗어나갈지(흐림정도)
    - 0 : 그림자의 퍼짐정도
    - rgb(red, green, blue) : 0 ~ 255
    - rgba(): a - 0 ~ 1 사이의 투명도를 가진 값 (0:투명, 0.1: 10%, 1: 100%)

### < 구글 웹 폰트 사용하기 >
- css폰트에 ```@import url('https://fonts.googleapis.com/css?family=Montserrat:100,200,300,400,500,600,700,800&display=swap');``` : Montserrat 폰트 추가
-  ```* { }``` : 모든 태그에 해당 css를 적용 -> ```font-family: 'Montserrat';``` : 몬세라트 폰트를 적용
- 기본 속성 값을 같도록 함
    ```
    body,h1,h2 {
        margin: 0px;
        padding: 0px;
    }
    ```
- ```<section>``` 태그: division과 같은 기능, html 태그를 꾸며주기 위해 묶어주는 태그
    - div를 묶어주는 역할도 함 ex) ```article```

### < About Me 제작하기 >
- 의미 없는 텍스트로 일단 채워놓는 (디자인을 보기 위해 사용하는) : Lorem ipsum
- 이탤릭체로 글자를 기울이기 : ```    font-style: italic;```
- 아래에만 테두리가 생기도록 : ```border-bottom: 1px solid #ebebeb;```

### < 나만의 이력서 작성 중 기록 내용 >
- ```line-height: 16px;```을 통해 줄 간 간격을 조절
- 각 ```<p>``` 태그를 좌우정렬 하고 싶을 떄 -> ```text-align: left; text-align: right;```로 하면 다른 줄에서 정렬이 됨
    - ```float```를 사용 : 왼쪽, 오른쪽에 붙어서 동작