# SuperClaude 명령어 가이드 🛠️

## 💡 너무 복잡하게 생각하지 마세요 - SuperClaude가 도와드립니다

**솔직한 이야기**: 이 17개 명령어를 모두 외울 필요가 없습니다. `/sc:analyze`나 `/sc:implement`부터 시작해서 어떤 일이 일어나는지 확인해보세요!

**보통 이렇게 작동합니다:**
- Claude Code에서 `/`를 입력 → 사용 가능한 명령어 확인  
- `/sc:analyze`, `/sc:build`, `/sc:improve` 같은 기본 명령어 사용
- **SuperClaude가 각 상황에 맞는 도구와 전문가를 자동으로 선택**합니다
- 편해지면 더 많은 명령어가 유용해집니다

**자동 활성화 기능이 정말 멋져요** 🪄 - SuperCladue가 여러분이 하려는 작업을 감지하고 관리 없이 관련 전문가(보안 전문가, 성능 최적화 전문가 등)를 활성화합니다. 보통 잘 작동해요! 😊

---

## 빠른 "그냥 시도해보세요" 목록 🚀

**여기서 시작하세요** (읽기 불필요):
```bash
/sc:index                           # 사용 가능한 명령어 보기
/sc:analyze src/                    # 코드를 똑똑하게 분석 
/sc:workflow feature-100-prd.md     # PRD에서 단계별 구현 워크플로우 생성
/sc:implement user-auth             # 기능 및 컴포넌트 생성 (v2 /build 대체)
/sc:build                           # 지능적인 프로젝트 빌드 시도
/sc:improve messy-file.js           # 코드 정리 시도 
/sc:troubleshoot "오류"             # 문제 해결 도움
```

**솔직히 이정도면 시작하기에 충분합니다.** 아래 내용은 어떤 다른 도구들이 있는지 궁금할 때 참고하세요. 🛠️

---

16개 SuperClaude 슬래시 명령어에 대한 실용적인 가이드입니다. 잘 작동하는 것과 아직 개선이 필요한 부분에 대해 솔직하게 말씀드립니다.

## 빠른 참조 📋

*(정말 외울 필요 없어요 - 유용해 보이는 것만 선택하면 됩니다)*

| 명령어 | 용도 | 자동 활성화 | 최적 용도 |
|---------|---------|-----------------|----------|
| `/sc:analyze` | 스마트 코드 분석 | 보안/성능 전문가 | 문제 찾기, 코드베이스 이해 |
| `/sc:build` | 지능적 빌드 | 프론트엔드/백엔드 전문가 | 컴파일, 번들링, 배포 준비 |
| `/sc:implement` | 기능 구현 | 도메인별 전문가 | 기능, 컴포넌트, API, 서비스 생성 |
| `/sc:improve` | 자동 코드 정리 | 품질 전문가 | 리팩토링, 최적화, 품질 수정 |
| `/sc:troubleshoot` | 문제 조사 | 디버그 전문가 | 디버깅, 문제 조사 |
| `/sc:test` | 스마트 테스팅 | QA 전문가 | 테스트 실행, 커버리지 분석 |
| `/sc:document` | 자동 문서화 | 작성 전문가 | README 파일, 코드 주석, 가이드 |
| `/sc:git` | 향상된 git 워크플로우 | DevOps 전문가 | 스마트 커밋, 브랜치 관리 |
| `/sc:design` | 시스템 설계 도움 | 아키텍처 전문가 | 아키텍처 계획, API 설계 |
| `/sc:explain` | 학습 도우미 | 교육 전문가 | 개념 학습, 코드 이해 |
| `/sc:cleanup` | 기술부채 감소 | 리팩토링 전문가 | 죽은 코드 제거, 파일 정리 |
| `/sc:load` | 컨텍스트 이해 | 분석 전문가 | 프로젝트 분석, 코드베이스 이해 |
| `/sc:estimate` | 스마트 추정 | 계획 전문가 | 시간/노력 계획, 복잡도 분석 |
| `/sc:spawn` | 복잡한 워크플로우 | 오케스트레이션 시스템 | 다단계 연산, 워크플로우 자동화 |
| `/sc:task` | 프로젝트 관리 | 계획 시스템 | 장기 기능 계획, 작업 추적 |
| `/sc:workflow` | 구현 계획 | 워크플로우 시스템 | PRD에서 단계별 워크플로우 생성 |
| `/sc:index` | 명령어 네비게이션 | 도움말 시스템 | 작업에 맞는 명령어 찾기 |

