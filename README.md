# 짠티 (ZZANT) — 맥락 기반 전문가 통역 플랫폼

> **Context-Aware Translation + Dual Viewer for Medical Conferences**

## 라이브 데모

**[https://huhyoundo.github.io/zzanti-demo/](https://huhyoundo.github.io/zzanti-demo/)**

브라우저로 열면 코엑스 한국심장학회 가상 세션의 짠티 듀얼 뷰어 동작 화면을 확인할 수 있습니다.

---

## 핵심 USP — 3축 구조

### 1) 맥락 기반 priming (Context-Aware Translation)

파파고·DeepL·구글번역은 **사용자가 누구인지 모른 채** 번역합니다. 짠티는 발표자/사용자의 정체성(소속·전공·발표주제·슬라이드)을 LLM system prompt에 사전 주입해 동음이의어·전문 약어를 정체성 기반으로 정확히 해석합니다.

| 단어 | 정체성: 생명공학 교수 | 정체성: 일반인 | 일반 AI (정체성 무지) |
|---|---|---|---|
| **가위** | CRISPR (유전자가위) | scissors | scissors (디폴트) |
| **AF** | atrial fibrillation (심장내과) | autofocus (사진가) | "AF" 그대로 |
| **교정** | orthodontic correction (치과) | proofreading (출판) | correction (디폴트) |

### 2) 듀얼 뷰어 (PPT/PDF/HTML 좌 · 실시간 자막 우)

학회 발표 자료와 실시간 통역 자막을 한 화면에 동시 표시. WebSocket으로 슬라이드·자막 자동 동기. 외국인 청중이 "슬라이드↔자막" 시선 분산 없이 발표를 따라갈 수 있습니다.

### 3) 의사 서면 testimonial — 사전 확보

코엑스 표준 통역 솔루션과 비교 평가한 의사의 서면 testimonial을 사전 확보. 의료기관 B2B 영업의 결정적 신뢰 시그널.

---

## 시장

- **1차 진입**: 코엑스 매년 의료 학회 약 100건 × 듀얼 뷰어 패키지 ₩700만 = **₩70억 시장**
- **2차**: 강남·종로 외국인 진료 의료기관 (성형·산부인과·내과) B2B 월정액
- **3차**: 의료 강의 콘텐츠사 다국어 자막 패키지
- **확장**: 의료를 beach-head로 법률·공학·금융 전문영역으로 priming 메커니즘 이전

---

## 비즈니스 모델

| 매출원 | 단가 | 비고 |
|---|---|---|
| 학회 일체형 듀얼 뷰어 패키지 | ₩500~1,000만/일 | 자료+통역+자막 송출 일체 |
| 의료기관 B2B 월정액 | ₩50~500만/월 | 외국인 진료 듀얼 뷰어 |
| 의료 강의 콘텐츠사 | ₩50~200만/편 | 다국어 자막 후처리 |
| API 분당 사용량 | ₩100~500/분 | EMR·VoIP·콘텐츠사 연동 |

---

## 기술 스택

- **음성 인식**: OpenAI Whisper API (스트리밍)
- **번역**: GPT-4 / Claude / DeepL API + priming system prompt
- **의료 용어 검증**: 1만 개 의료 용어 사전 후처리 매칭
- **듀얼 뷰어 프론트**: React + PDF.js (PDF) + reveal.js (HTML) + python-pptx (PPT)
- **슬라이드·자막 동기**: WebSocket 양방향
- **앱**: React Native (iOS/Android)
- **백엔드**: Python FastAPI

---

## 도전자 운영 이력

- 종토넷 (네이버 종목토론방 종합 스크래핑) — 월 방문 23만 · 서버비 ₩30만 · 1인 풀스택 운영 중
- Claude Code + Python 기반 1인 풀스택

---

## 모집공고

본 자료는 **모두의 창업 프로젝트 2026 (중기부 공고 제2026–208호)** 일반/기술트랙 도전신청서 첨부용입니다.
