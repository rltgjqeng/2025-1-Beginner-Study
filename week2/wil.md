#week2 Branch 생성 및 pull request, merge

##1. fork와 star
- **fork**: 다른 사람의 저장소를 내 github에 복사하는 기능
- **star**: 별을 클릭하여 관심 있는 프로젝트를 표시하거나 북마크하는 기능

##2. issue
- 프로젝트에서 버그나 기능 요청 등을 기록하고 관리하는 기능

##3. branch
- git 저장소에서 새로운 작업을 독립적으로 할 수 있는 분기.
- default 값은 main

##4. pull request
- 자신의 작업 브랜치를 원본 저장소에 통합하는 과정이다
- pull request를 승인 한 후 merge를 통해 두 브랜치를 통합 할 수 있다
- 병합 시 발생하는 충동을 해결한다 
- merge에 앞선 코드 리뷰

##5. merge
- pull reqest에서 변경된 내용을 원본 저장소에 통합하는 과정
- **merge commit**: 기존 브랜치와 새로운 브랜치를 모두 가지는 새로운 commit을 생성 한 뒤 새로운 브랜치가 그대로 main 브랜치로 병합된다
- **squash & merge**: 새로운 커및을 모두 squash하여 하나의 commit으로 만든 뒤 main으로 병합한다.
- **rebase & merge**: 새로운 커밋들의 base를 재설정하고 모두 새로운 commit으로 변경한다.

실습 과제제출: <https://github.com/rltgjqeng/2025-1-Beginner-Study/pull/2>
