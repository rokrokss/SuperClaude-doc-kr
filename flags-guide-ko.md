# SuperClaude 플래그 사용자 가이드 🏁

## 🤖 대부분의 플래그는 자동으로 활성화됩니다 - 걱정하지 마세요!

**솔직한 진실**: 이 플래그들을 외울 필요가 없습니다. SuperClaude는 여러분이 하는 작업을 바탕으로 도움이 되는 플래그를 추가하려고 시도합니다!

**실제로 일어나는 일:**
- `/analyze auth.js`를 입력
- SuperClaude가 보안 관련 코드를 감지
- **보통 추가**: `--persona-security`, `--focus security`, `--validate`
- 플래그 관리 없이 전문적인 보안 분석을 받게 됩니다

**언제 수동으로 플래그를 사용할까요?**
- SuperClaude가 선택한 것을 **무시**하고 싶을 때 (드물게)
- 특정 측면에 **호기심**이 있을 때 (`--focus performance`)
- 다른 접근법을 **실험**해보고 싶을 때

**결론**: 기본 명령어를 사용하고 자동 활성화가 작동하도록 두세요. 이 플래그들은 필요해서가 아니라 원할 때 사용할 수 있습니다. 🎯

---

## 🚀 그냥 시도해보세요 (플래그 지식 불필요)

```bash
# 플래그 지식 없이도 이것들은 훌륭하게 작동합니다:
/sc:analyze src/                    # 올바른 분석 플래그를 자동 선택
/sc:build                          # 프로젝트를 기반으로 자동 최적화  
/sc:improve messy-code.js          # 품질 및 안전 플래그를 자동 활성화
/sc:troubleshoot "이상한 오류"     # 디버깅 및 분석 플래그를 자동 활성화
```

**보세요? 플래그가 필요 없습니다.** 아래 모든 내용은 무슨 일이 일어나고 있는지 궁금할 때를 위한 것입니다.

---

SuperClaude의 플래그 시스템에 대한 실용적인 가이드입니다. 플래그는 SuperClaude의 동작을 변경하는 명령줄 옵션과 같습니다 - 명령어를 위한 슈퍼파워라고 생각하세요.

## 플래그란 무엇인가요? 🤔

**플래그는 수정자**로 SuperClaude가 요청을 처리하는 방식을 변경합니다. 명령어 다음에 나오며 `--`로 시작합니다.

**기본 문법** (하지만 보통 알 필요는 없습니다):
```bash
/sc:command --flag-name
/sc:command --flag-name value  
/sc:analyze src/ --focus security --depth deep
```

**실제로 플래그가 작동하는 방식**:
1. **자동 활성화** - SuperClaude가 컨텍스트를 기반으로 추가 (주요 방식! 🎯)
2. **수동 재정의** - 다른 동작을 원할 때 명시적으로 추가 가능

**플래그가 존재하는 이유** (대부분 자동 이점):
- 더 나은, 더 집중된 결과 얻기
- 올바른 사고 깊이를 자동 활성화
- 유용할 때 특별한 기능에 연결
- 작업에 따라 속도나 세부사항 최적화
- 실제로 작업하는 것에 주의를 집중

**핵심 포인트**: SuperClaude가 플래그 선택을 지능적으로 처리하므로 여러분이 생각할 필요가 없습니다! 🧠

## 플래그 카테고리 📂

### 계획 및 분석 플래그 🧠

SuperClaude가 요청에 대해 얼마나 깊이 생각할지 제어합니다.

#### `--plan`
**기능**: 실행 전에 실행 계획 표시  
**언제 사용**: SuperClaude가 무엇을 할지 먼저 보고 싶을 때  
**예시**: `/build --plan` - 실행하기 전에 빌드 단계 보기

