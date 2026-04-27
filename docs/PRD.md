# [앱 이름] PRD

> **이터레이션**: YYYY-MM-DD ~ YYYY-MM-DD
> **작성자**: 장수지, 박성훈
> **상태**: 초안 / 확정 / 진행 중 / 완료
> **Jira Project Key**:
> **Jira Epic**: (`/jira plan` 실행 후 자동 채움)
> **Figma**:
> **Repo**:

<details>
<summary>상단 메타 예시</summary>

> **이터레이션**: 2026-04-20 ~ 2026-04-26
> **작성자**: 장수지, 박성훈
> **상태**: 초안
> **Jira Project Key**: TIMECAPSULE
> **Jira Epic**: TIMECAPSULE-1
> **Figma**: https://figma.com/...
> **Repo**: https://github.com/ANDIZ-team/TimeCapsule

</details>

---

## 1. 한 줄 요약

누구를 위한, 무엇을 해주는 앱인지 한 문장.

<details>
<summary>예시 보기</summary>

충동구매가 잦은 사람이 사고 싶은 물건을 72시간 묵혀보게 해서 지갑을 지켜주는 앱.

</details>

---

## 2. Why / 타겟 유저

### 왜 만드는가
- 해결하려는 문제:
- 만들게 된 동기:

### 1차 타겟 유저
- 누구:
- 어떤 상황에서:
- 해결하려는 핵심 불편:

<details>
<summary>예시 보기</summary>

**왜 만드는가**
- 해결하려는 문제: 장바구니에 넣는 순간 뇌가 "이미 내 것" 모드 진입. 결제까지 이어짐.
- 만들게 된 동기: 일정 시간 강제로 기다리면 필요 없는 구매의 70%는 스스로 포기한다는 경험.

**1차 타겟 유저**
- 누구: 쇼핑앱 무한스크롤이 취미인 20~30대
- 어떤 상황에서: "이거 예쁘다" 하고 결제창 진입 직전
- 해결하려는 핵심 불편: 나중에 후회할 걸 알면서도 못 멈춤

</details>

---

## 3. MVP 핵심 기능

이번 이터레이션 안에 반드시 나와야 하는 기능. 3~5개.

- [ ] 기능 1 —
- [ ] 기능 2 —
- [ ] 기능 3 —

<details>
<summary>예시 보기</summary>

- [ ] 원탭 등록 — 상품 사진/URL/가격 입력해 쿨다운 시작
- [ ] 실시간 카운트다운 — 남은 시간, 진행도 바
- [ ] 종료 알림 — "아직도 갖고 싶어?" 푸시
- [ ] 누적 절약액 — 포기한 물건 가격 합계

</details>

---

## 4. 화면 & 유저 플로우

### 화면 목록

| # | 화면 이름 | 역할 (한 줄) |
|---|---|---|
| 1 |  |  |
| 2 |  |  |

### 주요 플로우

진입 → [화면 A] → [액션] → [화면 B] → 목표 달성

<details>
<summary>예시 보기</summary>

**화면 목록**

| # | 화면 이름 | 역할 |
|---|---|---|
| 1 | 홈 | 참는 중 리스트 + 등록 버튼 |
| 2 | 등록 시트 | 상품명/가격/사진/URL 입력 |
| 3 | 상세 | 카운트다운, 메모, 포기/구매 결정 |
| 4 | 절약 리포트 | 누적 절약액, 포기 히스토리 |
| 5 | 설정 | 기본 쿨다운 시간, 알림 설정 |

**주요 플로우**
- 등록 플로우: 홈 → + 버튼 → 등록 시트 → 저장 → 홈 리스트 상단에 추가
- 결정 플로우: 알림 탭 → 상세 → "포기" or "구매" → 절약 리포트 업데이트

</details>

---

## 5. 데이터 모델

### 엔티티 / 테이블

| 이름 | 필드 | 타입 | 비고 |
|---|---|---|---|
|  |  |  |  |

### 저장 위치
- 로컬 (UserDefaults / SwiftData / CoreData / Keychain):
- 서버 (Firebase / 자체 백엔드 / 외부 API):

<details>
<summary>예시 보기</summary>

**엔티티**

| 이름 | 필드 | 타입 | 비고 |
|---|---|---|---|
| WaitItem | id | UUID | PK |
| WaitItem | name | String | 상품명 |
| WaitItem | priceKRW | Int | 가격 |
| WaitItem | productURL | String? | 쇼핑 링크 |
| WaitItem | imageData | Data? | 로컬 저장 이미지 |
| WaitItem | registeredAt | Date | 등록 시각 |
| WaitItem | cooldownHours | Int | 기본 72 |
| WaitItem | decidedAt | Date? | 결정 시각 |
| WaitItem | decision | Enum | pending / gaveUp / bought |

**저장 위치**
- 로컬: SwiftData로 WaitItem 저장
- 서버: 없음 (오프라인 전용)

</details>

---

## 6. 외부 의존

### API
- 자체 백엔드:
- 외부 API:
- 키 발급 / 승인 상태:

### SDK & 라이브러리
- Firebase:
- 기타:

### 에셋
- 이미지 / 아이콘 출처 및 라이선스:
- 폰트 라이선스:

### 권한

이 앱이 요청할 iOS 권한과 거부 시 처리.

| 권한 | 언제 요청 | 거부 시 UX |
|---|---|---|
|  |  |  |

### Analytics 이벤트

Firebase Analytics에 발사할 이벤트 명세.

| 이벤트 이름 | 트리거 | 주요 속성 | 용도 |
|---|---|---|---|
|  |  |  |  |

