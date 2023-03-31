## ※ 깃을 모르는 친구에게 깃 사용법 알려주기

|명령어|의미|
|:---|:---|
|git clone [url]|레포지토리 복제|
|git add [파일명]|파일을 추적하고 stage에 올림(commit 준비)|
|git commit -m " [메시지] "|stage에 있는 변경 사항 반영|
|git push|원격 저장소에 커밋 반영|
|git pull|원격 저장소 버전 local에 반영하기|
|git status|현재 파일 상태 확인(Untracked, Unmodified, Modified, Staged)|
|git stash|수정하고 있던 작업 임시 저장(git pull하는 과정에서 conflict가 생길 수 있으므로)|
|git stash list|임시 저장한 리스트 보여주기|
|git stash apply stash@{ [index] }|index번 째의 임시 작업 덮어쓰기|

## ※ Remote에 Local 파일을 반영하는 방법
1. main 또는 develop에서 브랜치 생성 후 수정
2. git stash(작업 임시 저장)
3. main 또는 develop로 체크아웃 후 git pull
4. 내가 생성한 branch로 체크아웃 후, main 또는 develop merge(병합)
5. git stash apply
6. conflict가 발생하면 발생한 부분을 IDE(통합개발환경)확인
7. 기존 작업에서 추가를 하는 작업이면 추가를 해서 commit push
8. 완전 겹치면 상의를 하고 수정
9. 수정할 부분을 다시 add commit push