#### `--think`
**기능**: 다중 파일 분석 (~4K 토큰)  
**언제 사용**: 여러 파일과 관련된 복잡한 문제  
**자동 활성화**: 5개 이상 파일의 import 체인, 10개 이상 참조의 모듈 간 호출  
**예시**: `/analyze complex-system/ --think`

#### `--think-hard` 
**기능**: 심층 아키텍처 분석 (~10K 토큰)  
**언제 사용**: 시스템 전체 문제, 아키텍처 결정  
**자동 활성화**: 시스템 리팩토링, 3개 이상 모듈의 병목  
**예시**: `/improve legacy-system/ --think-hard`

#### `--ultrathink`
**기능**: 최대 깊이 분석 (~32K 토큰)  
**언제 사용**: 중요한 시스템 재설계, 복잡한 디버깅  
**자동 활성화**: 레거시 현대화, 중요한 취약점  
**예시**: `/troubleshoot "전체 인증 시스템 고장" --ultrathink`

**💡 팁**: `--think`부터 시작하여, 필요한 경우에만 더 깊이 들어가세요. 더 많은 사고 = 더 느리지만 더 철저함.

---

### 효율성 및 제어 플래그 ⚡

출력 스타일, 안전성, 성능을 제어합니다.

#### `--uc` / `--ultracompressed`
**기능**: 기호를 사용하여 60-80% 토큰 감소  
**언제 사용**: 대규모 작업, 컨텍스트가 가득 찰 때  
**자동 활성화**: 컨텍스트 사용량 >75%, 대규모 작업  
**예시**: `/analyze huge-codebase/ --uc`

#### `--safe-mode`
**기능**: 최대 검증, 보수적 실행  
**언제 사용**: 프로덕션 환경, 위험한 작업  
**자동 활성화**: 리소스 사용량 >85%, 프로덕션 환경  
**예시**: `/improve production-code/ --safe-mode`

#### `--validate`
**기능**: 작업 전 검증 및 위험 평가  
**언제 사용**: 변경하기 전에 확인하고 싶을 때  
**자동 활성화**: 위험 점수 >0.7  
**예시**: `/cleanup legacy/ --validate`

#### `--verbose`
**기능**: 최대 세부사항 및 설명  
**언제 사용**: 학습, 디버깅, 전체 컨텍스트 필요  
**예시**: `/build --verbose` - 모든 빌드 단계 보기

#### `--answer-only`
**기능**: 작업 생성 없이 직접 응답  
**언제 사용**: 빠른 질문, 워크플로우 자동화를 원하지 않을 때  
**예시**: `/explain React hooks --answer-only`

**💡 팁**: `--uc`는 큰 작업에 좋습니다. 중요한 것에는 `--safe-mode`. 학습할 때는 `--verbose`.

---

### MCP 서버 플래그 🔧

MCP 서버를 통해 전문화된 기능을 활성화합니다.

#### `--c7` / `--context7`
**기능**: 공식 라이브러리 문서를 위한 Context7 활성화  
**언제 사용**: 프레임워크 작업, 공식 문서 필요  
**자동 활성화**: 외부 라이브러리 import, 프레임워크 질문  
**예시**: `/build react-app/ --c7` - React 모범 사례 얻기

#### `--seq` / `--sequential`
**기능**: 복잡한 다단계 분석을 위한 Sequential 활성화  
**언제 사용**: 복잡한 디버깅, 시스템 설계  
**자동 활성화**: 복잡한 디버깅, `--think` 플래그  
**예시**: `/troubleshoot "인증 플로우 고장" --seq`

#### `--magic`
**기능**: UI 컴포넌트 생성을 위한 Magic 활성화  
**언제 사용**: UI 컴포넌트 생성, 디자인 시스템  
**자동 활성화**: UI 컴포넌트 요청, 프론트엔드 페르소나  
**예시**: `/build dashboard --magic` - 현대적인 UI 컴포넌트 얻기

