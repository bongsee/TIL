# 221214 Git Branch

## Foucs
- branch란 ?
- git branch commands
- CONFLICT 시나리오와 해결과정

### branch란?
- branch의 사전적의미로 '지사, 분점'를 뜻한다.
- git에서 branch가 가지는 의미는 다음과 같다.
	- branch마다 독립적인 work flow를 가지기 때문에 잘 돌아가는 소스코드를 건드리지 않으면서 기능개발, 버그 수정, 테스트 등 다양한 작업을 시도할 수 있다. (평행우주)
	- 같은 프로젝트 내에서 팀원과 각자 맡은 역할에 맞게  병렬적으로 개발을 할 수 있어 보다 유연한 협업이 가능하다.

### branch 관련 commands
- `git branch [branch명]` : 새로운 branch 따기. 가장 최신의 commit을 기준으로 분기점이 생성된다. 네이밍은 새로만들 branch의 역할을 잘 알 수 있도록 짓자.  branch명 생략 시 현재 프로젝트의 branch 현황을 출력한다.
- `git branch -D [branch명]` : branch 삭제.
- `git switch 브랜치명` : 현재 위치에서 다른 branch로 switch
- `git merge` : 다른 branch에서 작업한 내용을 병합할 때 사용한다. 흡수의 방향은 밀어내는 것이 아닌 "당겨오는 것". 따라서 merge 동작 시 `git branch`로 현재 내가 위치한 branch를 확인하고 신중히 merge 하는 것이 중요함. 보다 중심이 되는 branch에서 하위 branch를 흡수하도록하자. merge 후에 branch가 사라지는 게 아니라 최신 commit을 넘겨주는 것이기 때문에 생명주기가 다한 branch는 그때그때 지워주자.

### CONFLICT
- 내가 수정한 부분을 다른 팀원도 수정했을 때 git은 어떤 변경사항을 선택해서 merge해야할지 판단하지 못하기 때문에 CONFLICT났다고 사용자에게 던진다.
- 즉, git이 "나는 뭘 선택해야할지 모르니까 너가 알아서 '협상'후에 수정하여 commit해라~"라는 의미다. 
- CONFLICT 발생 시 shell에 출력되는 내용에서 어디에서 충돌이 일어났는지 알 수 있다. (이런거 보면 예기치 못한  이슈나 에러는 shell에서 하라는 대로 하면 대부분 해결되는듯하다. 정말 친절함..)
- 협상 후에 수정이 완료됐다면 해당 내용 staging하고 commit하면 충돌이 해결된 것을 확인할 수 있다~