**전문가 팁**: 유용해 보이는 것들만 시도해보세요. SuperClaude는 보통 각 상황에 맞는 도움이 되는 전문가와 도구를 활성화하려고 합니다! 🎯

## 개발 명령어 🔨

### `/workflow` - 구현 워크플로우 생성기 🗺️
**기능**: PRD와 기능 요구사항을 분석하여 포괄적인 단계별 구현 워크플로우를 생성합니다.

**도움이 되는 부분**: PRD를 받아서 전문가 가이드, 의존성 매핑, 작업 오케스트레이션이 포함된 구조화된 구현 계획으로 분해합니다! 🎯

**언제 사용하나요**:
- PRD나 사양서에서 새 기능 시작할 때
- 명확한 구현 로드맵이 필요할 때
- 구현 전략에 대한 전문가 가이드를 원할 때
- 여러 의존성이 있는 복잡한 기능을 계획할 때

**마법**: 기능 요구사항에 따라 적절한 전문가 페르소나(아키텍트, 보안, 프론트엔드, 백엔드)와 MCP 서버(패턴용 Context7, 복잡한 분석용 Sequential)를 자동 활성화합니다.

**예시**:
```bash
/sc:workflow docs/feature-100-prd.md --strategy systematic --c7 --sequential
/sc:workflow "사용자 인증 시스템" --persona security --output detailed
/sc:workflow payment-api --strategy mvp --risks --dependencies
```

**얻을 수 있는 것**:
- **로드맵 형식**: 일정과 함께 단계별 구현 계획
- **작업 형식**: 에픽, 스토리, 실행 가능한 작업으로 구성
- **상세 형식**: 시간 추정이 포함된 단계별 지침
- **위험 평가**: 잠재적 문제와 완화 전략
- **의존성 매핑**: 내부 및 외부 의존성
- **전문가 가이드**: 도메인별 모범 사례와 패턴

### `/implement` - 기능 구현
**기능**: 지능적인 전문가 활성화를 통해 기능, 컴포넌트, 기능을 구현합니다.

**도움이 되는 부분**: SuperClaude가 구현하는 내용에 따라 적절한 전문가(프론트엔드, 백엔드, 보안)와 도구를 자동 활성화합니다! 🎯

**언제 사용하나요**:
- 새 기능이나 컴포넌트 생성 (v2의 `/build` 기능 대체)
- API, 서비스, 모듈 구현
- 현대적인 프레임워크로 UI 컴포넌트 구축
- 비즈니스 로직과 통합 개발

**기본 문법**:
```bash
/sc:implement user authentication system      # 완전한 기능 구현
/sc:implement --type component LoginForm      # 특정 컴포넌트 생성  
/sc:implement --type api user-management      # API 엔드포인트 구축
/sc:implement --framework react dashboard     # 프레임워크별 구현
```

**유용한 플래그**:
- `--type component|api|service|feature|module` - 구현 유형
- `--framework react|vue|express|django|etc` - 대상 프레임워크
- `--safe` - 보수적인 구현 접근법
- `--iterative` - 검증을 통한 단계별 개발
- `--with-tests` - 테스트 구현 포함
- `--documentation` - 코드와 함께 문서 생성

**실제 예시**:
```bash
/sc:implement user authentication --type feature --with-tests
/sc:implement dashboard component --type component --framework react
/sc:implement REST API for orders --type api --safe
/sc:implement payment processing --type service --iterative
/sc:implement search functionality --framework vue --documentation
```

