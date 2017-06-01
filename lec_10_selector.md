Lec.10 selector
===============

css에서는 다양한 selector를 통해서 트리구조로 이루어진 돔의 태그들을 찾아갈 수 있다. 
- - - 

### tag로 지정
    span {
        color : red;
    }

    <span> Hello World ! </span>

태그 이름으로 속성 컨트롤 가능하다.  
구조안의 모든 동일한 태그에 속성이 적용된다.  

- - -

### id로 지정하기

    #nav-right {
        color : green;
    }

    <div id="nav-right">
        <p>nav바입니다.</p>
    </div>

html 구조에서 각각의 id값은 하나만 지정하는 것을 권장한다.  
id값은 #idname 으로 선택가능하다.

- - - 

### class로 지정하기

    .speical-class {
        font-size: 20px;
    }

    <div class="speical-class">
        <p>폰트사이즈는 20px</p>
    </div>

.classname을 통해서 특정 클래스 선택가능하다.

- - -

### id, class 요소 선택자와 함께 활용하기

    div#idname { color : red;}
    div.classname { color : blue;}

위와 같이 태그와 함께 id, class를 선택가능하다.  

- - -

### 그룹으로 선택하기

    h1, span, div { color : red;}
    h1, span, div#idname { color : black;}
    h1, div.classname { color : blue;}

여러 태그들을 그룹으로 선택가능하다.  
이때 각 태그들은 ','로 연결한다.  

- - -

### 그 외 다른 선택자와
__하위 요소 선택 (공백)__
    
    #daeweon span { color : red;}

    <div id="daeweon">
        <div>
            <span>선택</span>
        </div>
        <span>선택</span>
    </div>

__자식 선택(>)__

    #daeweon > span {color : red;}

    <div id="daeweon">
        <div>
            <span>선택안됨</span>
        </div>
        <span>선택</span>
    </div>

위 1번과 2번의 선택자의 차이는 하위 요소를 모두 포함하는가  
자식 요소만 포함하는 가이다.  
즉, '>'를 사용할 경우에는 #daewon 태그 바로 밑에 있는 span 태그만 속성이 적용된다. 

- - - 