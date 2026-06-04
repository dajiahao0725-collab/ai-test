# 이번 주 AI 핫 트렌드 분석

## 1. 챕터 핵심 주장

2026년 6월 2일(화)을 기준으로, AI 업계의 이번 주 핵심 화두는 **Microsoft Build 2026에서 Windows를 '에이전트 OS'로 재정의**한 것이며, 개발·배포·유통까지 아우르는 **에이전트 인프라 전쟁**이 본격화되고 있습니다.

## 2. 근거 자료 및 출처

| 번호 | 출처 | URL |
|------|------|-----|
| 1 | ChatForest, *Microsoft Build 2026 Recap* (2026-06-02) | https://chatforest.com/builders-log/microsoft-build-2026-recap-windows-agent-platform-project-polaris-copilot-workspace/ |
| 2 | byteiota, *Microsoft Build 2026: Windows Is Now an Agent Platform* | https://byteiota.com/microsoft-build-2026-windows-is-now-an-agent-platform/ |
| 3 | Windows News, *Build 2026: Microsoft Makes Windows an Agent Platform* | https://windowsnews.ai/article/build-2026-microsoft-makes-windows-an-agent-platform-for-ai-developers.420496 |
| 4 | Microsoft GitHub, *agent-framework* | https://github.com/microsoft/agent-framework |
| 5 | AnhTu.dev, *Microsoft Agent Framework 1.0* (2026-04-03) | https://anhtu.dev/microsoft-agent-framework-1-0-unified-sdk-for-ai-agents-on-dotnet-10-1096 |
| 6 | Mistral AI, *Vibe gets to work.* (2026-05-28) | https://mistral.ai/news/vibe-agent/ |
| 7 | Kore.ai, *Kore.ai Launches Artemis* (2026-05-21) | https://www.kore.ai/news/kore-ai-launches-artemis-the-new-generation-of-the-kore-ai-agent-platform-for-building-governing-and-optimizing-enterprise-ai |

## 3. 본문

### ① Build 2026: Windows = 에이전트 실행·배포·판매 플랫폼

6월 2~3일 샌프란시스코 Fort Mason에서 열린 Build 2026에서 Satya Nadella는 **Windows를 사람만 쓰는 OS가 아니라 에이전트도 일할 수 있는 런타임**으로 소개했습니다(출처 1). **Windows Agent Runtime** 프리뷰는 6월 Insider에게 제공되며, 초기에는 JSON·XML·PDF 같은 구조화 데이터를 다루는 텍스트 에이전트부터 지원합니다(출처 1, 3). 화면을 '보는' 비전 에이전트는 2027년 로드맵입니다(출처 3).

개발자는 **wagent CLI**로 에이전트 매니페스트를 패키징해 Windows 11·Server·Cloud PC에 동일하게 배포할 수 있습니다(출처 2). Git에 매니페스트를 두고 PR로 검토하는 방식은, AI 에이전트에도 **Dockerfile처럼 버전 관리**를 적용한다는 비유로 이해할 수 있습니다(출처 2).

**Windows Agent Store**는 에이전트 매니페스트를 판매하는 마켓플레이스로, 보안 심사와 85% 수익 배분을 제공합니다(출처 1). **Azure Agent Mesh**는 Windows·Cloud PC·엣지에 걸친 에이전트 연합 제어 평면입니다(출처 1). 즉 Build 2026은 "기능 추가"가 아니라 **에이전트 생태계 3종 세트(런타임·SDK·스토어)** 를 동시에 공개한 행사입니다.

### ② Agent Framework 1.0 + Project Polaris: 개발·모델 자립

**Microsoft Agent Framework 1.0**(4월 GA)은 AutoGen과 Semantic Kernel을 합친 통합 SDK로, .NET·Python에서 그래프 기반 멀티 에이전트 워크플로·MCP·A2A·OpenTelemetry를 지원합니다(출처 4, 5). NuGet 패키지 `Microsoft.Agents.AI`, GitHub 1만+ 스타(2026-05-28 기준 python-1.7.0)로 프로덕션 채택이 가속 중입니다(출처 4).

**Project Polaris**는 Microsoft 자체 코딩 모델로, 2026년 8월부터 GitHub Copilot 기본 모델로 GPT-4 Turbo를 대체할 예정입니다(출처 1). OpenAI 의존을 줄이고 Claude Code 등과 경쟁하려는 **모델 자립 + 에이전트 코딩** 전략으로 읽힙니다(출처 1).

### ③ 플랫폼·기업: '대화'에서 '업무 위임'으로

Mistral은 5월 28일 **Vibe**로 리브랜딩하며 Work Mode(메일·Slack 등 연동 업무)와 Code Mode(샌드박스 코딩·PR)를 통합했습니다(출처 6). Kore.ai **Artemis**(5월 21일)는 ABL·Arch 설계 도구로 기업용 멀티 에이전트를 빠르게 만들되 거버넌스를 전제로 합니다(출처 7). 두 사례 모두 **질문에 답하는 창 → 일을 맡기는 직원**으로 포지셔닝이 바뀌었음을 보여 줍니다(출처 6, 7).

## 4. 소결론

이번 주 AI 핫 트렌드는 **① Windows·Azure 기반 에이전트 OS·스토어·Mesh**, **② Agent Framework + Polaris로의 개발·모델 자립**, **③ Mistral·Kore.ai 등 업무 위임형 플랫폼 경쟁** 세 축으로 요약됩니다. 기술 선택 시 "어떤 모델이 더 똑똑한가"보다 **에이전트가 어디서 돌고, 어떻게 배포·감사·수익화되는가**가 더 중요한 질문이 되었습니다.

## 작성자 노트

본 초안은 report-writer 스킬을 메인 에이전트가 직접 적용해 작성했습니다. Build 2026 키노트·Agent Store 세부 정책은 행사 진행 중 공개분을 기준으로 했으며, Adobe·Zoom 등 초기 파트너 사례(출처 1)는 후속 검증이 필요합니다. EU 규제·글로벌 모델 출시(Anthropic, NVIDIA 등)는 본 챕터 범위에서 의도적으로 축소했습니다.

끝.
