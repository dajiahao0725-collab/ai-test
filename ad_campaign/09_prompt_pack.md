# Prompt Pack — AI 광고 대행사 & 보고서 작성

> GitHub 백업용 프롬프트 모음. Cursor 채팅창에 그대로 붙여넣어 재사용할 수 있습니다.

---

## 1. 광고 대행사 전체 실행 (스킬 트리거)

```
/adagency
```

또는

```
광고 캠페인 만들어줘
```

### 브리프 예시 (Outdoor Robot × 사우디 — 본 프로젝트 실제 실행)

```
브랜드: Outdoor Robot (실외로봇) × 사우디아라비아
목표: Vision 2030·NEOM 스마트시티 맥락에서 B2G·B2B 파트너십·PoC 유도
타겟: 사우디 공공·스마트시티 의사결정자·시설·물류·관광 운영 책임자 (35~55세)
전체 자동 실행해줘
```

---

## 2. 팀원 개별 호출 (에이전트 직접 지정)

| 팀원 | 호출 예시 |
|------|-----------|
| AE | `ad-ae 에이전트로 [브랜드] 캠페인 기획서 작성해줘. ad_campaign/01_ae_brief.md에 저장` |
| 카피 | `ad-copywriter로 01_ae_brief.md 읽고 02_copy.md 작성해줘` |
| 이미지팀 | `ad-image-team으로 01~02 참고해서 03_image_ad.md 작성해줘` |
| 영상팀 | `ad-video-team으로 04_video_ad.md 작성해줘` |
| 옥외팀 | `ad-outdoor-team으로 05_outdoor_ad.md 작성해줘` |
| 혁신팀 | `ad-creative-team으로 06_creative_ad.md 작성해줘` |
| 대표 | `ad-ceo-review로 01~06 검수하고 07_review.md에 채점해줘` |

### 제작팀 4개 동시 실행 (병렬)

```
ad-image-team, ad-video-team, ad-outdoor-team, ad-creative-team을 동시에 실행해줘.
입력: ad_campaign/01_ae_brief.md + 02_copy.md
출력: 03~06 각각 저장
```

---

## 3. 캠페인 바이블 통합

```
07_review.md 검수 결과가 50점 이상 통과야.
01~07 내용을 ad_campaign/08_campaign_bible.md로 통합해줘.
맨 앞에 캠페인 개요 요약, 맨 마지막 줄은 "끝."
```

---

## 4. 보고서 작성 (report-writer 스킬)

```
팀플 보고서 챕터 초안 작성해줘.

- 주제: [챕터 주제]
- 챕터: [예: 3장 시장 분석]
- 저장 경로: reports/[파일명].md
- 참고 자료: [URL 또는 파일 경로 나열]
```

---

## 5. 백업·정리 (부록2)

```
위키 부록2 지시처럼 백업할 것 한 폴더로 모아줘.
에이전트(.cursor/agents/), 스킬(.cursor/skills/), 캠페인 산출물(ad_campaign/) 확인.
```

---

## 6. 재작업 (검수 미통과 시)

```
07_review.md 재작업 지시에 따라 [팀명]만 다시 실행하고,
수정 후 ad-ceo-review로 재검수해줘.
```

---

## 파일 구조 (백업 체크리스트)

```
0602/
├── .cursor/
│   ├── agents/          ← 에이전트 8명 (ad-* 7 + report-writer)
│   └── skills/          ← ad-agency, report-writer
├── ad_campaign/
│   ├── 01_ae_brief.md
│   ├── 02_copy.md
│   ├── 03_image_ad.md
│   ├── 04_video_ad.md
│   ├── 05_outdoor_ad.md
│   ├── 06_creative_ad.md
│   ├── 07_review.md
│   ├── 08_campaign_bible.md
│   └── 09_prompt_pack.md   ← 이 파일
└── reports/             ← report-writer 산출물
```

⚠️ **GitHub에 올리면 안 되는 것:** `.cursor/mcp.json` 안의 API 키 (`GEMINI_API_KEY` 등)

끝.
