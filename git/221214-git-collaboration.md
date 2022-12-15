# 221214 Git Collaboration

## Focus
- Fork & Pull Request
- Etc

### Fork
- 'Fork'란, 원본 저장소의 사본을  내 Github 원격 저장소으로 가져오는 것을 의미.
- 따라서 원본 저장소에 직접적인 push가 이뤄질 수 없는 구조를 형성하게 되겠다.
- 나의 원격 저장소를 기점으로 작업을 하고, 변경 사항을원본 저장소에 반영하고 싶을 때 Pull Request(PR)을 한다. ("내 저장소에서 한번 이렇게 만들어봤는데 원본에 반영시켜주실 수 있나요 ~ ?")
- 요약하자면, Fork와 Pull Request 방식을 통해 프로젝트에 '간접적으로' 기여하는 구조가 되겠다.
- 위와는 다르게 프로젝트에 직접 push가 가능하면(Direct push) 팀원 각자 따로 놀게되고 각자의 주장이 너무 쎄짐. 그래서 여러 변경사항을 검토하고 반영할 수 있게 중재자를 두는 셈이다.
- Pull Request를 할 때 작업한 branch에 맞게 보내야함. ex) develop -> develop
- Fork 이후에 다른 팀원의 pull request로 소스코드가 update됐을 때 원본 저장소의 소스코드를 direct로 당겨오게 되는데, 두가지 방식이 존재한다.(원본 remote의 주소를 담을 'upstream' 을 생성해야하는 이유가 여기에 있다.`git remote add [remote이름-통상 upstream][원본 remote 주소]`)
	1. Pull (fetch + merge) : `git pull upstream` 
		- 참조와 병합이 한번에 이뤄진다.
	2. fetch & merge : `git fetch upstream develop`, `git merge fetch_HEAD`
		- fetch하면 fetch_HEAD라는 임시 branch에 담기고, 필요에 따라 내가 원하는 내용만 merge할 수 있다.
		- merge
- 이미 열려있는 Pull Request의 경우 내 remote 저장소의 update된 내용이 자동으로 연동된다.(협업 시 아주 편하겠다.)

### Etc
- `git restore 파일명` : (unstaged 상태) 수정사항 무시
- `git reset HEAD 파일명` : (staged -> unstaged)
- `git commit --amend` : 최신 커밋 수정
- `git revert --no-comit HEAD~3..` : 나의 실수를 인정하고 '되돌린다는 이력' 남기기
- `git mv 파일명 바꿀이름` : mv로 파일이름을 바꾸는 것은 바뀐 이름의 파일 생성과 원본 파일 삭제 두 단계로 이뤄짐. 이를 rename이라는 하나의 작업단위로 묶어줌. 단, staged상태 즉 git이 tracking 중이어야 인식함.