**자동 활성화 패턴**:
- **프론트엔드**: UI 컴포넌트, React/Vue/Angular → 프론트엔드 페르소나 + Magic MCP
- **백엔드**: API, 서비스, 데이터베이스 → 백엔드 페르소나 + Context7
- **보안**: 인증, 결제, 민감한 데이터 → 보안 페르소나 + 검증
- **복잡한 기능**: 다단계 구현 → Sequential MCP + 아키텍트 페르소나

**주의사항**:
- 더 나은 결과를 위해 `--type` 지정 (컴포넌트 vs 서비스 vs 기능)
- 특정 기술 스택 작업 시 `--framework` 사용
- 프로덕션 코드는 `--safe`, 복잡한 기능은 `--iterative` 시도
- 기억하세요: 실제 코드 구현을 위해 v2의 `/build`를 대체합니다

---

### `/build` - 프로젝트 빌드
**기능**: 스마트 오류 처리와 함께 프로젝트를 빌드, 컴파일, 패키징합니다.

**쉬운 방법**: 그냥 `/sc:build`를 입력하면 SuperClaude가 여러분의 빌드 시스템을 알아내려고 시도합니다! 🎯

**언제 사용하나요**:
- 프로젝트를 컴파일/번들링해야 할 때 (그냥 `/sc:build` 시도)
- 빌드 프로세스가 실패하고 디버깅 도움이 필요할 때  
- 빌드 최적화 설정 (필요한 것을 감지하려고 시도)
- 배포 준비

**기본 문법**:
```bash
/sc:build                          # 현재 프로젝트 빌드
/sc:build --type prod              # 프로덕션 빌드
/sc:build --clean                  # 클린 빌드 (이전 아티팩트 제거)
/sc:build --optimize               # 최적화 활성화
/sc:build src/                     # 특정 디렉토리 빌드
```

**유용한 플래그**:
- `--type dev|prod|test` - 빌드 유형
- `--clean` - 빌드 전 정리  
- `--optimize` - 빌드 최적화 활성화
- `--verbose` - 상세한 빌드 출력 표시

**실제 예시**:
```bash
/sc:build --type prod --optimize   # 최적화가 포함된 프로덕션 빌드
/sc:build --clean --verbose        # 상세 출력이 포함된 클린 빌드
/sc:build src/components           # 컴포넌트 폴더만 빌드
```

**주의사항**:
- 일반적인 빌드 도구(npm, webpack 등)와 가장 잘 작동
- 매우 사용자 정의된 빌드 설정과는 어려움을 겪을 수 있음
- 빌드 도구가 PATH에 있는지 확인

---

### `/design` - 시스템 및 컴포넌트 설계
**기능**: 시스템 아키텍처, API 설계, 컴포넌트 사양을 생성합니다.

**언제 사용하나요**:
- 새 기능이나 시스템 계획
- API나 데이터베이스 설계 필요
- 컴포넌트 아키텍처 생성
- 시스템 관계 문서화

**기본 문법**:
```bash
/sc:design user-auth-system        # 사용자 인증 시스템 설계
/sc:design --type api auth         # API 부분만 설계
/sc:design --format spec payment   # 공식 사양 생성
```

**유용한 플래그**:
- `--type architecture|api|component|database` - 설계 초점
- `--format diagram|spec|code` - 출력 형식
- `--iterative` - 반복을 통한 설계 개선

**실제 예시**:
```bash
/sc:design --type api user-management    # 사용자 관리 API 설계
/sc:design --format spec chat-system     # 채팅 시스템 사양 생성
/sc:design --type database ecommerce     # 데이터베이스 스키마 설계
```

**주의사항**:
- 코드 생성보다는 개념적
- 출력 품질은 요구사항을 얼마나 명확하게 설명하느냐에 따라 달라짐
- 계획 단계에는 좋지만 구현 세부사항에는 덜 유용

## 분석 명령어 🔍

### `/analyze` - 코드 분석  
**기능**: 코드 품질, 보안, 성능, 아키텍처의 종합적인 분석.

