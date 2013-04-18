{
    "title": "하루프레스 시작하기 4",
    "author": "s0und0ne Kang",
    "date": "2013-04-18T12:27:46.479Z",
    "categories": [
        "haroopress",
        "util",
        "tool"
    ],
    "tags": [
        "haroopress",
        "blog",
        "util",
        "tool"
    ],
    "acceptComment": true,
    "acceptTrackback": true,
    "published": "2013-04-18T12:27:46.479Z",
    "status": "publish",
    "important": false,
    "advanced": {}
}


> haroopress 를 설치하고 바꾸고 싶은 부분들이 있어서 수정하려고 찾아본 내용들이다.
(당분간 이것저것 바꾸면서 테스트해봐야겠다.)

## 1. 블로그 이름 바꾸기

> 나중에 정리하자 ^^;;



## 2. 블로그 테마 수정하기

    haroopress 에서는 현재(2013.02.09) 총 7개의 테마를 제공하고 있다.
    - basic, basic-for-haroopress, clean, dark, node, wood-dark

### <font color="yellow">Before</font>

블로그에 적용되는 테마를 수정하려고 한다.

* 테마의 종류는 config.js 파일에서 수정한다.
* 위치 : ***myBlog***(haroopress 설치경로) > config.js
* 지원하는 테마는 ***myBlog***(haroopress 설치경로) > source > themes 의 폴더명으로 확인할 수 있다.
* 원하는 테마의 이름을 적어준다.

```javascript
"theme": {
    "name": "basic"
},
```

![img2_1](@img/blog_img2_1.png)

### <font color="yellow">After</font>

테마를 ***basic*** 에서 ***dark*** 로 수정했다.

```javascript
"theme": {
    "name": "dark"
},
```

![img2_2](@img/blog_img2_2.png)



## 3. ABOUT THIS SITE 문구 수정하기!!

### <font color="yellow">Before</font>

화면의 오른쪽에 아래의 이미지 처럼 *ABOUT THIS SITE* 가 나온다. 이 부분을 내가 원하는 내용으로 수정하려고 한다.

![blog_img3_1](@img/blog_img3_1.png)

* 사용하는 theme 에 따라서 위치는 다르다.(현재 dark 테마를 기준으로 한다.)
* 위치 : ***myBlog***(haroopress 설치경로) > source > themes > ***dark***(사용하는 테마) > views > plugins > intro.ejs
* ***"A Bad Plan is better than no plan."*** 이라는 문구를 추가했다.

```javascript
<div id="author" class="well">
    <h3 class="title"><font color="#FFBB00">A Bad Plan is Better than No Plan.</font></h3>
    <h3 class="title">About This Site</h3>
    <p>
        이 사이트는 <a href="http://github.com/rhiokim/haroopress" target="_target">haroopress</a> 엔진으로 생성된 정적 페이지 기반의 웹 사이트입니다.
    </p>
</div>
```

### <font color="yellow">After</font>


![blog_img3](@img/blog_img3_2.png)

