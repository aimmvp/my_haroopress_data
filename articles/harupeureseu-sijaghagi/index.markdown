{
    "title": "하루프레스 시작하기 1 (환경설정)",
    "author": "s0und0ne Kang",
    "date": "2013-04-06T07:16:28.323Z",
    "categories": [
        "haroopress",
        "util",
        "tool"
    ],
    "tags": [
        "haroopress",
        "blog",
        "util",
        "tool",
        "git"
    ],
    "acceptComment": true,
    "acceptTrackback": true,
    "published": "2013-04-06T07:16:28.323Z",
    "status": "publish",
    "important": false,
    "advanced": {}
}

벌써 하루프레스를 몇번이나 세팅을 해봤지만, 나같은 초보는 세팅을 할때마다 여기저기 찾아보면서 세팅을 해야했다. 그래서 한번 정리해보려고 한다.

***info <i class="icon-info-sign icon-white">이 글은 다음의 URL을 참고해서 정리했다.</i>***

    http://insanehong.kr/post/haroopress-pre/
    http://opentutorials.org/course/488/2605
    http://haroopress.com/post/haroopress-deploy-to-github/

1. 설치전에 몇가지 확인해야 할 부분들이 있다.

[하루프레스](http://haroopress.com/about/)는 [node.js](http://nodejs.org) 를 기반으로 하고, 기본적으로 [Github](http://github.com) 의 정적페이지 서비스를 이용해서 퍼블리싱을 하고 때문에 로컬의 **node.js** 와 **Git**의 설정을 확인해야 한다.(nodejs와 Git을 처음설치하는 방법은 [이곳](http://haroopress.com/post/haroopress-install-requirements/) 을 참고한다.
    

git의 설치여부 확인하기.
--
    
```
$ git
```
    
![git 설치 확인](@img/haroopress_1_1.png)
    
node.js 설치하기
--
        
### node.js의 모듈설치를 쉽게하기 위해서 npm을 설치해서 사용한다.

```
$ curl http://npmjs.org/install.sh | sh
```

[npm(Node Packaged Modules)](https://npmjs.org/) 설치여부 확인하기( 2013. 04. 06 현재 1.2.15가 최신버전이다.)

```
$ npm -v
1.2.15
```

### Github에 동기화 하기

- ssh_key 를 생성하고 복사한다.

```
$ ssh-keygen
$ cat ~/.ssh/id_rsa.pub
```

![ssh_key 복사하기](@img/haroopress_1_2.png)

- github 에 등록하기

[github.com](http://github.com) --> Account Settings --> SSH Keys --> Add SSH key

![github에 등록하기](@img/haroopress_1_3.png)

### 저장소 생성하기

[github.com](http://github.com) --> New Repository(우측 하단) --> Repository name 은 본인의 github.com 계정 아이디 입력(ex. aimmvp.github.com)

