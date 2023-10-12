# lecture 6

## Version control and collaboration
프로젝트 단계가 존재, 하지만 다음 단계로 넘어가면 이전으로 돌아갈 수 없기 때문에 여러 버전을 다른 이름으로 만들어 놓는다.  
collaboration: 협력을 할 때, 누가 어떤 내용을 수정했는지 표시하는 것이 중요하다.  
**따라서 버전 컨트롤을 아는 것이 중요함**

version control: 시간이 지남에 따라 버전을 기록하는데, 원하는 시점에서 이전 버전으로 돌아가는 것.
버전 컨트롤은 크게 2가지 방식이 있다.  
***1. changes***  
- 버전 시점마다 파일이 변화할 수도 있고, 안할수도 있다. base 버전에 변화된 부분만을 기록해놓음. 복구할 때에는 base 버전에 변화한 부분만 누적해서 표시.

***2. Snapshots***  
- 파일을 특정시간에 따라 기록하는 것. 버전이 바뀔때에 base버전에 변화내용 그대로 기록. 그 파일 전체를 저장.

***3. Collaboration***  
1. local: 개인 단계
2. centralized: 중앙서버에서 관리, 로컬 컴퓨터에서 필요할때 마다 서버에 요청하고 작업. 중앙서버 다운시 어려움이 존재하고 서버에 올리는 것도 어려움.
3. Distributed: 각각의 로컬 컴퓨터가 database의 자료 전체를 가져온다. git의 방식.

## Three states in Git
파일이나 디렉토리가 가질 수 있는 상태  
Working Directory: os에서 작업하는 프로젝트를 담는 디렉토리
git을 사용하면 staging area로 이동 후 문제가 없다 Commit과정을 거치면 git directory로 이동. commit은 snapshots을 했다는 의미

## Git config: first time setup
Git configuration은 3개의 레벨이 존재
1. system level: --system 이라는 옵션을 붙여 사용가능, 모든 repositories에 사용가능하기에 권한이 있어야함 file: /etc/gitconfig
2. Global (user) level: --global option. 이 명령어를 실행한 유저의 모든 repositories에 적용 file:~/.config/git/config
3. local level: --local option. 특정 repository안에서만 적용 된다.  
   **레벨에 따라 더 높은 레벨의 option이 더 중요시 여겨짐**
   git config --list : 현재 적용되어 있는 config 확인가능

Untracked files: 수정해도 git은 아무런 상관도 하지 않겠다.  
따라서 stage area로 올리기 위해서는 git add file_name
git rm --cached file name : 파일시스템이 아닌 git에서 사라짐.
.gitignore 무시해준다. 없는 취급을 해줌

git commit -m "쓰고싶은 메시지"


 
   
