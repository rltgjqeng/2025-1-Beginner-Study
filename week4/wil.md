## 브랜치 전략

### 브랜치 관리의 필요성
- 작업 간 충돌을 방지하기 위해 브랜치를 분리해야 한다  
- 각 브랜치의 목적을 명확히 해야 한다  
- main 브랜치는 안정적으로 관리해야 한다

### 브랜치 보호 규칙
- 승인 없는 Pull Request 병합을 제한할 수 있다  
- 특정 브랜치에 Push할 수 있는 사용자를 제한할 수 있다

---

## Git Flow

- Vincent Driessen이 고안한 브랜치 전략이다  
- 다음과 같은 브랜치를 사용한다:
  - `main`: 제품의 최종 버전이 존재하는 브랜치이다
  - `develop`: 개발의 기준이 되는 브랜치이다
  - `feature`: 기능 단위 개발을 위한 브랜치이다
  - `release`: 배포 준비 및 QA 작업을 위한 브랜치이다
  - `hotfix`: 운영 환경의 긴급 수정을 위한 브랜치이다

- 기능 개발은 feature 브랜치에서 시작하여 develop 브랜치로 병합한다  
- release 브랜치는 develop에서 분기하며, 작업 완료 후 main과 develop에 병합한다  
- hotfix 브랜치는 main에서 분기하며, 수정 후 main과 develop에 병합한다

---

## GitHub Flow

- 수시로 배포되는 웹 환경에 적합한 브랜치 전략이다  
- 다음 두 가지 브랜치만 사용한다:
  - `main`: 항상 배포 가능한 상태를 유지한다
  - `feature`: main에서 분기하여 작업 후 다시 main으로 병합한다

- 브랜치 명에는 작업 목적이 잘 드러나야 한다  
- 병합 전 충분한 테스트와 코드 리뷰를 수행해야 한다

---

- 배포 주기가 짧고 지속적인 통합이 필요한 경우 GitHub Flow가 더 적합하다  
- 팀의 개발 방식과 환경에 따라 전략을 선택해야 한다