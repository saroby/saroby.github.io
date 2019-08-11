---
published: false
---
노트북 어뎁터를 회사에서 가져오지 않았기 때문에, 맥북으론 jekyll 블로그를 관리해야 할 일이 생겼다.
MacOS에서는 기본적으로 Ruby가 설치되있다.
```shell
gem install bundler
```
위와 같이 gem을 실행하려고 하면 Permission Denied 오류가 계속 발생했다.
super user권한이 없기 때문인데,
```shell
su
password: 
su: Autheticaiton failure
```
su 명령어로 슈퍼유저 권한을 받아오려고 했지만, root password를 설정하지 않은 탓에 위와 같은 에러메세지와 함께 인스톨이 되지 않았다.

그렇다면 아래의 명령어로 패스워드를 설정하면 된다.
```shell
passwd root
```
이제 gem 명령어를 실행할 수 있다.
```shell
gem install bundler
gem install jekyll
bundle install
```
위 명령어로 jekyll 환경을 셋팅해주자.

```shell
bundle exec jekylee serve
```
그리고 위의 명령어로 로컬서버를 키면 된다.