**도움이 되는 부분**: SuperClaude가 필요한 분석 유형을 감지하고 보통 관련 전문가를 선택합니다! 🔍

**언제 사용하나요**:
- 익숙하지 않은 코드베이스 이해 (아무 폴더나 지정)
- 보안 취약점 찾기 (보안 전문가가 보통 도움)
- 성능 병목 현상 찾기 (성능 전문가가 보통 도움)
- 코드 품질 평가 (품질 전문가가 자주 참여)

**기본 문법**:
```bash
/sc:analyze src/                   # 전체 src 디렉토리 분석
/sc:analyze --focus security       # 보안 문제에 초점
/sc:analyze --depth deep app.js    # 특정 파일의 심층 분석
```

**유용한 플래그**:
- `--focus quality|security|performance|architecture` - 분석 초점
- `--depth quick|deep` - 분석 철저함
- `--format text|json|report` - 출력 형식

**실제 예시**:
```bash
/sc:analyze --focus security --depth deep     # 심층 보안 분석
/sc:analyze --focus performance src/api/      # API 성능 분석
/sc:analyze --format report .                 # 분석 보고서 생성
```

**주의사항**:
- 큰 코드베이스에서는 시간이 걸릴 수 있음
- 보안 분석은 꽤 좋고, 성능 분석은 다양함
- 일반적인 언어(JS, Python 등)와 가장 잘 작동

---

### `/troubleshoot` - 문제 조사
**기능**: 체계적인 디버깅과 문제 조사.

**언제 사용하나요**:
- 뭔가 고장났는데 이유를 모를 때
- 체계적인 디버깅 접근이 필요할 때
- 오류 메시지가 혼란스러울 때
- 성능 문제 조사

**기본 문법**:
```bash
/sc:troubleshoot "로그인이 작동하지 않음"     # 로그인 문제 조사
/sc:troubleshoot --logs error.log        # 오류 로그 분석
/sc:troubleshoot performance             # 성능 문제 해결
```

**유용한 플래그**:
- `--logs <file>` - 로그 파일 분석 포함
- `--systematic` - 구조화된 디버깅 접근 사용
- `--focus network|database|frontend` - 초점 영역

**실제 예시**:
```bash
/sc:troubleshoot "API가 500 반환" --logs server.log
/sc:troubleshoot --focus database "느린 쿼리"
/sc:troubleshoot "빌드 실패" --systematic
```

**주의사항**:
- 구체적인 오류 설명과 함께 더 잘 작동
- 관련 오류 메시지와 로그를 가능하면 포함
- 명백한 것부터 제안할 수 있음 (보통 좋은 일!)

---

### `/explain` - 교육적 설명
**기능**: 코드, 개념, 기술을 교육적인 방식으로 설명합니다.

**언제 사용하나요**:
- 새로운 기술이나 패턴 학습
- 복잡한 코드 이해
- 팀원을 위한 명확한 설명 필요
- 까다로운 개념 문서화

**기본 문법**:
```bash
/sc:explain async/await               # async/await 개념 설명
/sc:explain --code src/utils.js       # 특정 코드 파일 설명
/sc:explain --beginner React hooks    # 초보자 친화적 설명
```

**유용한 플래그**:
- `--beginner` - 더 간단한 설명
- `--advanced` - 기술적 깊이
- `--code <file>` - 특정 코드 설명
- `--examples` - 실용적인 예시 포함

**실제 예시**:
```bash
/sc:explain --beginner "REST API가 무엇인가요"
/sc:explain --code src/auth.js --advanced
/sc:explain --examples "React context 패턴"
```

**주의사항**:
- 잘 알려진 개념에는 좋지만 매우 틈새 주제에는 어려움을 겪을 수 있음
- 막연한 "이 코드베이스 설명"보다는 구체적인 질문이 더 좋음
- 경험 수준에 대한 컨텍스트 포함

## 품질 명령어 ✨

### `/improve` - 코드 개선
**기능**: 코드 품질, 성능, 유지보수성의 체계적인 개선.

