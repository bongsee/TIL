# 221214 Git-Flow Strategy

## Focus
- Branching Models
- Git flow tool 사용하여 편리하게 작업하기
- Etc

### Branching Models
- git branch를 어떻게 활용하면 더 효율적인 work flow를 구축할 수 있을지에 대한 방법론이 등장.
- git flow, github flow, gitlab flow
- github, gitlab 같은 경우 버전 관리의 의미가 모호한 웹앱에서 주로 쓰인다고 한다.
- git flow
	- hotfix : 메인 소스코드에서 긴급히 수정하여 바로 배포를 해야할 때 hotfix branch를 사용한다.
	- main(master) : 사용자가 직접적으로 사용하게 되는 소스코드가 담긴 branch.
	- release : 기능 개발을 제외하고 minify, unglify, build 등과 관련된 작업이 이루어지는 branch. release branch는 main과 develop branch로 각각 merge된다.
	- develop : 실질적으로 개발자들이 작업하는 메인 라인이다. develop branch를 기점으로 분기하여 개발하게 된다. 
	- feature : develop으로부터 기능 개발을 위해 따낸 branch.

### Git flow tool
- `git flow init` : git flow를 초기화하는 단계. init을 실행하기 전에 main branch 제외하고 다른 branch가 있으면 안되고, working tree도 clean해야함. main branch와 develop branch를 설정하고 그 외 branch의 prefix 설정 등을 함.
- `git flow branch종류 start branch명` : start의 명령에 switch와 생성 두가지 단위가 함께 동작한다.
- `git flow branch종류 finish branch명` : finish 명령에 switch, merge, 제거 세가지 단위가 함께 동작한다.

### Etc
- local에서 새로운 branch를 따고 remote에 push할 경우 -u tag(upstream set)를 사용하여 원격 저장소와의 링크를 형성하도록 한다. (첫 push때만 하면 됨.)
- release branch를 finish할 때 설정해준 release version tag는 remote에 push할때 `git push --tags`로 태그도 같이 날려주자.
