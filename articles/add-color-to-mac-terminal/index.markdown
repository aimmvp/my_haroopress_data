{
    "title": "Mac OS X 터미널에 색상 추가하기",
    "author": "s0und0ne Kang",
    "date": "2013-04-28T00:49:52.996Z",
    "categories": [
        "mac",
        "tip"
    ],
    "tags": [
        "mac",
        "tip"
    ],
    "acceptComment": true,
    "acceptTrackback": true,
    "published": "2013-04-28T00:49:52.996Z",
    "status": "publish",
    "important": false,
    "advanced": {}
}

***info <i class="icon-info-sign icon-white">이 글은 다음의 URL을 참고해서 정리했다.</i>***
    
참고 URL : http://osxdaily.com/2012/02/21/add-color-to-the-terminal-in-mac-os-x/

이 방법은 디렉토리, 파일, 실행가능, 심볼릭 링크 등의 다른 항목을 다른 색상으로 보이게 한다.

커맨드 라인에서 "ls -G" 를 타이핑하여 색상을 미리 볼 수 있다. "ls -G" 를 이용한 미리보기는 터미널의 색상설정에 따르며, 반드시 아래의 스크린샷처럼 보이는 것은 아니다.

* 터미널을 열고 입력
    
    nano .bash_profile

* 방향키를 이용해서 문서의 제일 밑으로 이동해서 아래의 텍스트 중 하나를 복사해서 붙여넣자. 

### Dark Terminal 테마

    export CLICOLOR=1
    export LSCOLORS=GxFxCxDxBxegedabagaced

### Light Terminal 테마

    export CLICOLOR=1
    export LSCOLORS=ExFxBxDxCxegedabagacad

![addColor1](@img/addcolor1.png)

* Control+O 를 입력해서 저장 한 후에 새로운 터미널을 열고 "ls" 를 입력해서 테마가 바뀐것을 확인한다.

만약 .bash_profile 에 "ls -GFh" 처럼 다른 것의 링크를 생성하고 싶다면 다음의 방법으로 하면 된다.

    alias ls='ls -GFh'

이것은 Mac OS X 10.6, OS X 10.7, OS X 10.8 이상의 버전에서 당신이 bash shell 을 사용하는 한 동작할 것이다. 당신이 [어떤 shell](http://osxdaily.com/2009/09/25/what-shell-am-i-using/) 을 사용하는지 모른다면, 터미널 윈도우의 타이틀바의 "bash" 표시를 보거나 다음의 명령어로 확인 할 수 있다.

    echo $SHELL

결과가 "/bin/bash" 이면 bash 이고, 다른것이라면 아니다.

[즉시](http://osxdaily.com/2011/05/02/change-the-appearance-of-terminal-windows-quickly/) 터미널 윈도우의 모양을 바꿀 수 있고, [배경화면](http://osxdaily.com/2011/08/05/change-the-terminal-background-picture/)도 바꿀 수 있음을 잊지 말자