#### `--play` / `--playwright`
**기능**: 브라우저 자동화 및 테스팅을 위한 Playwright 활성화  
**언제 사용**: E2E 테스팅, 성능 모니터링  
**자동 활성화**: 테스트 워크플로우, QA 페르소나  
**예시**: `/test e2e --play`

#### `--all-mcp`
**기능**: 모든 MCP 서버를 동시에 활성화  
**언제 사용**: 복잡한 다중 도메인 문제  
**자동 활성화**: 문제 복잡도 >0.8, 다중 도메인 지표  
**예시**: `/analyze entire-app/ --all-mcp`

#### `--no-mcp`
**기능**: 모든 MCP 서버 비활성화, 네이티브 도구만  
**언제 사용**: 더 빠른 실행, 전문화된 기능 불필요  
**예시**: `/analyze simple-script.js --no-mcp`

**💡 팁**: MCP 서버는 기능을 추가하지만 더 많은 토큰을 사용합니다. 문서용 `--c7`, 사고용 `--seq`, UI용 `--magic`.

---

### 고급 오케스트레이션 플래그 🎭

복잡한 작업과 워크플로우를 위해.

#### `--delegate [files|folders|auto]`
**기능**: 병렬 처리를 위한 하위 에이전트 위임 활성화  
**언제 사용**: 대규모 코드베이스, 복잡한 분석  
**자동 활성화**: 7개 이상 디렉토리 또는 50개 이상 파일  
**옵션**:
- `files` - 개별 파일 분석 위임
- `folders` - 디렉토리 수준 분석 위임  
- `auto` - 스마트 위임 전략

**예시**: `/analyze monorepo/ --delegate auto`

#### `--wave-mode [auto|force|off]`
**기능**: 복합 지능을 갖춘 다단계 실행  
**언제 사용**: 복잡한 개선, 체계적 분석  
**자동 활성화**: 복잡도 >0.8 AND 파일 >20 AND 작업 유형 >2  
**예시**: `/improve legacy-system/ --wave-mode force`

#### `--loop`
**기능**: 반복적 개선 모드  
**언제 사용**: 품질 개선, 정제 작업  
**자동 활성화**: polish, refine, enhance 키워드  
**예시**: `/improve messy-code.js --loop`

#### `--concurrency [n]`
**기능**: 최대 동시 하위 에이전트 제어 (1-15)  
**언제 사용**: 리소스 사용량 제어  
**예시**: `/analyze --delegate auto --concurrency 3`

**💡 팁**: 이것들은 강력하지만 복잡합니다. 큰 프로젝트에는 `--delegate auto`, 개선에는 `--loop`부터 시작하세요.

---

### 초점 및 범위 플래그 🎯

SuperClaude의 주의를 특정 영역으로 유도합니다.

#### `--scope [level]`
**옵션**: file, module, project, system  
**기능**: 분석 범위 설정  
**예시**: `/analyze --scope module auth/`

#### `--focus [domain]`
**옵션**: performance, security, quality, architecture, accessibility, testing  
**기능**: 특정 도메인에 분석 집중  
**예시**: `/analyze --focus security --scope project`

#### 페르소나 플래그
**사용 가능한 페르소나**: architect, frontend, backend, analyzer, security, mentor, refactorer, performance, qa, devops, scribe  
**기능**: 전문가 행동 패턴 활성화  
**예시**: `/analyze --persona-security` - 보안 중심 분석

**💡 팁**: `--focus`는 표적 분석에 좋습니다. 페르소나는 자동 활성화되지만 수동 제어도 도움이 됩니다.

---

## 일반적인 플래그 패턴 🔄

### 빠른 분석
```bash
/sc:analyze src/ --focus quality          # 빠른 품질 확인
/sc:analyze --uc --focus security         # 빠른 보안 스캔
```

### 심층 조사  
```bash
/sc:troubleshoot "버그" --think --seq      # 체계적 디버깅
/sc:analyze --think-hard --focus architecture  # 아키텍처 분석
```

