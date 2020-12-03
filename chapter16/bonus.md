## CSS 가상클래스
* 가상클래스 : 가상클래스는 요소의 이벤트에 대응하기 위해 미리 만들어 놓은 클래스다. 별도의 class를 지정하지 않아도 지정한 것 처럼 할 수 있다.

### 가상클래스의 종류
* link : 하이퍼링크가 적용된 요소
* visited : 링크 요소를 한 번 이상 방문한 요소
* hover : 요소에 마우스가 올라간 상태
* active : 링크 요소가 활성화된 상태 / 마우스가 누르고 있을 때
* focus : 폼요소가 선택된 상태, 입력대기모드

### 사용법
* 선택자로 사용시 요소명 : 가상클래스 이름과 같이 사용
* 선택자로 사용시 요소명 아이디 또는 클래스 선택자가 올 수 있다.
```
        a:link{color: #000;}
        .visited:visited{color:#f00;}
        .hover:hover{color: #0f0;}
        .active:active{color: #fc0;}
        .focus:focus{background-color: #f00;}
```

## CSS 가상요소
* 가상요소는 문서의 특정위치, 특정영역, 특정요소를 선택하기 위해 미리 만들어 놓은 선택자이고, 존재하지 않는 요소를 존재하는 것처럼 한다.

### 가상요소의 종류
* first-letter : 문장의 첫글자
* first-line : 문장의 첫줄
* first-child : 연속되는 자식 요소 중 첫 번째 자식
* before : 실제 내용 바로 앞에서 생성되는 자식요소
* after : 실제 내용 바로 뒤에서 생성되는 자식요소​
    * before와 after을 사용하기 위해서는 content라는 속성이 꼭 필요하다.
    * content : HTML 문서에 정보로 포함되지 않은 요소를 CSS에서 새롭게 생성시켜준다

### 사용법
* 선택자로 사용시 요소명 : 가상요소 이름과 같이 사용
* 선택자로 사용시 요소명 대신에 아이디 또는 클래스 선택자를 사용할 수 있다.
```
        .letter:first-letter{font-size: 50px;}
        .letter:first-line{color: #f00;}
        .list li:first-child{color: #f0f;}
        .list li:last-child{color: #0f0;}
        .txt01:before{content: '*앞쪽';}
        .txt02:after{content: '뒤쪽*';}
```

## CSS 코딩 컨벤션
```
1. display(표시)
2. overflow(넘침)
3. float(흐름)
4. position(위치)
5. width/height(크기)
6. padding/margin(간격)
7. border(테두리)
8. background(배경)
9. color/font(글꼴)
10. animation
11. 기타

1~6 레이아웃  |  7~8 테두리/배경  |  9 글꼴  |  10 동작  |  11 기타  

```