**언제 사용하나요**:
- 지저분한 코드 리팩토링
- 성능 최적화
- 모범 사례 적용
- 오래된 코드 현대화

**기본 문법**:
```bash
/sc:improve src/legacy/            # 레거시 코드 개선
/sc:improve --type performance     # 성능에 초점
/sc:improve --safe src/utils.js    # 안전하고 위험도 낮은 개선만
```

**유용한 플래그**:
- `--type quality|performance|maintainability|style` - 개선 초점
- `--safe` - 위험도 낮은 변경사항만 적용
- `--preview` - 실제 변경 없이 바뀔 내용 표시

**실제 예시**:
```bash
/sc:improve --type performance --safe src/api/
/sc:improve --preview src/components/LegacyComponent.js
/sc:improve --type style . --safe
```

**주의사항**:
- 변경하고 싶은 내용을 보려면 항상 `--preview`를 먼저 사용
- `--safe`가 친구 - 위험한 리팩토링 방지
- 전체 코드베이스보다는 작은 파일/모듈에서 가장 잘 작동

---

### `/cleanup` - 기술부채 감소
**기능**: 죽은 코드, 사용하지 않는 import, 파일 구조 정리를 제거합니다.

**언제 사용하나요**:
- 코드베이스가 어수선하게 느껴질 때
- 사용하지 않는 import/변수가 많을 때
- 파일 정리가 엉망일 때
- 주요 리팩토링 전에

**기본 문법**:
```bash
/sc:cleanup src/                   # src 디렉토리 정리
/sc:cleanup --dead-code            # 죽은 코드 제거에 초점
/sc:cleanup --imports package.js   # 특정 파일의 import 정리
```

**유용한 플래그**:
- `--dead-code` - 사용하지 않는 코드 제거
- `--imports` - import 문 정리
- `--files` - 파일 구조 재정리
- `--safe` - 보수적인 정리만

**실제 예시**:
```bash
/sc:cleanup --dead-code --safe src/utils/
/sc:cleanup --imports src/components/
/sc:cleanup --files . --safe
```

**주의사항**:
- 공격적일 수 있음 - 항상 변경사항을 신중히 검토
- 모든 죽은 코드를 잡지 못할 수 있음 (특히 동적 import)
- 전체 프로젝트보다는 작은 섹션에서 실행하는 것이 좋음

---

### `/test` - 테스팅 및 품질 보증
**기능**: 테스트 실행, 커버리지 보고서 생성, 테스트 품질 유지.

**언제 사용하나요**:
- 테스트 스위트 실행
- 테스트 커버리지 확인
- 테스트 보고서 생성
- 지속적인 테스팅 설정

**기본 문법**:
```bash
/sc:test                           # 모든 테스트 실행
/sc:test --type unit               # 유닛 테스트만 실행
/sc:test --coverage                # 커버리지 보고서 생성
/sc:test --watch src/              # 개발용 감시 모드
```

**유용한 플래그**:
- `--type unit|integration|e2e|all` - 테스트 유형
- `--coverage` - 커버리지 보고서 생성
- `--watch` - 감시 모드에서 테스트 실행
- `--fix` - 실패한 테스트 자동 수정 시도

**실제 예시**:
```bash
/sc:test --type unit --coverage
/sc:test --watch src/components/
/sc:test --type e2e --fix
```

**주의사항**:
- 테스트 프레임워크가 제대로 구성되어 있어야 함
- 커버리지 보고서는 기존 테스트 설정에 따라 달라짐
- `--fix`는 실험적 - 변경사항 검토

## 문서화 명령어 📝

### `/document` - 집중된 문서화
**기능**: 특정 컴포넌트, 함수, 기능에 대한 문서를 생성합니다.

**언제 사용하나요**:
- README 파일 필요
- API 문서 작성
- 코드 주석 추가
- 사용자 가이드 생성

**기본 문법**:
```bash
/sc:document src/api/auth.js       # 인증 모듈 문서화
/sc:document --type api            # API 문서화
/sc:document --style brief README  # 간단한 README 파일
```

