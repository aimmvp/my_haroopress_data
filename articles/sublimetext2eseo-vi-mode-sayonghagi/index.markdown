{
    "title": "SublimeText2에서 vi Mode 사용하기",
    "author": "s0und0ne Kang",
    "date": "2013-04-05T22:58:50.165Z",
    "categories": [
        "tool",
        "editor"
    ],
    "tags": [
        "tool",
        "editor"
    ],
    "acceptComment": true,
    "acceptTrackback": true,
    "published": "2013-04-05T22:58:50.165Z",
    "status": "publish",
    "important": false,
    "advanced": {}
}

ublimeText2 에서 vi 의 command mode 를 사용할 수 있는 방법이다.

http://www.sublimetext.com/docs/2/vintage.html 를 요약해봤다.

### Vintage Mode 란? 
-----
***Vintage*** 는 Sublime Text 2 의 vi 모드 에디트 패키지이다. 이 패키지는 Sublime Text 에서 다수 선택(multiple selection)을 포함한 vi 명령모드를 사용 할 수 있게 해준다.

### Vintage 사용하기
-----

***Vintage***는 기본적으로 <code>ignored_packages</code> 에서 비활성화 되어 있다. ignored packages 에서 ***Vintage*** 를 제거하면 vi key 를 이용해서 문서를 편집 할 수 있다.

1. Preferences / Settings - Default menu 선택

2. <code>ignored_packages</code> 를 수정한다.
    > "ignored_packages": ["Vintage"]

    to:
    > "ignored_packages": []

    파일 저장

3. 이제 ***Vintage Mode*** 를 사용 할 수 있다. - 상태표시줄(화면하단) 에서 "INSERT MODE" 를 볼 수 있다.

*** 참고사항 ***

* 기본적으로 insert mode 로 시작하게 하는 방법

1. Preferences / Settings - User menu 선택

2. <code>ignored_packages</code> 를 수정한다.

    > "vintage_start_in_command_mode": true
