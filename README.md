# template-ios-app

Andiz 신규 iOS 앱을 시작하기 위한 템플릿 레포.

## 사용법

1. 우측 상단 **`Use this template`** 클릭
2. 새 레포 이름 입력 (앱 이름)
3. 클론 후 아래 ✅ 체크리스트 진행

---

## ✅ 새 앱 셋업 체크리스트

### 1. Tech Stack 결정

- [ ] UI 프레임워크 (SwiftUI / UIKit / 혼합)
- [ ] iOS Deployment Target (16+ / 17+ / 18+)
- [ ] Architecture (MV / MVVM / TCA / 기타)
- [ ] Data (UserDefaults / SwiftData / CoreData / 서버만)
- [ ] Dark Mode (지원 / 라이트 / 다크 전용)

📖 선정 기준: [노션 - 개발 컨벤션](URL)

### 2. 프로젝트 셋업

- [ ] Xcode 프로젝트 생성 (앱 이름 = 레포 이름)
- [ ] 번들 ID 설정 (`com.andiz.{앱이름}`)
- [ ] Build Configurations 확인 (Debug / Release)
- [ ] Firebase 프로젝트 생성 + 연동 (Analytics, Crashlytics)
- [ ] SwiftLint Build Phase 스크립트 추가
- [ ] 앱 아이콘 임시 적용
- [ ] `CLAUDE.md` 채우기 (앱 이름, 프로젝트 정보 블록)
- [ ] `docs/PRD.md` 작성 (월요일 기획 시간에 Claude와 함께)
- [ ] `/jira plan` 실행 (PRD 기반 Jira Epic/Story/Task 자동 생성)
- [ ] 이 README를 앱 소개로 교체 ⬇️

### 3. README 교체 템플릿

```markdown
# {앱 이름}

한 줄 소개

## Tech Stack
- UI: {SwiftUI / UIKit / 혼합}
- iOS Target: {16.0+ / 17.0+ / 18.0+}
- Architecture: {MV / MVVM / TCA}
- Data: {UserDefaults / SwiftData / CoreData / 서버만}
- Dark Mode: {지원 / 미지원}

## 선택 근거
- UI: {이유}
- iOS Target: {이유}
- Architecture: {이유}
- Data: {이유}

## 주요 기능
1.
2.
3.

## 관련 링크
- Jira: [KEY]
- Figma: [URL]
- Firebase: [URL]
```

---

## 자동 포함되는 것

### 그대로 두기 (수정 X)
- `CODEOWNERS` — 자동 리뷰어 지정
- `.gitignore` — Swift/Xcode/SPM/Fastlane 표준
- `.swiftlint.yml` — 공통 코드 스타일
- 조직 차원 PR 템플릿 (`.github` 메타 레포에서 자동)

### 복제 후 채워야 할 것
- `CLAUDE.md` — Claude용 프로젝트 정보 (`## 프로젝트 정보` 블록은 `/jira plan`이 자동 갱신)
- `docs/PRD.md` — 주간 이터레이션 PRD (Claude와 함께 작성)

---

## 공통 운영 스택

- **Firebase Analytics + Crashlytics** (모니터링/분석)
- **Swift Logger (OSLog)** (로깅, `print()` 대신)
- **DebugView** (개발자용 숨겨진 화면, 권장)

📖 상세 사용법: [노션 - 개발 컨벤션](URL)

---

## Git Flow

```
main    ← App Store 출시 코드
develop ← 개발 통합
feature/{이슈키}-{기능명}  ← 기능 개발
release/v{버전}           ← 출시 준비
hotfix/{이슈키}-{설명}     ← 긴급 수정
```

📖 상세: [노션 - Git 컨벤션](URL)