### 대규모 프로젝트 작업
```bash
/sc:analyze monorepo/ --delegate auto --uc     # 효율적인 대규모 분석
/sc:improve legacy/ --wave-mode auto --safe-mode  # 안전한 체계적 개선
```

### 학습 및 문서화
```bash
/sc:explain React hooks --c7 --verbose    # 문서와 함께 상세 설명
/sc:document api/ --persona-scribe        # 전문적인 문서화
```

### 성능 중심
```bash
/sc:analyze --focus performance --play     # 테스팅과 함께 성능 분석
/sc:build --uc --no-mcp                   # 추가 기능 없이 빠른 빌드
```

### 보안 중심
```bash
/sc:analyze --focus security --think --validate  # 철저한 보안 분석
/sc:scan --persona-security --safe-mode         # 보수적인 보안 스캔
```

## 실용적인 예시 💡

### 전후 비교: 기본 분석
**이전** (기본):
```bash
/sc:analyze auth.js
# → 간단한 파일 분석
```

**이후** (플래그 사용):
```bash
/sc:analyze auth.js --focus security --think --c7
# → 심층 사고와 공식 문서를 사용한 보안 중심 분석
# → 훨씬 더 철저하고, 보안 패턴 찾고, 모범 사례와 대조
```

### 전후 비교: 대규모 프로젝트
**이전** (느림):
```bash
/sc:analyze huge-monorepo/
# → 모든 것을 한 번에 분석하려고 시도, 타임아웃 또는 너무 많은 토큰 사용 가능
```

**이후** (효율적):
```bash
/sc:analyze huge-monorepo/ --delegate auto --uc --focus architecture
# → 하위 에이전트에 작업 위임, 출력 압축, 아키텍처에 집중
# → 더 빠르고, 더 집중적이고, 더 나은 결과
```

### 전후 비교: 개선 작업
**이전** (위험함):
```bash
/sc:improve legacy-system/
# → 너무 많은 변경을 할 수 있고, 깨뜨릴 수 있음
```

**이후** (안전함):
```bash
/sc:improve legacy-system/ --safe-mode --loop --validate --preview
# → 안전한 변경만, 반복적 접근, 먼저 검증, 미리보기 표시
# → 훨씬 더 안전하고, 점진적 개선
```

## 자동 활성화 예시 🤖

SuperClaude는 보통 컨텍스트를 기반으로 플래그를 추가합니다. 언제 시도하는지 알아보세요:

### 복잡도 기반
```bash
/sc:analyze huge-codebase/
# 자동 추가: --delegate auto --uc
# 이유: 50개 이상 파일 감지, 컨텍스트 관리 필요

/sc:troubleshoot "복잡한 시스템 문제"  
# 자동 추가: --think --seq
# 이유: 다중 컴포넌트 문제 감지
```

### 도메인 기반
```bash
/sc:build react-app/
# 자동 추가: --c7 --persona-frontend
# 이유: 프론트엔드 프레임워크 감지

/sc:analyze --focus security
# 자동 추가: --persona-security --validate
# 이유: 보안 초점이 보안 전문가 트리거
```

### 성능 기반
```bash
# 컨텍스트 사용량 >75%일 때
/sc:analyze large-project/
# 자동 추가: --uc
# 이유: 토큰 최적화 필요

# 위험 점수 >0.7일 때
/sc:improve production-code/
# 자동 추가: --safe-mode --validate
# 이유: 고위험 작업 감지
```

## 고급 사용법 🚀

### 복잡한 플래그 조합

**포괄적인 코드 리뷰**:
```bash
/sc:review codebase/ --persona-qa --think-hard --focus quality --validate --c7
# → QA 전문가 + 심층 사고 + 품질 초점 + 검증 + 문서
```