**유용한 플래그**:
- `--type inline|external|api|guide` - 문서화 유형
- `--style brief|detailed` - 세부사항 수준
- `--template` - 특정 문서화 템플릿 사용

**실제 예시**:
```bash
/sc:document --type api src/controllers/
/sc:document --style detailed --type guide user-onboarding
/sc:document --type inline src/utils/helpers.js
```

**주의사항**:
- 전체 프로젝트보다는 특정 파일/함수와 더 잘 작동
- 품질은 코드가 얼마나 잘 구조화되어 있느냐에 따라 달라짐
- 프로젝트의 문서화 스타일에 맞추려면 약간의 편집이 필요할 수 있음

## 프로젝트 관리 명령어 📊

### `/estimate` - 프로젝트 추정
**기능**: 개발 작업의 시간, 노력, 복잡도를 추정합니다.

**언제 사용하나요**:
- 새 기능 계획
- 스프린트 계획
- 프로젝트 복잡도 이해
- 리소스 배분

**기본 문법**:
```bash
/sc:estimate "사용자 인증 추가"    # 인증 기능 추정
/sc:estimate --detailed shopping-cart     # 상세 분석
/sc:estimate --complexity user-dashboard  # 복잡도 분석
```

**유용한 플래그**:
- `--detailed` - 작업의 상세 분석
- `--complexity` - 기술적 복잡도에 초점
- `--team-size <n>` - 추정에 팀 크기 고려

**실제 예시**:
```bash
/sc:estimate --detailed "결제 시스템 구현"
/sc:estimate --complexity --team-size 3 "마이크로서비스로 마이그레이션"
/sc:estimate "실시간 채팅 추가" --detailed
```

**주의사항**:
- 추정은 대략적 - 절대적이 아닌 시작점으로 사용
- 명확하고 구체적인 기능 설명과 더 잘 작동
- 기술 스택에 대한 팀의 경험 고려

---

### `/task` - 장기 프로젝트 관리
**기능**: 복잡하고 다중 세션 개발 작업과 기능을 관리합니다.

**언제 사용하나요**:
- 며칠/몇 주가 걸리는 기능 계획
- 대규모 프로젝트 분해
- 세션 간 진행 상황 추적
- 팀 작업 조정

**기본 문법**:
```bash
/sc:task create "사용자 대시보드 구현"  # 새 작업 생성
/sc:task status                            # 작업 상태 확인
/sc:task breakdown "결제 통합"    # 하위 작업으로 분해
```

**유용한 플래그**:
- `create` - 새 장기 작업 생성
- `status` - 현재 작업 상태 확인
- `breakdown` - 큰 작업을 작은 작업으로 분해
- `--priority high|medium|low` - 작업 우선순위 설정

**실제 예시**:
```bash
/sc:task create "REST를 GraphQL로 마이그레이션" --priority high
/sc:task breakdown "전자상거래 체크아웃 플로우"
/sc:task status
```

**주의사항**:
- 여전히 실험적 - 세션 간에 항상 안정적으로 유지되지 않음 😅
- 실제 프로젝트 관리보다는 계획에 더 적합
- 요구사항을 구체적으로 명시할 때 가장 잘 작동

---

### `/spawn` - 복잡한 작업 오케스트레이션
**기능**: 복잡하고 다단계 작업과 워크플로우를 조정합니다.

**언제 사용하나요**:
- 여러 도구/시스템을 포함하는 작업
- 병렬 워크플로우 조정
- 복잡한 배포 프로세스
- 다단계 데이터 처리

**기본 문법**:
```bash
/sc:spawn deploy-pipeline          # 배포 오케스트레이션
/sc:spawn --parallel migrate-data  # 병렬 데이터 마이그레이션
/sc:spawn setup-dev-environment    # 복잡한 환경 설정
```

**유용한 플래그**:
- `--parallel` - 가능한 경우 병렬로 작업 실행
- `--sequential` - 순차 실행 강제
- `--monitor` - 작업 진행 상황 모니터링

