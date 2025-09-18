# 샘플 화면 구현 작업 체크리스트

아래 체크리스트를 모두 완료한 후에만 코드를 작성한다. (현재 단계: 계획 수립)

## 공통
- [ ] 업로드된 레퍼런스 이미지와 동일한 레이아웃/구성으로 구현 범위 확정
- [ ] Shadcn UI 컴포넌트 매핑표 작성 (각 영역 → 사용할 컴포넌트)
- [ ] 반응형(>=1024, <1024) 배치 규칙 정의
- [ ] 다크모드 대응 여부 결정 및 스타일 토큰 정의
- [ ] 접근성(A11y) 기준: label, aria-* 속성, 키보드 탐색성 체크 항목 정의

## 데이터 설계 (apps/web/app/template/examples/data.json)
- [ ] 카드/테이블/그래프에 필요한 모든 데이터 구조 정의
- [ ] 더미 데이터 작성 (총매출, 구독, 캘린더, 목표, 운동분 그래프, 결제내역 표, 팀원, 쿠키 설정, 이슈 신고, 공유 링크, 접근권한자 등)
- [ ] 키 네이밍 컨벤션 확정 (camelCase)

## 페이지 엔트리 (apps/web/app/template/examples/page.tsx)
- [ ] 데이터 로딩 로직 정의 (정적 import)
- [ ] 전체 그리드 레이아웃 설정 (shadcn Card/Grid 유틸ities 사용)
- [ ] 각 기능 카드를 컴포넌트로 분리하여 배치

## 컴포넌트 분리 (apps/web/app/template/examples/components)
- [ ] TotalRevenueCard
- [ ] SubscriptionsCard
- [ ] CalendarCard
- [ ] MoveGoalCard
- [ ] UpgradePlanCard (업그레이드 폼)
- [ ] CreateAccountCard (소셜/이메일 가입 폼)
- [ ] SupportChatCard (채팅 UI)
- [ ] ExerciseMinutesCard (라인 차트)
- [ ] PaymentsTableCard (테이블 + 페이징 + 선택)
- [ ] TeamMembersCard (역할 선택 드롭다운 포함)
- [ ] CookieSettingsCard (토글 스위치 2종)
- [ ] ReportIssueCard (폼: Area, Security Level, Subject, Description)
- [ ] ShareDocumentCard (링크 복사 + 접근 권한 리스트)

## UI 세부 사항
- [ ] shadcn/ui 문서의 컴포넌트만 사용하여 구성 (https://ui.shadcn.com)
- [ ] 버튼/인풋/셀렉트/스위치/아바타/배지/테이블/캘린더/차트(가능한 shadcn 예제 조합) 활용
- [ ] 숫자 포맷, 단위(달러, 칼로리/일) 표시 규칙 정의
- [ ] 차트는 예제 스타일과 유사한 톤으로 렌더링 (대체 라이브러리 사용 시 스타일 일치)
- [ ] 카드 헤더/설명/액션 버튼 텍스트 한글/영문 표기 규칙 결정

## 상호작용
- [ ] 폼 유효성 기본 처리(필수 필드, 이메일 형식)
- [ ] 테이블 행 선택, 페이징 버튼 동작 모의 처리
- [ ] "Copy Link" 버튼의 클립보드 복사 처리
- [ ] 스위치/셀렉트/라디오 등의 상태는 로컬 상태로만 유지

## 스타일/테마
- [ ] spacing, radius, border, shadow 등 공통 스타일 일치화
- [ ] 아이콘 사용 규칙(예: lucide-react) 정의

## 테스트/검수
- [ ] 주요 사용자 경로 수동 테스트 체크리스트 작성
- [ ] 스냅샷 캡처로 레퍼런스 이미지 대비 시각적 차이 검토
- [ ] 타입 오류/린트 오류 0건

## 산출물
- [ ] data.json 작성 완료
- [ ] components/* 컴포넌트 파일 생성 및 코드 작성 완료
- [ ] page.tsx에 컴포넌트 배치 완료
- [ ] README에 사용 방법 간단 추가(선택)