**레거시 시스템 현대화**:
```bash
/sc:improve legacy/ --wave-mode force --persona-architect --safe-mode --loop --c7
# → 웨이브 오케스트레이션 + 아키텍트 관점 + 안전성 + 반복 + 문서
```

**보안 감사**:
```bash
/sc:scan --persona-security --ultrathink --focus security --validate --seq
# → 보안 전문가 + 최대 사고 + 보안 초점 + 검증 + 체계적 분석
```

### 성능 최적화

**속도를 위해**:
```bash
/sc:analyze --no-mcp --uc --scope file
# → 추가 기능 비활성화, 출력 압축, 범위 제한
```

**철저함을 위해**:
```bash
/sc:analyze --all-mcp --think-hard --delegate auto
# → 모든 기능, 심층 사고, 병렬 처리
```

### 사용자 정의 워크플로우

**버그 조사 워크플로우**:
```bash
/sc:troubleshoot "특정 오류" --seq --think --validate
/sc:analyze affected-files/ --focus quality --persona-analyzer  
/sc:test --play --coverage
```

**기능 개발 워크플로우**:
```bash
/sc:design new-feature --persona-architect --c7
/sc:build --magic --persona-frontend --validate
/sc:test --play --coverage
/sc:document --persona-scribe --c7
```

## 빠른 참조 📋

### 가장 유용한 플래그
| 플래그 | 용도 | 언제 사용 |
|------|---------|-------------|
| `--think` | 더 깊은 분석 | 복잡한 문제 |
| `--uc` | 출력 압축 | 대규모 작업 |
| `--safe-mode` | 보수적 실행 | 중요한 코드 |
| `--c7` | 공식 문서 | 프레임워크 작업 |
| `--seq` | 체계적 분석 | 디버깅 |
| `--focus security` | 보안 초점 | 보안 우려사항 |
| `--delegate auto` | 병렬 처리 | 대규모 코드베이스 |
| `--validate` | 행동 전 확인 | 위험한 작업 |

### 잘 작동하는 플래그 조합
```bash
# 안전한 개선
--safe-mode --validate --preview

# 심층 분석  
--think --seq --c7

# 대규모 프로젝트
--delegate auto --uc --focus

# 학습
--verbose --c7 --persona-mentor

# 보안 작업
--persona-security --focus security --validate

# 성능 작업
--persona-performance --focus performance --play
```

### 자동 활성화 트리거
- **--think**: 복잡한 import, 모듈 간 호출
- **--uc**: 컨텍스트 >75%, 대규모 작업  
- **--safe-mode**: 리소스 사용량 >85%, 프로덕션
- **--delegate**: 7개 이상 디렉토리 또는 50개 이상 파일
- **--c7**: 프레임워크 import, 문서 요청
- **--seq**: 디버깅 키워드, --think 플래그
- **페르소나**: 도메인별 키워드와 패턴

## 플래그 문제 해결 🚨

### 일반적인 문제

**"플래그가 작동하지 않는 것 같음"**
- 철자 확인 (일반적인 오타: `--ultracompresed`, `--persona-fronted`)
- 일부 플래그는 값이 필요: `--scope project`, `--focus security`
- 플래그 충돌: `--no-mcp`가 `--c7`, `--seq` 등을 무시

**"작업이 너무 느림"**
- 압축을 위해 `--uc` 시도
- 추가 기능을 비활성화하려면 `--no-mcp` 사용
- 범위 제한: `--scope project` 대신 `--scope file`

**"출력이 너무 많음"**
- 압축을 위해 `--uc` 추가
- `--verbose`가 있으면 제거
- 간단한 질문에는 `--answer-only` 사용

**"충분히 철저하지 않음"**
- `--think` 또는 `--think-hard` 추가
- 관련 MCP 서버 활성화: `--seq`, `--c7`
- 적절한 페르소나 사용: `--persona-analyzer`