**실제 예시**:
```bash
/sc:spawn --parallel "스테이징에 테스트 및 배포"
/sc:spawn setup-ci-cd --monitor
/sc:spawn --sequential database-migration
```

**주의사항**:
- 가장 복잡한 명령어 - 약간의 거친 부분 예상
- 임시 작업보다는 잘 정의된 워크플로우에 더 적합
- 올바르게 하려면 여러 반복이 필요할 수 있음

## 버전 제어 명령어 🔄

### `/git` - 향상된 Git 작업
**기능**: 지능적인 커밋 메시지와 워크플로우 최적화를 통한 Git 작업.

**언제 사용하나요**:
- 더 좋은 메시지로 커밋하기
- 브랜치 관리
- 복잡한 git 워크플로우
- Git 문제 해결

**기본 문법**:
```bash
/sc:git commit                     # 자동 생성 메시지로 스마트 커밋
/sc:git --smart-commit add .       # 스마트 메시지로 추가 및 커밋
/sc:git branch feature/new-auth    # 새 브랜치 생성 및 전환
```

**유용한 플래그**:
- `--smart-commit` - 지능적인 커밋 메시지 생성
- `--branch-strategy` - 브랜치 명명 규칙 적용
- `--interactive` - 복잡한 작업을 위한 대화형 모드

**실제 예시**:
```bash
/sc:git --smart-commit "로그인 버그 수정"
/sc:git branch feature/user-dashboard --branch-strategy
/sc:git merge develop --interactive
```

**주의사항**:
- 스마트 커밋 메시지는 꽤 좋지만 검토하세요
- 일반적인 git 워크플로우를 따른다고 가정
- 나쁜 git 습관을 고치지는 않음 - 그냥 쉽게 만들 뿐

## 유틸리티 명령어 🔧

### `/index` - 명령어 네비게이션
**기능**: 작업에 맞는 올바른 명령어를 찾는 데 도움.

**언제 사용하나요**:
- 어떤 명령어를 사용할지 확실하지 않을 때
- 사용 가능한 명령어 탐색
- 명령어 기능에 대해 학습

**기본 문법**:
```bash
/sc:index                          # 모든 명령어 나열
/sc:index testing                  # 테스팅 관련 명령어 찾기
/sc:index --category analysis      # 분석 카테고리의 명령어
```

**유용한 플래그**:
- `--category <cat>` - 명령어 카테고리별 필터링
- `--search <term>` - 명령어 설명 검색

**실제 예시**:
```bash
/sc:index --search "performance"
/sc:index --category quality
/sc:index git
```

**주의사항**:
- 간단하지만 발견에 유용
- 16개 명령어를 모두 기억하려고 하는 것보다 좋음

---

### `/load` - 프로젝트 컨텍스트 로딩
**기능**: 더 나은 이해를 위해 프로젝트 컨텍스트를 로드하고 분석합니다.

**언제 사용하나요**:
- 익숙하지 않은 프로젝트 작업 시작
- 프로젝트 구조 이해 필요
- 주요 변경 전에
- 팀 멤버 온보딩

**기본 문법**:
```bash
/sc:load                           # 현재 프로젝트 컨텍스트 로드
/sc:load src/                      # 특정 디렉토리 컨텍스트 로드
/sc:load --deep                    # 프로젝트 구조의 심층 분석
```

**유용한 플래그**:
- `--deep` - 프로젝트의 종합적인 분석
- `--focus <area>` - 특정 프로젝트 영역에 초점
- `--summary` - 프로젝트 요약 생성

**실제 예시**:
```bash
/sc:load --deep --summary
/sc:load src/components/ --focus architecture
/sc:load . --focus dependencies
```

**주의사항**:
- 큰 프로젝트에서는 시간이 걸릴 수 있음
- 개발 중보다는 프로젝트 시작 시 더 유용
- 온보딩에 도움이 되지만 좋은 문서를 대체하지는 않음

