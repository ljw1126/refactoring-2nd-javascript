## 리팩터링 2판 실습

> 리팩터링 ‘적용 방법’을 아는 것과 ‘제때 적용’할 줄 아는 것은 다르다. 리팩터링을 언제 시작하고 언제 그만할지를 판단하는 일은 리팩터링의 작동 원리를 아는 것 못지않게 중요하다. (Chapter3. 코드에서 나는 악취)

### 🔹 개발 환경 및 도구
- 사용 언어: JavaScript
- 테스트 프레임워크: Jest
- 형상관리: Git

### 🔹 의존성 (Dependencies)
- **ESLint**: 코드 스타일 및 린트 검사 (`eslint`)
- **Husky**: Git Hook을 활용하여 커밋 전 자동 실행 (`husky`)
- **Lint-Staged**: 스테이징된 파일만 대상으로 린트 적용 (`lint-staged`)

### 🔹 코드 컨벤션 (Convention)
- **ESLint + Prettier 조합 사용**: 코드 스타일 일관성 유지
- `lint-staged`를 사용하여 **커밋 전에 특정 파일만 린트 적용**
- `husky`를 이용하여 **Git Hook 단계에서 자동 실행**

### 🔹 Git Hook 설정
- `.husky/pre-commit`에 `lint-staged` 설정 추가하여 자동화