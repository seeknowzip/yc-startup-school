# Interaction Models 용어 번역안 v2

- 원문: <https://thinkingmachines.ai/blog/interaction-models/>
- 작성 기준: 2026-05-25 KST
- 대상 독자: Claude Code, Codex, Cursor 등 AI coding/agent 도구에 익숙한 사람
- 원칙: 핵심 기술어는 보존한다. 한국어로 완전히 풀어헤치기보다, 읽는 흐름을 막는 용어만 짧게 보정한다.

## 번역 기준

이 글의 `interaction`은 UI 이벤트가 아니라 **실시간 협업 능력**에 가깝다. 따라서 제목과 핵심 thesis에서는 `interaction model`을 **실시간 협업형 모델**로 옮긴다. 다만 기술 설명에서는 원문 용어를 함께 둔다. 독자가 검색하고 원문과 대조할 수 있어야 한다.

## 용어표

| 원문 | v4 번역 | 사용 메모 |
|---|---|---|
| interaction model | 실시간 협업형 모델 | 첫 등장: 실시간 협업형 모델(interaction model). 이후 문맥상 원문 병기 생략 가능. |
| interactivity | 실시간 협업성 / interactivity | 평가·벤치마크 문맥에서는 interactivity 병기. |
| external scaffolding | 외부 scaffolding / 바깥 scaffolding | “연결 장치”보다 기술 맥락을 살림. |
| harness | harness / 하네스 | AI agent/tooling 독자는 이해 가능. VAD, ASR/TTS, router를 붙이는 구조. |
| turn-based interface | 턴제 인터페이스 | 그대로 사용. |
| human-in-the-loop | human-in-the-loop | 굳이 “루프 안의 인간”으로 풀지 않음. |
| modality | modality | 첫 등장에만 “텍스트·음성·영상 같은 modality” 정도로 보조. |
| multimodal / omnimodal | multimodal / omnimodal | 원문 유지. 필요하면 짧게만 설명. |
| multi-stream, micro-turn design | multi-stream, micro-turn 설계 | 200ms 단위라는 숫자를 본문에서 설명. |
| time-aligned micro-turns | time-aligned micro-turns / 시간 정렬 micro-turn | 섹션 제목은 원문 유지. |
| full-duplex | full-duplex / 동시 양방향 | 기술어 유지. |
| background model | background model / 배경 모델 | “뒤에서 깊게 생각하는 모델”은 설명문에만 사용. |
| agentic workflows | agentic workflow | 원문 유지. |
| dialog management | dialog management / 대화 타이밍 관리 | 컴포넌트명 느낌 유지. |
| backchannel | backchannel / 맞장구 신호 | 대화 분석 용어라 원문 유지. |
| proactive interjection | proactive interjection / 선제적 끼어들기 | “먼저 끼어들기”보다 덜 유아적. |
| visual proactivity | visual proactivity | 원문 유지. 필요하면 “시각 입력 기반 선제 응답”으로 풀이. |
| encoder-free early fusion | encoder-free early fusion | 제목 원문 유지, 본문에서 구조 설명. |
| prefill / decode | prefill / decode | 추론 서버 용어 그대로. |
| streaming sessions | streaming sessions | 원문 유지. “GPU memory의 persistent sequence에 append”로 설명. |
| bidirectional serving | bidirectional serving | 원문 유지. |
| MoE kernels | MoE kernels | 원문 유지. |
| trainer-sampler alignment | trainer-sampler alignment | 원문 유지. |
| batch-invariant kernels | batch-invariant kernels | 원문 유지. |
| modality-appropriate refusals | modality-appropriate refusals | 안전성 문맥에서 원문 유지 후 짧게 설명. |
| long-horizon robustness | long-horizon robustness | 원문 유지. |

## v4 편집 방향

- “쉽게 말하면”식 설명을 줄인다.
- 독자를 AI 도구 초심자가 아니라, Claude Code/Codex를 이미 쓰는 builder로 둔다.
- thesis는 과감하게 살린다. 이 글은 “voice chatbot UX 개선”이 아니라, **agentic AI의 다음 병목을 실시간 협업성으로 재정의하는 글**이다.
- 설명은 낮추지 말고 압축한다. 예: “background model = 뒤에서 깊게 생각하는 모델”보다는 “background model이 tool use와 long-horizon work를 비동기로 처리한다.”

## 참고 출처

- Thinking Machines Lab 원문: <https://thinkingmachines.ai/blog/interaction-models/>
- METR, “Measuring AI Ability to Complete Long Tasks”: <https://metr.org/blog/2025-03-19-measuring-ai-ability-to-complete-long-tasks/>
- Sutton, “The Bitter Lesson”: <http://www.incompleteideas.net/IncIdeas/BitterLesson.html>
- Moshi: <https://arxiv.org/abs/2410.00037>
- SGLang streaming sessions PR: <https://github.com/sgl-project/sglang/pull/19171>
- Thinking Machines, “Defeating Nondeterminism in LLM Inference”: <https://thinkingmachines.ai/blog/defeating-nondeterminism-in-llm-inference/>
