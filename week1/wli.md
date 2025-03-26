#Git, Github 흐름
git, github는 코드의 버전 관리와 협업을 위한 도구이다.

##1. **작업 디렉토리(Working Directory)**
  - 실제 코드가 있는 폴더
  - **주요 작업**:
    - 파일 수정, 파일 추가, 삭제 가능

  - **명령어**:  
    - git add : 작업 디렉토리에서 수정된 파일을 스테이징 영역에 추가함함

##2. **스테이징 영역(Staging Area)**
  - 커밋할 변경 사항을 임시로 보관하는 공간
  - **명령어**:
    - git commit -m "commit_message" : 스테이징 영역에 있는 변경 사항을 로컬 저장소에 커밋하여 버전 히스토리에 기록함

##3. **로컬 저장소(Local Repository)**
  - 로컬 컴퓨터에 존재하는 Git 저장소로, 프로젝트의 버전 히스토리를 관리함
  - **명령어**: 
    - git push origin <branch_name> : 로컬 저장소의 커밋을 원격저장소에 업로드하여 다른 사람들과 공유함
    - git merge <branch_name>: 다른 브랜치의 변경 사항을 현재 브랜치에 저장함
    - git checkout <branch_name> : 다른 브랜치로 전환하거나 특정 커밋 상태로 작업 디렉토리를 업데이트 함.

##4. **원격 저장소(Remote Repository)**
  - Github 등 서버에 호스팅되는 저장소, 협업 공간이다
  - **명령어**:
    - git fetch origin : 원격 저장소의 변경 사항을 로컬 저장소로 가져오지만 자동으로 병합하지 않는다. 
    - git pull origin <branch_name> : 원격 저장소의 변경 내용을 작업 디렉토리로 가져오고 자동으로 현재 브랜치에 병합한다.
    - git clone "저장소URL" : 원격 저장소를 로컬에 복제하여 새 작업 환경을 구축함.

#파일의 생명주기
Git에서 파일이 어떻게 이동하는가

##1. **Untracked**
  - Git의 버전 관리 시스템에 포함되지 않는 파일.
  - 새로운 파일을 생성하고 git status를 실행하면 "Untracked files: "메세지를 확인할 수 있다.

##2. **Unmodified**
  - Git이 관리하는 파일이지만, 마지막 커밋 이후로 수정되지 않은 파일.
  - Git을 추적되며, 변경이 없는 경우 git status 실행하면 "no changes"로 표시된다.

##3. **Modified**
  - 파일을 수정하였고, 아직 staging area에 추가되지 않은 상태.
  - 작업 디렉토리에서 수정한 파일은 여기에 분류됨.
  - git add로 파일을 staging area에 추가 가능함.

##4. **Staged**
  - 파일이 수정되고 나서 git add 통해 staging area에 추가된 상태
  - git commit후에는 다시 unmodified 상태로 돌아감.