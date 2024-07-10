# Git 필기
## 커밋/푸시 규칙
* 꼭! 항상 절대! `add`, `commit`, `push`는 최상단 폴더에서 작업하기

## 내가 지금 사용하고 있는 컴퓨터에서 처음으로 git 작업을 할 때 1번만 하면 되는 작업
### `git config`
* 계정설정 및 추가
    * `git config --global user.name [나의 유저네임]`
    * `git config --global user.email [나의 github 이메일]`
* 계정확인
    * `git config --global user.name`
    * `git config --global user.email`
* 만약 잘못 입력했을 때, 코드 다시 쓰면 됨
* `git config --global --unset user.name`
* `git config --global --unset user.email`

## 처음으로 깃을 시작할 때 1번만 하면 되는 작업
### `git init`
### `git remote`
* `git remote add origin [나의 github의 원격저장소(github) 레포 주소]`
* `git remote -v`: 내가 등록한 원격저장소 레포 주소 확인
* `git remote remove origin`: 등록한 원격저장소 삭제

## working directory에 변동이 있을 때마다 하는 작업
### `git add`
* `git add .`: 전체 파일 올리기
* 파일 1개만 올리거나 공백으로 구분해서 올리기
### `git commit`
* `git commit -m [커밋메시지]`
### `git push`
* `git push [원격저장소] [브랜치]`
    -`git push origin master`
### `git pull`
* 폴더 생성 `mkdir [폴더명]`
    - 폴더로 이동 `cd [폴더명]`
* `git init`
* `git remote add origin [원격저장소 레포 이름]`
* `git pull [원격저장소] [브랜치]`
* 충돌 주의
### `git clone`
* `git clone [원격저장소 레포 이름]`
* 폴더가 생성되고 그 폴더로 들어가면 add, commit, push 자유롭게 사용 가능
* git init 할 필요 없음

## 상태확인
### working directory에서
- `git status`
    - add 전/후
### staging area에서 (.git)
- `git status`
    - 추적이 되고 있는지만 확인 가능
- `git log`
    - commit 이후에만!!
    - 내림차순 최신이 맨 위
    - `git log --oneline` 짧게 보기