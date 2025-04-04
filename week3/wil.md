# wil 3주차

## 1. git log 
- 커밋 기록을 최신순으로 확인
- --oneline 옵션 사용하면 커밋을 한줄로 요약하여 보여줌
'''git log --oneline'''

### 1.1. Commit id
- 커밋 식별자
- sha-1을 사용하는데 sha-1은 160bit hash 값을 생성하므로 40자리의 16진수(4bit) 값으로 나타난다.

### 1.2.HEAD
- 현재 작업중인 브랜치의 최신 커밋을 나타낸다
- 다음 커밋의 base가 되는 커밋이다.
- 새로운 커밋이 생성될 때마다 변경된다.

## 2. git status
- untracked, unstaged, staged 세 종류로 파일을 구분한다.

## 3. 커밋 되돌리기
### 3.1. commit --amend
- 마지막 커밋 내용에 변경이 있을 때 사용
- 완전히 새로운 커밋으로 대체(id 바뀜)
- 커밋 메세지는 vim/vi로 수정
- **vim 진입 안 하려면 -m 옵션 사용**
'''git commit --amend -m "commitMessage"'''
- **커밋 메세지 수정이 필요 없다면 --no-edit 사용**
'''git commit --amend --no-edit'''
- 주의사항 : 다른 사람이 base로 삼고 있는 커밋은 amend 하면 안됨.

### 3.2. git reset
- 커밋 제거에 사용함
- **돌아갈 커밋의 id 입력**
'''git reset '--option(soft,mixed,hard)' "commit_id"'''
#### 3.2.1. reset --soft
- 커밋만 취소함 = 변경 사항이 staging area로 돌아감
#### 3.2.2. reset --mixed(default)
- 커밋을 취소하고, 변경 사항이 working directory로 돌아감
#### 3.2.3. reset --hard
- 커밋을 취소하고 이전 커밋으로 돌아감, 변경 사항을 모두 삭제함(=컴퓨터에서 삭제됨)

### 3.3. git revert
- 커밋을 **제거하지 않고** 되돌림.
- 되돌릴 커밋이 새로 생성됨
- --edit 옵션(default)과 --no-edit옵션이 존재, 편집기 진입 여부 결정.
'''git revert --no-edit "commit_id"
- 새로 커밋하지 않고 staging area에 올리기만 하는 옵션도 있음
'''git revert --no-commit "commit_id"
- 협업 시 충돌 방지를 위해 revert 사용을 권장.