## 명령어 팁 및 패턴 💡

### 효과적인 플래그 조합
```bash
# 안전한 개선 워크플로우
/sc:improve --preview src/component.js    # 바뀔 내용 보기
/sc:improve --safe src/component.js       # 안전한 변경만 적용

# 포괄적인 분석
/sc:analyze --focus security --depth deep
/sc:test --coverage
/sc:document --type api

# 스마트 git 워크플로우
/sc:git add .
/sc:git --smart-commit --branch-strategy

# 프로젝트 이해 워크플로우
/sc:load --deep --summary
/sc:analyze --focus architecture
/sc:document --type guide
```

### 일반적인 워크플로우

**새 프로젝트 온보딩**:
```bash
/sc:load --deep --summary
/sc:analyze --focus architecture
/sc:test --coverage
/sc:document README
```

**버그 조사**:
```bash
/sc:troubleshoot "특정 오류 메시지" --logs
/sc:analyze --focus security
/sc:test --type unit affected-component
```

**코드 품질 개선**:
```bash
/sc:analyze --focus quality
/sc:improve --preview src/
/sc:cleanup --safe
/sc:test --coverage
```

**배포 전 체크리스트**:
```bash
/sc:test --type all --coverage
/sc:analyze --focus security
/sc:build --type prod --optimize
/sc:git --smart-commit
```

### 명령어 문제 해결

**명령어가 예상대로 작동하지 않나요?**
- 모든 옵션을 보려면 `--help` 추가
- 가능한 경우 `--preview`나 `--safe` 플래그 사용
- 작은 범위부터 시작 (전체 프로젝트 vs 단일 파일)

**분석이 너무 오래 걸리나요?**
- 범위를 좁히려면 `--focus` 사용
- 심층 분석 대신 `--depth quick` 시도
- 먼저 작은 디렉토리 분석

**빌드/테스트 명령어가 실패하나요?**
- 도구가 PATH에 있는지 확인
- 구성 파일이 예상 위치에 있는지 확인
- 먼저 기본 명령어를 직접 실행해보기

**어떤 명령어를 사용할지 확실하지 않나요?**
- 사용 가능한 명령어를 탐색하려면 `/index` 사용
- 위의 빠른 참조 표 보기
- 가장 구체적인 명령어부터 시도한 다음 더 광범위한 것으로

---

## 최종 참고사항 📝

**이 명령어들에 대한 진실** 💯:
- **그냥 시도해보세요** - 이 가이드를 먼저 공부할 필요 없음
- **기본부터 시작** - `/analyze`, `/build`, `/improve`가 대부분의 필요를 충족
- **자동 활성화가 작동하도록 두세요** - SuperClaude가 보통 도움이 되는 전문가를 선택
- **자유롭게 실험** - 먼저 무슨 일이 일어날지 보고 싶으면 `--preview` 사용

**여전히 거친 부분들:**
- 복잡한 오케스트레이션 (spawn, task)은 약간 불안정할 수 있음
- 일부 분석은 프로젝트 설정에 크게 의존
- 일부 명령어에서 오류 처리가 더 나아질 수 있음

**계속 개선되고 있음:**
- 사용자 피드백을 바탕으로 명령어를 적극적으로 개선
- 최신 명령어 (analyze, improve)가 더 잘 작동하는 경향
- 자동 활성화가 계속 똑똑해지고 있음

**이것을 외우는 것에 대해 스트레스받지 마세요** 🧘‍♂️
- SuperClaude는 사용을 통해 발견할 수 있도록 설계됨
- `/`를 입력하여 사용 가능한 명령어 보기
- 명령어는 `--help`를 사용할 때 할 수 있는 일을 제안
- 지능적인 라우팅이 대부분의 복잡성을 처리

**도움이 필요하신가요?** 막히면 GitHub 이슈를 확인하거나 새 이슈를 만드세요! 🚀

---

*즐거운 코딩! 이 가이드의 대부분을 건너뛰고 실습으로 배울 수 있다는 걸 기억하세요. 🎯* 