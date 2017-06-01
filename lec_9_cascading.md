Lec.9 Cascading
===============

CSS(Cascading Style Sheets)는 여러가지 스타일정보를 기반으로  
최종적으로 '__경쟁__'에 의해서 적절한 스타일이 반영된다.  


그렇다면? 무엇을 기준으로 브라우저는 속성을 반영할까?  


## 선언방식에 따른 차이

inline > internal > external(외부 css 파일)  

- - -

    span {
        color : red;
    }

    span {
        color : blue;
    }

위 두개의 span 태그 스타일 중 아래 span 태그의 속성(파란색)이 적용된다.  
즉, 같은 노드를 칭하는 태그는 가장 하단의 속성의 영향을 받는다.

- - - 

    body > span {
        color : red;
    }

    span {
        color : blue;
    }

위의 경우는 좀더 구체적으로 명시되어 있는 body > span 선택자의 속성이 먼저 적용된다.

- - - 

    <div id="a" class="b">
        text ...
    </div>

    #a {
        color : red;
    }                                                          

    .b {
        color : blue;
    }

위의 경우는 id값이 class값보다 우선순위를 가지기 때문에 red 속성이 적용된다.  
참고로, id > class > element.

- - -

## 좀더 자세한 정보는 구글에 'css specificity'로 검색해보면 된다.