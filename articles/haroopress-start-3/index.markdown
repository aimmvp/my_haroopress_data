{
    "title": "하루프레스 시작하기 3 (개인도메인 사용하기)",
    "author": "s0und0ne Kang",
    "date": "2013-04-07T13:08:02.472Z",
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
        "git",
        "gabia"
    ],
    "acceptComment": true,
    "acceptTrackback": true,
    "published": "2013-04-07T13:08:02.472Z",
    "status": "publish",
    "important": false,
    "advanced": {}
}

- haroopress를 사용하면서, 얼마 전에 산 도메인을 사용해보려고 한다.

- [가비아](http://www.gabia.com)에서 도메인 서비스를 사용하고 있다.

- [github help page](https://help.github.com/articles/setting-up-a-custom-domain-with-pages) 를 참고했다.

### haroopress 에서 CNAME 등록하기

- ***config.js*** 에서 CNAME 을 설정한다.

![CNAME 설정](@img/haroopress_3_1.png)

- [gabia](http://gabia.com) -> 부가서비스 관리 -> ***네임플러스*** 로 이동한다.
- subdomain 을 사용 할 예정이기 때문에 CNAME 을 등록한다. (Top-level domain 을 사용 할 경우 호스트(IP)정보 관리에 항목을 등록한다.)
- CNAME 정보 관리에 ***호스트이름(별칭)*** 을 등록한다.

![CNAME 등록](@img/haroopress_3_2.png)

