# 221213 Shell Command Summary

## Key
- what is kernel & shell ?
- CLI & GUI
- various shell commands
- what is Vim ?

## Index
- GNU프로젝트와 Linux의 탄생
- CLI & GUI
- Shell Commands
- Vim

### GNU프로젝트와 Linux의 탄생
- 독점 소프트웨어인 Unix로부터 벗어나 모든 소프트웨어의 오픈소스화를 위한 GNU프로젝트가 등장
- 리누스 토르발즈에 의해 Linux 커널이 등장하였고, GNU프로젝트의 라이브러리와 도구들과 합쳐져 Linux OS 가 등장한다.
- Kernel이란, 하드웨어를 직접 제어하며 운영체제의 서비스를 제공하는 운영체제의 핵심이라고 볼 수 있다.
- 사용자는 Shell이라는 매개체를 통하여 운영체제의 서비스를 이용할 수 있다.

### CLI & GUI
- Shell의 인터페이스로는 CLI와 GUI가 있다.
	- CLI
		- 명령줄 기반의 인터페이스로, 텍스트를 통해 상호작용하므로 일반적인 사용자가 사용하기엔 직관적이지 않다.
		- 허나, 텍스트 기반이므로 GUI와 비해 하드웨어 리소스를 비교적 효율적으로 다룰 수 있는 장점이 있다.
		- 또한, 작업에 따라 GUI에 비해 더욱 효과적인 작업을 수행할 수 있다. (반복적인 작업 등)
		- 대표적인 예로 Unix 기반의 bash, zsh 등이 있다.
	- GUI
		- 마우스로 폴더를 클릭하고 폴더가 열리는, 우리가 흔히 접해왔던 인터페이스가 그래픽 기반의 Graphic User Interface이다.
		- 확실히 텍스트보다 직관적이다.
		- Graphic을 다루기 때문에 렌더링에 있어서 하드웨어 리소스 효율은 텍스트 기반의 CLI보다 나쁘다.
		- 대표적인 예로 MacOS의 Finder, Windows의 탐색기 등이 있다.

- 그럼에도 불구하고 CLI first인 이유 ?
	- CLI의 Command로 git을 사용할 줄 알면 GUI도구가 제공하는 기능에 대한 이해가 빠르다.
	- 후에 Source Code를 Cloud Platform에서 사용하는 날이 올 때, CLI Command로 버전관리를 수행해야한다.
	- 수행은 CLI, 확인용도로의 GUI를 지향하자.

### Shell Commands (git bash)
- `$` : Command Line의 맨 앞에 등장하는 특수문자로, 사용자의 입력을 받을 준비가 되어있다는 표식이다.
- `~` : 틸드(Tilde)라고 부르며, 사용자의 home directory를 지칭하는 특수문자다.
- `/` : 명령줄 맨 앞에서 사용할 땐, 하드디스크의 최상단 directory를 의미하며, Path의 사이에서는 구분자로 사용된다. (절대경로)
- `pwd` : 'print working directory'의 약자. 현재 작업중인 폴더의 경로를 출력한다. (상대적인 개념)
- `ls` : 'list segment'의 약자. 현재 폴더내에 존재하는 파일과 directory list를 출력한다.
- `ls -a` : 숨김 파일까지 모두 list up
- `cd` : 'change directory'의 약자.
- `mkdir` : 'make directory'의 약자.
- `touch` : 새로운 file을 생성할 때 쓰는 명령어. directory는 경로를 표현하기 위해 등장한 논리적인 차원의 개념이지만, file은 그 자체로 실재하기 때문에touch라는 명령어로 지정한게 아닌가 싶다. 실제로, file을 지우는 명령어인 rm으로 directory를	직접 제거하지 못하도록 막아놨는데, 이는 directory가 경로라는 의미를 갖는  논리적인 개념이기 때문에 그렇다. directory와 그 하위 파일과 dir을 제거하기 위해선 재귀적인 의미를 갖는 `rm -r`또는 `rm -rf`로 가능하다.
- `rm` : 'remove'의 약자
- `*` : 'Asterisk'라고 부르며, 모든 것을 통칭할 때 쓰인다.  ex) *.js == 확장자가 js인 모든 파일, *.* 모든 확장자의 모든 파일
- cp : 'copy'의 줄임말. 복사할 파일명과 복사할 위치의 경로를 넣어줘야한다. 같은 폴더 내에 복사시 복사본의 이름을 지정해야한다.		     안해도 실행되긴하는데 같은파일을 덮어씌우는꼴이라 그렇게 의미없는 짓을 할 이유가 없다.
- 물리적인 삭제를 의미하는 delete와 논리적인 제거를 의미하는 remove의 차이점을 이해한다. 논리적인 제거는 하드웨어의 메모리에 	접근하는 방식을 제거함을, 물리적인 삭제는 메모리의 데이터 자체를 들어내는 것을 의미한다. 즉, 제거는 복구가 가능하지만 삭제는 복구가 불가능한 개념이다.
- cat : text 파일을 CLI에 뿌려 확인할 때 쓰임.

### Vim

- Vim을 배워야하는 이유 : CLI 전용 text editor이다. 같은 개념으로 GUI의 메모장이 있다.
- text 파일을 vim으로 여는 방법 :  `vi learn-md.md` "vim으로 learn-md 마크다운 파일 열어주세요~"
- GUI에서 text파일을 더블클릭해서 메모장으로 여는 것과 같은 이치다.
- `node index.js`와 같이  node로 index.js 파일을 실행하는 것과 같은 이치.
- vim editor에서 Mode라는 개념이 존재하는데, Command Line Interface의 경우 마우스 없이 키보드만으로 동작하기 때문에 생겨난 개념이다.
	- Normal Mode : 모든 모드는 기어 변속하듯 Normal mode를 거쳐가야한다.
	- Insert Mode : Normal Mode에서 `i`text 입력을 하기 위한 모드(`o`입력 시 다음줄에서 입력모드 전환)
	- Command Mode : Normal Mode에서 `:`를 눌러 진입. 하단에서 명령 하달 가능
		- `:q` : quit 
		- `:q!` : quit discarding all changes (저장하지않고 나가기)
		- `:w`  : write (중간 저장)
		- `:wq` : write and quit (저장 후 나가기)
		- :{number} : jump to {number}th line.
	- Visual Mode : V 또는 Ctrl+V를 눌러 블록을 선택.

