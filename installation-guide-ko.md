# SuperClaude 설치 가이드 📦

## 🎯 보이는 것보다 쉽습니다!

**솔직한 이야기**: 모든 세부사항을 다루고 싶어서 이 가이드가 길어 보이지만, 실제로는 설치가 꽤 간단합니다. 대부분의 사람들은 한 명령어로 2분 안에 끝낍니다!

### 1단계: 패키지 설치

**옵션 A: PyPI에서 설치 (권장)**
```bash
uv add SuperClaude
```

**옵션 B: 소스에서 설치**
```bash
git clone https://github.com/NomenAK/SuperClaude.git
cd SuperClaude
uv sync
```
### 🔧 UV / UVX 설정 가이드

SuperClaude v3는 [`uv`](https://github.com/astral-sh/uv) (더 빠르고 현대적인 Python 패키지 관리자) 또는 크로스 플랫폼 사용을 위한 `uvx`를 통한 설치도 지원합니다.

### 🌀 `uv`로 설치

`uv`가 설치되어 있는지 확인하세요:

```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

> 또는 다음 지침을 따르세요: [https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)

`uv`를 사용할 수 있게 되면, SuperClaude를 이렇게 설치할 수 있습니다:

```bash
uv venv
source .venv/bin/activate
uv pip install SuperClaude
```

### ⚡ `uvx`로 설치 (크로스 플랫폼 CLI)

`uvx`를 사용한다면, 그냥 실행하세요:

```bash
uvx pip install SuperClaude
```
## 🔧 UV / UVX 설정 가이드

SuperClaude v3는 [`uv`](https://github.com/astral-sh/uv) (더 빠르고 현대적인 Python 패키지 관리자) 또는 크로스 플랫폼 사용을 위한 `uvx`를 통한 설치도 지원합니다.

### 🌀 `uv`로 설치

`uv`가 설치되어 있는지 확인하세요:

```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

> 또는 다음 지침을 따르세요: [https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)

`uv`를 사용할 수 있게 되면, SuperClaude를 이렇게 설치할 수 있습니다:

```bash
uv venv
source .venv/bin/activate
uv pip install SuperClaude
```

### ⚡ `uvx`로 설치 (크로스 플랫폼 CLI)

`uvx`를 사용한다면, 그냥 실행하세요:

```bash
uvx pip install SuperClaude
```

### ✅ 설치 완료

설치 후, 일반적인 설치 프로그램 단계를 계속하세요:

```bash
python3 -m SuperClaude install
```

또는 bash 스타일 CLI 사용:

```bash
SuperClaude install
```

### 🧠 참고사항:

* `uv`는 더 나은 캐싱과 성능을 제공합니다.
* Python 3.8+와 호환되며 SuperClaude와 원활하게 작동합니다.

---

### ⚠️ 중요한 참고사항 
**SuperClaude를 설치한 후**
**`SuperClaude commands`, `python3 -m SuperClaude commands` 또는 `python3 SuperClaude commands`를 사용할 수 있습니다**

**무슨 일이 일어났을까요?** SuperClaude가 필요한 모든 것을 설정하려고 시도했습니다. 보통 복잡한 구성, 의존성 찾기, 설정 골치 아픈 일이 없습니다! 🎉

---

SuperClaude v3 설치에 대한 종합 가이드입니다. 하지만 기억하세요 - 대부분의 사람들은 위의 빠른 시작 이후로는 읽을 필요가 없습니다! 😊

## 시작하기 전에 🔍

### 필요한 것 💻

SuperClaude는 **Windows**, **macOS**, **Linux**에서 작동합니다. 다음이 필요합니다:

**필수:**
- **Python 3.8 이상** - 프레임워크가 Python으로 작성됨
- **Claude CLI** - SuperClaude가 Claude Code를 향상시키므로 먼저 설치해야 함

**선택사항 (하지만 권장):**
- **Node.js 16+** - MCP 서버 통합을 원하는 경우에만 필요
- **Git** - 개발 워크플로우에 도움

### 빠른 확인 🔍

설치하기 전에 기본사항이 있는지 확인해보겠습니다:

```bash
# Python 버전 확인 (3.8+ 이어야 함)
python3 --version

# Claude CLI가 설치되어 있는지 확인
claude --version

# Node.js 확인 (선택사항, MCP 서버용)
node --version
```

이 중 하나라도 실패하면 아래 [전제조건 설정](#전제조건-설정-🛠️) 섹션을 참조하세요.

## 빠른 시작 🚀

**🏆 "그냥 작동하게 하기" 접근법 (90% 사용자에게 권장)**
**옵션 A: PyPI에서 설치 (권장)**
```bash
pip install SuperClaude

# 권장 설정으로 설치  
SuperClaude install --quick

# 끝! 🎉
```
**옵션 B: 소스에서 설치**
```bash
# 저장소 복제
git clone <repository-url>
cd SuperClaude
pip install .

# 권장 설정으로 설치  
SuperClaude install --quick

# 끝! 🎉
```
**⚠️ 중요한 참고사항**
**SuperClaude를 설치한 후**
**`SuperClaude commands`, `python3 -m SuperClaude commands` 또는 `python3 SuperClaude commands`를 사용할 수 있습니다**

**얻은 것:**
- ✅ 전문가를 자동 활성화하는 16개의 스마트 명령어
- ✅ 언제 도움을 줄지 아는 11개의 전문가 페르소나
- ✅ 복잡성을 알아서 파악하는 지능적 라우팅
- ✅ 약 2분의 시간과 ~50MB 디스크 공간

**정말로, 끝났습니다.** Claude Code를 열고 `/help`를 입력한 다음 SuperClaude의 마법을 확인하세요.

**무엇을 할지 궁금하신가요?** 먼저 확인해보세요:
```bash
SuperClaude install --quick --dry-run
```

## 설치 옵션 🎯

선택할 수 있는 세 가지 설치 프로필이 있습니다:

### 🎯 최소 설치
```bash
SuperClaude install --minimal
```
- **내용**: 핵심 프레임워크 파일만
- **시간**: ~1분
- **공간**: ~20MB  
- **적합한 경우**: 테스팅, 기본 향상, 최소 설정
- **포함**: Claude를 안내하는 핵심 동작 문서

### 🚀 빠른 설치 (권장)
```bash
SuperClaude install --quick
```
- **내용**: 핵심 프레임워크 + 16개 슬래시 명령어
- **시간**: ~2분
- **공간**: ~50MB
- **적합한 경우**: 대부분의 사용자, 일반 개발
- **포함**: 최소 설치의 모든 것 + `/analyze`, `/build`, `/improve` 같은 전문 명령어

### 🔧 개발자 설치  
```bash
SuperClaude install --profile developer
```
- **내용**: MCP 서버 통합을 포함한 모든 것
- **시간**: ~5분
- **공간**: ~100MB
- **적합한 경우**: 고급 사용자, 기여자, 고급 워크플로우
- **포함**: 모든 것 + Context7, Sequential, Magic, Playwright 서버

### 🎛️ 대화형 설치
```bash
SuperClaude install
```
- 컴포넌트를 선택할 수 있음
- 각 컴포넌트가 무엇을 하는지 자세한 설명 표시
- 설치되는 것에 대한 제어를 원할 때 좋음

## 단계별 설치 📋

### 전제조건 설정 🛠️

**Python이 없나요?**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install python3 python3-pip

# macOS  
brew install python3

# Windows
# https://python.org/downloads/에서 다운로드
# 또는 명령 프롬프트나 powershell을 열어서
winget install python
```

**Claude CLI가 없나요?**
- 설치 지침은 https://claude.ai/code를 방문하세요
- SuperClaude가 Claude Code를 향상시키므로 먼저 필요합니다

**Node.js가 없나요? (선택사항)**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install nodejs npm

# macOS
brew install node

# Windows  
# https://nodejs.org/에서 다운로드
# 또는 명령 프롬프트나 powershell을 열어서
winget install nodejs
```

### SuperClaude 받기 📥

**옵션 1: PyPI에서 설치 (권장)**
```bash
pip install SuperClaude
```

**옵션 2: 최신 릴리스 다운로드**
```bash
# 최신 릴리즈 다운로드 및 압축 해제
# (URL을 실제 릴리즈 URL로 교체)
curl -L <release-url> -o superclaude-v3.zip
unzip superclaude-v3.zip
cd superclaude-v3
pip install .
```

**옵션 3: Git에서 복제**
```bash
git clone <repository-url>
cd SuperClaude
pip install .
```

### 설치 프로그램 실행 🎬

설치 프로그램은 꽤 똑똑하고 과정을 안내해줍니다:

```bash
# 사용 가능한 모든 옵션 보기
SuperClaude install --help

# 빠른 설치 (권장)
SuperClaude install --quick

# 먼저 무슨 일이 일어날지 보고 싶으신가요?
SuperClaude install --quick --dry-run

# 모든 것 설치
SuperClaude install --profile developer

# 조용한 설치 (최소 출력)
SuperClaude install --quick --quiet

# 강제 설치 (확인 건너뛰기)
python3 SuperClaude.py install --quick --force
```

### 설치 중 📱

설치할 때 일어나는 일:

1. **시스템 확인** - 필요한 의존성이 있는지 확인
2. **디렉토리 설정** - `~/.claude/` 디렉토리 구조 생성
3. **핵심 파일** - 프레임워크 문서 파일 복사
4. **명령어** - 슬래시 명령어 정의 설치 (선택한 경우)
5. **MCP 서버** - MCP 서버 다운로드 및 구성 (선택한 경우)
6. **구성** - 기본 설정으로 `settings.json` 설정
7. **검증** - 모든 것이 작동하는지 테스트

설치 프로그램이 진행 상황을 표시하고 문제가 생기면 알려줍니다.

## 설치 후 ✅

### 빠른 테스트 🧪

모든 것이 작동했는지 확인해보겠습니다:

```bash
# 파일이 설치되었는지 확인
ls ~/.claude/

# 표시되어야 할 것: CLAUDE.md, COMMANDS.md, settings.json 등
```

**Claude Code로 테스트:**
1. Claude Code 열기
2. `/help` 입력해보기 - SuperClaude 명령어가 보여야 함
3. `/analyze --help` 시도 - 명령어 옵션이 표시되어야 함

### 설치된 것 📂

SuperClaude는 기본적으로 `~/.claude/`에 설치됩니다. 다음을 찾을 수 있습니다:

```
~/.claude/
├── CLAUDE.md              # 메인 프레임워크 진입점
├── COMMANDS.md             # 사용 가능한 슬래시 명령어  
├── FLAGS.md                # 명령어 플래그와 옵션
├── PERSONAS.md             # 스마트 페르소나 시스템
├── PRINCIPLES.md           # 개발 원칙
├── RULES.md                # 운영 규칙
├── MCP.md                  # MCP 서버 통합
├── MODES.md                # 운영 모드
├── ORCHESTRATOR.md         # 지능적 라우팅
├── settings.json           # 구성 파일
└── commands/               # 개별 명령어 정의
    ├── analyze.md
    ├── build.md
    ├── improve.md
    └── ... (13개 더)
```

**각 파일의 역할:**
- **CLAUDE.md** - Claude Code에게 SuperClaude에 대해 알리고 다른 파일들을 로드
- **settings.json** - 구성 (MCP 서버, 훅 등)
- **commands/** - 각 슬래시 명령어의 상세 정의

### 첫 단계 🎯

시작하려면 다음 명령어를 시도해보세요:

```bash
# Claude Code에서 이것들을 시도해보세요:
/sc:help                    # 사용 가능한 명령어 보기
/sc:analyze README.md       # 파일 분석
/sc:build --help           # 빌드 옵션 보기
/sc:improve --help         # 개선 옵션 보기
```

**압도당하는 것 같아도 걱정하지 마세요** - SuperClaude는 Claude Code를 점진적으로 향상시킵니다. 원하는 만큼 사용할 수 있습니다.

## 설치 관리 🛠️

### 업데이트 📅

SuperClaude를 최신 상태로 유지하세요:

```bash
# 업데이트 확인
SuperClaude update

# 강제 업데이트 (로컬 변경사항 덮어쓰기)
SuperClaude update --force

# 특정 컴포넌트만 업데이트
SuperClaude update --components core,commands

# 업데이트될 내용 보기
SuperClaude update --dry-run
```

**언제 업데이트해야 하나요:**
- 새 SuperClaude 버전이 릴리스될 때
- 문제가 있는 경우 (업데이트에 수정사항이 포함되는 경우가 많음)
- 새 MCP 서버를 사용할 수 있을 때

### 백업 💾

주요 변경 전에 백업을 생성하세요:

```bash
# 백업 생성
SuperClaude backup --create

# 기존 백업 목록  
SuperClaude backup --list

# 백업에서 복원
SuperClaude backup --restore

# 사용자 정의 이름으로 백업 생성
SuperClaude backup --create --name "before-update"
```

**언제 백업해야 하나요:**
- SuperClaude 업데이트 전
- 설정 실험 전
- 제거 전
- 많이 사용자 정의했다면 주기적으로

### 제거 🗑️

SuperClaude를 제거해야 하는 경우:

```bash
# SuperClaude 제거 (백업은 유지)
SuperClaude uninstall

# 완전 제거 (모든 것 제거)
SuperClaude uninstall --complete

# 제거될 내용 보기
SuperClaude uninstall --dry-run
```

**제거되는 것:**
- `~/.claude/`의 모든 파일 
- MCP 서버 구성
- Claude Code의 SuperClaude 설정

**남아있는 것:**
- 백업 (`--complete`를 사용하지 않는 한)
- Claude Code 자체 (SuperClaude는 건드리지 않음)
- 프로젝트와 다른 파일들

## 문제 해결 🔧

### 일반적인 문제 🚨

**"Python을 찾을 수 없음"**
```bash
# python3 대신 python 시도
python --version

# 또는 설치되어 있지만 PATH에 없는지 확인
which python3
```

**"Claude CLI를 찾을 수 없음"**
- 먼저 Claude Code가 설치되어 있는지 확인
- `claude --version`으로 확인해보기
- 설치 도움은 https://claude.ai/code 방문

**"권한 거부됨"**
```bash
# 명시적인 Python 경로로 시도
/usr/bin/python3 SuperClaude.py install --quick

# 또는 다른 권한이 필요한지 확인
ls -la ~/.claude/
```

**"MCP 서버가 설치되지 않음"**
- Node.js가 설치되어 있는지 확인: `node --version`
- npm을 사용할 수 있는지 확인: `npm --version`  
- 먼저 MCP 없이 설치 시도: `--minimal` 또는 `--quick`

**"설치가 중간에 실패함"**
```bash
# 무슨 일이 일어나는지 보려면 자세한 출력 사용
SuperClaude install --quick --verbose

# 또는 먼저 dry run 시도
SuperClaude install --quick --dry-run
```

### 플랫폼별 문제 🖥️

**Windows:**
- "명령을 찾을 수 없음"이 나오면 `python3` 대신 `python` 사용
- 권한 오류가 나오면 관리자로 명령 프롬프트 실행
- Python이 PATH에 있는지 확인

**macOS:**  
- 보안 및 개인정보 보호 설정에서 SuperClaude를 승인해야 할 수 있음
- Python 3.8+이 없으면 `brew install python3` 사용
- `python` 대신 `python3`를 명시적으로 사용해보기

**Linux:**
- `python3-pip`이 설치되어 있는지 확인
- 일부 패키지 설치에 `sudo`가 필요할 수 있음
- `~/.local/bin`이 PATH에 있는지 확인

### 여전히 문제가 있으신가요? 🤔

**문제 해결 리소스 확인:**
- GitHub Issues: https://github.com/NomenAK/SuperClaude/issues
- 여러분과 비슷한 기존 이슈 찾기
- 해결책을 찾을 수 없으면 새 이슈 생성

**버그를 신고할 때 다음을 포함해주세요:**
- 운영 체제와 버전
- Python 버전 (`python3 --version`)
- Claude CLI 버전 (`claude --version`)
- 실행한 정확한 명령어
- 완전한 오류 메시지
- 예상했던 동작

**도움 받기:**
- 일반적인 질문은 GitHub Discussions
- 최신 업데이트는 README.md 확인
- 알려진 문제인지 ROADMAP.md 확인

## 고급 옵션 ⚙️

### 사용자 정의 설치 디렉토리

```bash
# 사용자 정의 위치에 설치
SuperClaude install --quick --install-dir /custom/path

# 환경 변수 사용
export SUPERCLAUDE_DIR=/custom/path
SuperClaude install --quick
```

### 컴포넌트 선택

```bash
# 사용 가능한 컴포넌트 보기
SuperClaude install --list-components

# 특정 컴포넌트만 설치
SuperClaude install --components core,commands

# 특정 컴포넌트 건너뛰기
SuperClaude install --quick --skip mcp
```

### 개발 설정

SuperClaude에 기여하거나 수정할 계획이라면:

```bash
# 모든 컴포넌트가 포함된 개발자 설치
SuperClaude install --profile developer

# 개발 모드로 설치 (복사 대신 심볼릭 링크)
SuperClaude install --profile developer --dev-mode

# 개발용 git 훅과 함께 설치
SuperClaude install --profile developer --dev-hooks
```

## 다음은? 🚀

**이제 SuperClaude가 설치되었으니 (쉬웠죠?):**

1. **그냥 사용하기 시작하세요** - `/analyze some-file.js`나 `/build`를 시도해보고 무슨 일이 일어나는지 보세요 ✨
2. **학습에 대해 스트레스받지 마세요** - SuperClaude는 보통 필요한 것을 알아냅니다
3. **자유롭게 실험하세요** - `/improve`와 `/troubleshoot` 같은 명령어는 꽤 관대합니다
4. **궁금하면 가이드 읽기** - 무슨 일이 일어났는지 이해하고 싶을 때 `Docs/` 확인
5. **피드백 주기** - 무엇이 작동하고 무엇이 작동하지 않는지 알려주세요

**진짜 비밀**: SuperClaude는 새로운 것을 많이 배우지 않고도 기존 워크플로우를 향상시키도록 설계되었습니다. 일반 Claude Code처럼 사용하되, 얼마나 똑똑해지는지 확인해보세요! 🎯

**여전히 확신이 서지 않으신가요?** `/help`와 `/analyze README.md`부터 시작하세요 - 실제로 얼마나 위협적이지 않은지 보실 수 있습니다.

---

## 최종 참고사항 📝

- **설치는 1-5분** 선택한 것에 따라
- **필요한 디스크 공간: 20-100MB** (많지 않아요!)
- **기존 도구와 함께 작동** - 설정을 방해하지 않음
- **마음이 바뀌면 쉽게 제거** 가능
- **커뮤니티 지원** - 실제로 이슈를 읽고 응답합니다
- ### ⚠️ 중요한 참고사항 
**SuperClaude를 설치한 후**
**`SuperClaude commands`, `python3 -m SuperClaude commands` 또는 `python3 SuperClaude commands`를 사용할 수 있습니다**

SuperClaude를 시도해주셔서 감사합니다! 개발 워크플로우가 조금 더 원활해지기를 바랍니다. 🙂

---

*최종 업데이트: 2024년 7월 - 이 가이드에서 잘못되거나 혼란스러운 부분이 있으면 알려주세요!*