**"변경이 너무 위험함"**
- 중요한 코드에는 항상 `--safe-mode` 사용
- 먼저 확인하려면 `--validate` 추가
- 적용하기 전에 변경사항을 보려면 `--preview` 사용

### 플래그 충돌

**다른 것들을 무시하는 것들**:
- `--no-mcp`는 모든 MCP 플래그를 무시 (`--c7`, `--seq` 등)
- `--safe-mode`는 최적화 플래그를 무시
- 마지막 페르소나 플래그가 승리: `--persona-frontend --persona-backend` → backend

**우선순위 순서**:
1. 안전 플래그 (`--safe-mode`)가 최적화를 이김
2. 명시적 플래그가 자동 활성화를 이김
3. 사고 깊이: `--ultrathink` > `--think-hard` > `--think`
4. 범위: system > project > module > file

## 효과적인 플래그 사용 팁 💡

### 시작하기 (솔직한 진실)
1. **처음에는 플래그를 무시하세요** - 자동 활성화가 대부분의 경우를 꽤 잘 처리합니다
2. **무엇이 자동 활성화되는지 보세요** - SuperClaude가 무엇을 선택하는지 보면서 배울 수 있습니다
3. **궁금할 때 `--help` 사용** - 많은 명령어가 사용 가능한 플래그를 보여줍니다
4. **자동화를 신뢰하세요** - SuperClaude는 보통 합리적인 기본값을 선택합니다

### 고급 되기 (원한다면)
1. **재정의 실험** - 보안이 아닌 코드에 `--persona-security`를 시도해서 다른 관점 보기
2. **유용한 조합 배우기** - 중요한 것에는 `--safe-mode --validate`
3. **성능 트레이드오프 이해** - 빠름 (`--uc --no-mcp`) vs 철저함 (`--think-hard --all-mcp`)
4. **학습을 위해 플래그 사용** - 무슨 일이 일어났는지 이해하고 싶을 때 `--verbose`

### 성능 팁 (고급 사용자용)
- **속도를 위해**: `--uc --no-mcp --scope file`
- **철저함을 위해**: `--think-hard --all-mcp --delegate auto`
- **안전을 위해**: `--safe-mode --validate --preview`
- **학습을 위해**: `--verbose --c7 --persona-mentor`

---

## 최종 참고사항 📝

**플래그에 대한 진실** 💯:
- **자동 활성화는 보통** 수동 플래그 선택에 비해 꽤 잘 작동합니다
- **이 가이드의 대부분을 무시할 수 있고** 그냥 기본 명령어를 사용할 수 있습니다
- **플래그는 필요해서가 아니라** 원할 때 여기 있습니다
- **학습은 자연스럽게** 사용을 통해 일어나고, 가이드 공부를 통해서가 아닙니다 😊

**압도당하지 마세요** 🧘‍♂️:
- SuperClaude는 플래그 지식 없이도 잘 작동하려고 시도합니다
- 위의 자세한 정보는 호기심을 위한 것이지 필수가 아닙니다
- 자동 활성화는 사용 패턴을 바탕으로 계속 똑똑해지고 있습니다
- 플래그를 외우지 않아서 놓치고 있는 것은 없습니다

**실제로 플래그가 필요한 때**:
- 자동 활성화 무시 (드물게)
- 다른 접근법 실험 (재미있게)
- 특정 성능 필요에 최적화 (고급)
- 무슨 일이 일어났는지 학습 (교육적)

**간단하게 시작하고, 간단하게 유지** 🎯:
- 기본 명령어 사용: `/analyze`, `/build`, `/improve`
- 자동 활성화가 복잡성을 처리하도록 두기
- 실험하고 싶을 때만 수동 플래그 추가
- SuperClaude가 무엇을 하고 있는지 신뢰

---

*기억하세요: 이 모든 겉보기 복잡성 뒤에서, SuperClaude는 실제로 사용하기 간단합니다. 그냥 명령어 입력을 시작하세요! 🚀* 