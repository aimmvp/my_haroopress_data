{
    "title": "하루프레스 시작하기 2 (설치하기)",
    "author": "s0und0ne Kang",
    "date": "2013-04-06T11:46:29.303Z",
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
    "published": "2013-04-06T11:46:29.303Z",
    "status": "publish",
    "important": false,
    "advanced": {}
}

## 본격적인 haroopress 설치하기

- make directory(directory name : myblog.com)

```
$ mkdir myblog.com
```

- github 에서 소스 clone 하기

```
$ git clone git@github.com:rhiokim/haroopress.git myblog.com
```

- 설정 초기화하기 (블로그의 기본적인 정보들을 설정한다.)

```
$ make init
========================================
= configurate haroopress
========================================
./bin/setup.js
haroo> Insert your site title (*) "My Haoopress Blog"
 > My BlaBla Blog
haroo> Insert your site description (*) "My Development diary, I love node.js & javascript"
 > My BlaBla Blog
haroo> Insert site url (*) "http://www.myblog.com"
 > http://aimmvp.github.com
haroo> Insert you full name (*) "Rhio Kim (sync to source/data/authors/Rhio Kim.markdown)"
 > s0und0ne Kang
haroo> Insert you gravatar emaill address (*) "abc123@gmail.com"
 > aimmvp@gmail.com
haroo> Insert you site meta information (*) "javascript, css3, html5"
 > javasciprt, Raspberry Pi, html5
http://aimmvp.github.com Meta Information
-----------------------------------------------
{
    "version": "0.9.2",
    "defaultTitle": "My BlaBla Blog",
    "description": "My BlaBla Blog",
    "siteUrl": "http://aimmvp.github.com",
    "author": "s0und0ne Kang",
    "email": "aimmvp@gmail.com",
    "keywords": [
        "javasciprt",
        "RaspberryPi",
        "html5"
    ]
}
haroo> Save? [y/n] :           y
========================================
= clear public & deployment directories
========================================
./bin/clear.js
haroo> clear to deploy directory¶
haroo> clear to public directory
========================================
= setup repository for deployment
========================================
cd ./bin/;./gh-pages.js
haroo> Enter the read/write repository for your haroopress site
"git@github.com:[github-id]/[github-id].github.com.git"
 > git@github.com:aimmvp/aimmvp.github.com.git
```