<details>
<summary>예시 보기</summary>

**API**
- 자체 백엔드: 없음
- 외부 API: 없음 (URL 미리보기도 시스템 제공만 사용)

**SDK & 라이브러리**
- Firebase: Analytics, Crashlytics
- 기타: Lottie (절약액 축하 애니메이션)

**에셋**
- 아이콘: SF Symbols
- 폰트: Pretendard (OFL)

**권한**

| 권한 | 언제 요청 | 거부 시 UX |
|---|---|---|
| UserNotifications | 온보딩 종료 시 | 설정 유도 배너, 쿨다운은 앱 내 카운트다운만으로 진행 |
| Photos (선택) | 상품 사진 추가 시 | 시스템 파일 피커로 대체 |

**Analytics 이벤트**

| 이벤트 이름 | 트리거 | 주요 속성 | 용도 |
|---|---|---|---|
| item_registered | 참기 등록 완료 시 | price_krw, cooldown_hours | 등록 전환율 측정 |
| cooldown_finished | 72시간 경과 | item_age_hours | 앱 복귀율 측정 |
| decision_made | 포기/구매 버튼 탭 | decision, price_krw | 핵심 KPI (포기율) |

</details>

---

## 7. 기술 스택 & 아키텍처 결정

| 항목 | 결정 |
|---|---|
| iOS 최소 지원 버전 |  |
| UI 프레임워크 |  |
| 아키텍처 |  |
| 상태 관리 |  |
| 네트워크 |  |
| 의존성 관리 |  |
| 기타 주요 라이브러리 |  |

### 결정 근거 (중요한 것만)
-

<details>
<summary>예시 보기</summary>

| 항목 | 결정 |
|---|---|
| iOS 최소 지원 버전 | iOS 17 |
| UI 프레임워크 | SwiftUI |
| 아키텍처 | MVVM |
| 상태 관리 | @Observable |
| 네트워크 | 불필요 |
| 의존성 관리 | SPM |
| 기타 | Firebase, Lottie |

**결정 근거**
- iOS 17 하한: SwiftData 도입 목적. CoreData 병행 시 리포지토리 이중화 부담.
- 알림: UserNotifications만 사용 (서버 푸시 불필요).

</details>

---

## 8. 릴리즈 기준 (Definition of Done)

### 공통
- [ ] 핵심 플로우 크래시 없이 완주
- [ ] 지원 기기/OS에서 주요 화면 깨짐 없음
- [ ] 앱 아이콘, 스플래시, 메타데이터 세팅 완료
- [ ] Firebase Analytics / Crashlytics 연동 확인
- [ ] 다크모드 주요 화면 점검 완료
- [ ] 기본 접근성 점검 (VoiceOver 라벨, 다이나믹 타입 최소 3단계)
- [ ] App Store Connect 심사 제출

### 앱별 추가
- [ ]

<details>
<summary>예시 보기</summary>

**앱별 추가 DoD**
- [ ] 앱 강제 종료 상태에서도 쿨다운 종료 알림 정확히 도달
- [ ] 타이머 오차 60초 이내 (백그라운드 포함)
- [ ] 포기 → 누적 절약액 실시간 반영

</details>

---

## 9. 백로그 (이번 주 제외)

이번 이터레이션에 **넣지 않기로 결정한** 기능.

-

<details>
<summary>예시 보기</summary>

- 쇼핑앱 공유시트 확장 (Safari/쿠팡에서 바로 등록)
- 위젯 (현재 참는 중 개수/남은 시간)
- 월간 인사이트 (가장 자주 참은 카테고리)
- 친구와 참기 챌린지

</details>

---

## 10. 리스크 / 미해결 질문

| 구분 | 내용 | 담당 | 데드라인 |
|---|---|---|---|
|  |  |  |  |

> 구분: `결정 필요` / `기술 불확실` / `외부 의존`

<details>
<summary>예시 보기</summary>

| 구분 | 내용 | 담당 | 데드라인 |
|---|---|---|---|
| 결정 필요 | 기본 쿨다운 24/48/72 중 어느 것? | 장수지 | D+1 |
| 기술 불확실 | 백그라운드 알림 정확도 검증 | 박성훈 | D+2 |
| 결정 필요 | 이미지 저장 방식 (원본 Data vs 썸네일) | 장수지 | D+2 |

</details>

---

## 11. 시장 조사 & 레퍼런스

### 유사 / 경쟁 앱

| 앱 이름 | 링크 | 참고할 점 | 피할 점 |
|---|---|---|---|
|  |  |  |  |

### 디자인 레퍼런스
-

### 차용할 UX 패턴
- 온보딩 방식:
- 네비게이션 구조:

<details>
<summary>예시 보기</summary>

**유사 / 경쟁 앱**

| 앱 이름 | 링크 | 참고할 점 | 피할 점 |
|---|---|---|---|
| One Sec | [앱스토어] | 진입 전 숨 고르기 UX, 강제 대기 체감 | 과한 유료 전환 |
| Opal | [앱스토어] | 타이머 진행도 시각화 | 기능 과잉 |
| Delay Buy (크롬 확장) | [링크] | 컨셉 유사, 쿠팡/아마존 연동 | UX는 웹 한정 |

**디자인 레퍼런스**
- Mobbin "minimalist timer" 카테고리
- Dribbble "countdown app ios" 상위 10개

**차용할 UX 패턴**
- 온보딩: 2스텝 (컨셉 설명 → 기본 쿨다운 선택)
- 네비: 탭바 없음. 홈 단일 화면 + 시트 모달. 설정/리포트는 우상단 버튼.

</details>
