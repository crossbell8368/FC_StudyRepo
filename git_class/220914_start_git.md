* 리눅스의 개발 히스토리
* 다양한 리눅스 배포판 소개 
* bash 환경에 대한 설명 
	~ : tilde => 현재 로그인된 유저의 권한내 최상위 위치
	- : flag => 서브커맨드로 해당 명령의 옵션을 부여하고 싶을때 사용
	touch : 텍스트 기반 파일생성 명령어
	기본적인 리눅스 명령어 설명 : cd, pwd, ls 등등
	명령어 사용을 통한 파일생성, 이동, 변경등의 실습진행
	rm & del : 논리적, 물리적 삭제방식의 차이 => 복구가능 or 불가능의 차이를 가짐
			
* git : 버젼관리 시스템
  github : git의 시스템을 이용한 remote repo 서비스

* 기업체에서는 Github 대신 BitBucket이나 GitLab을 더 많이이용
	: 보안 및 업무관리 솔루션과의 연동성을 위해
	
* git & github 진행과정
	- (local) git 설정
	- (github) repo 생성
	- (local) repo clone 진행
	- (local) README.md 파일수정
	- (local) git add README.md : Workspace => Staging Area
	- (local) git commit : Staging Area => Local Repo
	--------------------------------------------------
	- (github) 유저토큰 발행
	- (local) 발행된 토큰을 로컬git에 적용
	--------------------------------------------------
	- (local) git push origin master : Local Repo => Remote Repo
		=> 윈도우의 경우, 리눅스 방식으로 형식으로 변경하겠다라는 주의메세지 발생
	- (GitHub) 'master' 브랜치에서 README.md 파일 확인


* 작업단위 구분 ( about commit )
	- 어떤 작업을 마쳤다고 바로 commit을 하는것이 아님
	- test repo 기준, local에서 README.md 를 수정하고 test.py를 만들었다고 가정
	- 이 두가지는 작업단위가 다르기에, 이 두가지 작업내용을 하나의 commit에 묶기는 부적절
		: 두가지 작업이 서로 전혀 연관이 없는데, commit할때 뭐라하고 commit할 것인가?
	- 이럴때는 git add 명령어를 통해 다양한 작업내용들 중, 본인이 하나의 작업단위로 묶을 내용들을 staging area로 올림
	- 그렇게 모인 작업내용들을 포괄하는 설명을 붙여서 commit을 진행과정
	- 남은 작업내용들도 묶이는 작업들끼리 묶어서 Commit을 진행
	=> 왜 이렇게 하는가?
		: 남들이 github의 프로젝트를 볼때 이 commit 메세지들을 봄
		: 그런데 이 구분들이 제대로 이뤄지지 않았다면 협업 프로젝트 및 이 프로젝트를 바라보는
		 사람의 입장에서도 좋지않을 것이기에 = 협업의 편의성을 위해


* commit 메세지
	- commit 메세지의 제목과 설명을 보고 무슨 작업인지 바로 알수있도록 해야됨
	- 제목에는 feat, fix, docs 등의 prefix 꼭 달아주기!
	
	
* .gitignore 생성
	- git의 버젼관리 시스템을 적용하고 싶지 않은 파일들의 목록을 적어놓는 곳
	- 환경이나, 변경이 일어나도 Git이 신경을 쓰지 않았으면 좋겠을 파일들 대상
	- 일일이 만들어주는 것도 방법이지만, 'gitignore.io' 에서 템플릿을 받아사용하는것을 추천 
	
* git status 플래그
	-uall : 새로운 디렉토리 내 생성되는 파일들을 자세히 보기위해 다는 옵션
	
