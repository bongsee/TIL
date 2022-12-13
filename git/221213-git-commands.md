# 221213 Git Command Summary

## Key
- Can you explain how to set configuration for Git ?
- Commands for git
- Can you explain what a Commit Convention is ?
- Concerns about commit units

## Index
- Git Objects (Simple is the best)
- Git & Github
- Before Start
- Start Project
- Git process flow and commands
- Commit
- Commit Convention
- README.md
- .gitignore and gitignore.io
- License
- etc

### Git Objects
1. Blob : 파일 하나의 내용에 대한 정보
2. Tree : Blob이나 subtree의 메타데이터
3. Commit : Commit 순간의 스냅샷 

### Git & Github
- Git : 분산형 버전관리시스템(VCS)
- Github : Git을 기반으로한 Cloud Remote Repository Service

### Before Start
- git -v : git 설치여부 확인
- git configuration
  - ```shell
      $ git config --global user.name "github유저네임"
      $ git config --global user.email "github이메일"
      $ git config --global core.editor "vim"
      $ git config --global core.pager "cat"
    ```
  - 설정확인
    ```shell
    $ git config --list
    ```
  - 수정이 필요한 경우
    ```shell
    $ iv ~/.gitconfig
    <!--또는-->
    $ git config --global unset user.name
    $ git config --global user.name "유저네임"
    ```
### Start Project
- github에서 repo 만들고 로컬에 clone하기
- local에서 git init부터 쌓아나가기
- 전자가 수월

### git process flow & Commands
- 일단 파일에 변경사항이 생기면 git status로 확인하는 습관
- "Staging"이 필요한 이유 : Commit을 단위별로 행하기 위함.
- `$ git add`로 untracked file을 staging.
- `$ git commit`로 local repository에 스냅샷 저장.(하나의 완성된 이력이 생성되는 순간이며, 그렇기 때문에 commit은 신중하게 한다.)
- `$ git push origin branch`로 remote repository(github)에 push.

### Commit
- Commit을 나누는 기준은 "작업 단위" 이어야 한다.
- 즉, 같은 Commit 내의 파일들은 논리적으로 연결되어 있어야 한다.
- vim editor로 Commit에 대한 제목과 내용을 기술.


### Commit Convention
- 협업을 위한 통일된 규칙
  1. 제목은 구나 절로 표현
  2. 대문자 활용
  3. prefix 사용
    	- feat: 기능 개발
    	- fix: 오류 수정
    	- docs: 문서화 작업
    	- test: 테스트 관련
    	- conf: 환경설정 관련
    	- build: 빌드 관련
    	- ci: Continuous Integration 관련
- [Commit Convention 교본](https://github.com/angular/angular/pulls)

### README.md
- 나의 project와 사용자가  만나는 첫번째 문으로 얼마나 잘 작성하느냐에 따라그 성패가 나뉠만큼 중요하다!
- 양식
	- Project Name
	- Documentation
	- Installation
	- about Version
	- More Info
	- Contribution
	- License
### .gitignore & gitignore.io
- git의 추적 대상에서 제외시키기 위한 파일들 모음
- 작업 환경에 따라 [gitignore.io](https://www.toptal.com/developers/gitignore/)에서 자동으로 생성 가능하다.

### License
- MIT
- Apache
- GNU의 GPL(General Public License)

### etc
- origin과 HEAD가 갖는 의미
- `git remote`
- `git remote -v`
- `git remote add 식별자 주소`
- `git remote remove 식별자`
- staging 상태를 되돌리기 : `git reset HEAD 파일명`
- repo의 버전 관리 현황 출력 : `git log` -> Git Alias를 이용하여 `git lg`
- `git status -uall` : 변경 사항을 디렉토리 아래 파일레벨까지 확인가능
- .vimrc


