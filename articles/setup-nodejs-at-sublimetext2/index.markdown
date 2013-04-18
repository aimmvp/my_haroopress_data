{
    "title": "SublimeText2 에 nodejs 세팅하기",
    "author": "s0und0ne Kang",
    "date": "2013-04-18T12:38:36.660Z",
    "categories": [
        "tool",
        "util",
        "nodejs"
    ],
    "tags": [
        "too",
        "util",
        "nodejs",
        "sublimetext2"
    ],
    "acceptComment": true,
    "acceptTrackback": true,
    "published": "2013-04-18T12:38:36.660Z",
    "status": "publish",
    "important": false,
    "advanced": {}
}

Sublime Text2 는 그냥 Text Editor 로만 사용하는 줄 알았지만, 절대 아니였다 ^^;;

Nodejs 를 콘솔에서만 이것저것 테스트용으로 사용했었는데, Sublime Text2 에서 사용 할 수 있다고 해서 사용방법을 정리해보려고 한다.

이 글에서는 nodejs 테스트환경에 대해서만 다루고 추가적인 내용은 계속 추가하려고 한다.

>  Nodejs 설치하기

1. [nodejs 홈페이지](http://nodejs.org/#download) 에서 install 을 클릭하여 설치파일을 다운받는다.(2013년 1월 13일 현재 node-v0.8.17.pkg 이 다운로드 된다.)

    ![Nodejs 다운받기](@img/node1.png)

2. 다운받은 파일로 nodejs 를 설치하면 된다.


### 이제 ***Sublime Text2*** 먼저 설치하기
>
참고 URL : http://wbond.net/sublime_packages/package_control/installation 

1. Sublime Text2 설치파일 다운로드 받기

   - [Sublime Text 홈페이지](http://www.sublimetext.com)
   - 2013년 1월 13일 현재 2.0.1이 최신 버전이다.
      * Mac에서 실행하면 자동으로 Download for OS X 라고 나오며, 버튼위에 마우스 커서를 올리면 다른 OS 용 버전도 다운로드 가능하다.
    ![Sublime Text2 다운받기](@img/sublime1.png)  
     
2. 다운로드 받은 ***Sublime Text 2.0.1.dmg*** 파일을 실행시킨다.

3. 나중에 Sublime Text2 에 여러가지 플러그인을 쉽게 추가하고 관리하기 위해서 Package Maanger 을 설치한다.
***info <i class="icon-info-sign icon-white"></i> info 아래의 내용은 wbond.net 에 나와있는 내용을 필요한 부분만 정리한 것이다.***
- [wbond.net](http://wbond.net/sublime_packages/package_control/installation) 에서 script 를 복사해서 설치힌다.
    - Sublime Text 2 를 실행시킨 상태에서 ***Ctrl+`*** 를 입력하면 아래의 이미지처럼 console 창이 활성화 된다.
    - 위의 사이트에서 script 를 복사해서 붙여넣기 한다.
    
    ````
import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print 'Please restart Sublime Text to finish installation'
    ````
    >Enter 키를 입력해서 설치가 끝나면 다음의 문구가 나오는데 다시 실행한다.
    ```
    Please restart Sublime Text to finish installation
    ```
    
4. Console( ***Ctrl+`*** )에서 다음의 script 를 입력해서 설치한다.

    ```
    < Mac OS X >
    'git clone git@github.com:tanepiper/SublimeText-Nodejs.git ~/Library/Application\ Support/Sublime\ Text\ 2/Packages/Nodejs/'
    
    < Windows >
    `git clone git://github.com/tanepiper/SublimeText-Nodejs.git "%APPDATA%\Sublime Text 2\Packages\Nodejs"`
    ```
5. ***comand + shift + p*** 를 누르면 Command Palette 를 실행시킨 후 ***install Package*** 를 입력한다.

    ![Sublime Text2](@img/sublime2.png)
6. 처음에는 Sublime Text 하단에 Loading Packages 가 나오는데 한번 더 5번의 과정을 실행하면 install package에 들어가게 되고 여기에서 설치를 원하는 package 이름을 입력하면 Github에서 package 를 검색해서 카피하게 된다.( [Sublime package Control](http://wbond.net/sublime_packages/package_control/usage 참고) )
    - 여기에서는 nodejs 관련 패키지 설치가 목적이기 때문에 Nodejs 를 입력한다.
    
    ![Sublime Text2](@img/sublime3.png)
    
    아래의 이미지에서 제일 위에 있는 Nodejs 를 선택한다.
    
### 테스트 하기

1. Tools - Build System 에서 Nodejs가 추가된 것을 확인 하고 선택한 후 테스트 코드를 입력하고 Build 를 실행하면, 아래처럼 에러가 발생한다.

    ![Sublime Text2](@img/sublime4.png)

2. Nodejs 패키지가 설치되어 있는 위치(~/Library/Application Support/Sublime Text 2/Packages)에서 ***Nodejs.sublime-build*** 파일을 열어서 아래의 문구를 추가한다.

    ```
    "path": "/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin:/usr/X11/bin: No such file or directory"
    
    - 윗줄에 , 는 센스 ^^
    - 이 내용을 검색으로 찾았었는데 어디서 찾았었는지는 모르겠다….
    ```
    ![Sublime Text2](@img/sublime5.png)
3. 이제는 Build(***cmd+B***) 를 통해서 성공적으로 빌드 성공이다.