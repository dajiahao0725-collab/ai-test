# AI 광고 대행사 (Ad Agency)

Cursor 서브에이전트 7명 + 스킬 1개로 캠페인 기획서 묶음을 자동 생성하는 모듈입니다.

## 빠른 시작

Cursor 채팅창에 아래 중 하나를 입력하세요.

```
/adagency
```

또는

```
광고 캠페인 만들어줘
```

브랜드·목표·타겟을 알려주면 AE → 카피 → 제작팀(4개 동시) → 대표 검수 → 캠페인 바이블까지 자동 실행됩니다.

## 폴더 구조

```
.cursor/
├── agents/          # AI 팀원 8명 (ad-* 7 + report-writer)
└── skills/          # ad-agency, report-writer 진행 대본
ad_campaign/         # 캠페인 산출물 01~09
reports/             # report-writer 보고서 산출물
```

## 산출물

| 파일 | 만드는 팀원 |
|------|------------|
| `01_ae_brief.md` | AE |
| `02_copy.md` | 카피라이터 |
| `03_image_ad.md` | 이미지팀 |
| `04_video_ad.md` | 영상팀 |
| `05_outdoor_ad.md` | 옥외팀 |
| `06_creative_ad.md` | 혁신팀 |
| `07_review.md` | 대표 (검수) |
| `08_campaign_bible.md` | 통합 바이블 |
| `09_prompt_pack.md` | 재사용 프롬프트 모음 |

## 샘플 캠페인

본 레포에는 **Outdoor Robot × 사우디아라비아** 캠페인 결과물이 포함되어 있습니다.  
`ad_campaign/08_campaign_bible.md`에서 전체를 한눈에 볼 수 있습니다.

## 주의사항

- AI 크리에이티브는 **초안**입니다. 최종 검수는 사람이 해주세요.
- `.cursor/mcp.json` 등 **API 키가 담긴 파일은 GitHub에 올리지 마세요.**

## 복원 방법 (노트북 반납 후)

1. Cursor 설치
2. `Clone Repository` → 이 레포 주소 입력
3. `/adagency`로 바로 재사용

끝.
