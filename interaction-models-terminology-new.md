# Interaction Models 용어 쉬운 번역안 (new)

- 원문: <https://thinkingmachines.ai/blog/interaction-models/>
- 작성 기준: 2026-05-25 09:54 KST
- 대상 독자: Claude Code, Codex, Cursor, Replit Agent 등 AI 코딩/에이전트 도구는 써봤고, 다음 세대 인터페이스를 더 잘 이해하고 싶은 사람
- 원칙: 논문식 직역보다 “손에 잡히는 한국어” 우선. 단, 첫 등장에는 원문 병기.

## 한 줄 결론

이 글의 핵심 용어는 `interaction`이 아니다. **“사람이 실시간으로 끼어들 수 있는 협업”**이다. 그래서 `interaction model`은 단순히 “상호작용 모델”이라고 하면 약하다. 본문에서는 **실시간 협업형 모델**을 기본어로 쓰고, 기술 설명에서는 원문을 병기한다.

## 용어 치환표

| 원문 용어 | v3 기본 번역 | 더 쉬운 설명 | 왜 이렇게 바꿨나 |
|---|---|---|---|
| Interaction models | **실시간 협업형 모델** | 사람과 AI가 말·화면·텍스트를 동시에 주고받으며 같이 일하는 모델 | “상호작용”은 UI 이벤트처럼 들린다. 이 글의 주장은 “협업 능력도 모델 안에서 스케일해야 한다”에 가깝다. |
| Interactivity | **실시간 협업성** | 똑똑함뿐 아니라, 제때 보고 듣고 끼어드는 능력 | 단순 반응성이 아니라 “함께 일하기 좋은 성질”이다. |
| External scaffolding / harness | **바깥 덧대기 / 연결 장치** | 모델 밖에서 VAD, ASR, TTS, 툴 라우터 등을 이어붙인 구조 | Claude Code/Codex 사용자는 “에이전트 하네스” 감각이 있다. 다만 일반 독자에게는 연결 장치가 더 쉽다. |
| Turn-based interface | **턴제 인터페이스** | 사용자가 끝까지 말하면 AI가 답하고, AI가 끝까지 답하면 다시 사용자가 말하는 방식 | 게임의 턴제 비유가 직관적이다. |
| Human in the loop | **사람이 계속 개입하는 상태** | AI가 혼자 달리는 게 아니라 사람이 중간중간 방향을 잡는 상태 | “루프 안의 인간”은 어색하다. |
| Modality | **입력/표현 방식** | 텍스트, 음성, 영상처럼 정보를 주고받는 채널 | 첫 등장: “입력/표현 방식(modality)”로 병기. |
| Multimodal / omnimodal | **멀티모달 / 모든 방식 통합형** | 글·말·영상 등을 함께 다루는 것 | 업계 독자는 멀티모달을 안다. omnimodal은 “모든 방식 통합형”으로 풀어준다. |
| Multi-stream, micro-turn design | **여러 흐름을 0.2초 단위로 쪼개 처리하는 설계** | 입력과 출력을 긴 턴 하나가 아니라 짧은 라이브 조각으로 엮는 방식 | micro-turn을 “미세 턴”이라 하면 감이 없다. 본문 핵심 숫자인 200ms를 살린다. |
| Time-aligned micro-turns | **시간에 맞춘 0.2초 단위 턴** | 같은 시간대의 입력·출력을 한 묶음으로 모델에 넣는 방식 | “time-aligned”는 동시성/타이밍이 핵심이다. |
| Full-duplex | **동시 양방향 대화** | 전화처럼 동시에 듣고 말할 수 있는 상태 | 네트워크 용어보다 통화 비유가 쉽다. |
| Background model | **뒤에서 깊게 생각하는 모델** | 앞에서는 즉각 대화하고, 뒤에서는 오래 걸리는 추론·검색·툴 작업을 하는 모델 | Claude Code의 서브에이전트/백그라운드 작업 감각과 연결된다. |
| Agentic workflows | **에이전트식 작업 흐름** | 계획 세우기, 도구 호출, 검색, 긴 작업 수행 | 업계어를 남기되 한 번 풀어쓴다. |
| Dialog management | **대화 타이밍 조절** | 말할 차례인지, 끼어들지, 기다릴지 판단하는 기능 | “대화 관리”보다 실제 기능이 보인다. |
| Backchannel | **맞장구/경청 신호** | “음”, “맞아요”, 끄덕임처럼 말권을 빼앗지 않는 반응 | 대화 분석 용어라 쉽게 풀어야 한다. |
| Proactive interjection | **먼저 끼어들기** | 사용자가 끝내기 전에 필요하면 바로 말하는 것 | 이 글의 데모 감각과 맞다. |
| Visual proactivity | **화면을 보고 먼저 말하기** | 사용자가 말하지 않아도 화면 변화가 생기면 AI가 말하는 능력 | “시각적 능동성”은 딱딱하다. |
| Encoder-free early fusion | **처음부터 한 모델 안에 섞기** | 음성/영상을 별도 큰 번역기(인코더)로 바꾸지 않고 초반부터 함께 학습 | 기술적으로는 early fusion이지만 독자에게는 “한 냄비에 처음부터 넣는다”가 이해된다. |
| Prefill / decode | **맥락 채우기 / 다음 말 뽑기** | LLM 서버가 기존 맥락을 읽고 다음 토큰을 생성하는 두 단계 | 추론 서버 경험이 없는 독자도 이해 가능. |
| Streaming sessions | **이어붙이는 라이브 세션** | 매 0.2초 요청을 GPU 메모리의 같은 대화 흐름에 계속 덧붙이는 방식 | 단순 스트리밍과 구분하려고 “이어붙이는”을 넣는다. |
| Bidirectional serving | **양방향 실시간 서빙** | 입력을 받으면서 동시에 출력도 내보내는 모델 서빙 | 인프라 문맥에서 사용. |
| MoE kernels | **전문가 묶음 모델용 GPU 계산** | Mixture-of-Experts 모델을 빠르게 돌리는 저수준 계산 | MoE는 업계어 유지, 첫 등장에 풀이. |
| Trainer-sampler alignment | **훈련 때와 실제 실행 때 결과 맞추기** | 학습기와 샘플러가 같은 조건에서 같은 비트 결과를 내도록 맞추는 것 | 직역하면 의미가 안 온다. |
| Batch-invariant kernels | **배치가 달라도 흔들리지 않는 GPU 계산** | 같이 처리하는 요청 묶음이 달라도 결과가 바뀌지 않게 하는 커널 | Thinking Machines의 다른 글과 연결되는 핵심. |
| Modality-appropriate refusals | **상황과 매체에 맞는 거절** | 텍스트식 딱딱한 거절이 아니라 말로 자연스럽지만 단호하게 거절 | 안전성 파트에서 중요. |
| Long-horizon robustness | **긴 대화에서도 무너지지 않는 안정성** | 오래 말해도 안전/행동 규칙이 흐트러지지 않는 성질 | 일반어로 풀어쓴다. |
| FD-bench / TimeSpeak / CueSpeak 등 | **벤치마크명은 유지 + 괄호 설명** | 예: TimeSpeak(정해진 시간에 말하기 평가) | 고유명사는 보존해야 검색 가능. |

## 웹 리서치 기반 근거 메모

| 출처 | 확인한 점 | v3 반영 |
|---|---|---|
| Thinking Machines Lab 원문 | interaction models는 외부 하네스가 아니라 모델 내부에서 오디오·비디오·텍스트를 실시간 처리하는 모델이라고 설명 | “실시간 협업형 모델”, “바깥 덧대기” 사용 |
| METR, “Measuring AI Ability to Complete Long Tasks” | 최근 AI 평가가 “얼마나 오래 혼자 작업할 수 있나”로 기울어 있다는 배경 | 자율 에이전트 vs 협업 인터페이스 대비를 강하게 설명 |
| Anthropic frontier model card 인용 | hands-on-keyboard 방식에서는 느리게 느껴져 가치가 덜했다는 진술 | Claude Code/Codex 독자에게 “지금 도구의 병목은 지능만이 아니라 대기/턴 구조”로 해석 |
| Clark & Brennan, “Grounding in Communication” | 공동 주의, 즉시성, 동시성이 커뮤니케이션 품질을 높인다는 프레임 | copresence/contemporality/simultaneity를 “같은 것을 보고, 바로 받고, 동시에 주고받기”로 풀어씀 |
| Sutton, “The Bitter Lesson” | 손으로 만든 시스템보다 일반적인 학습/스케일링이 장기적으로 이긴다는 주장 | “VAD 같은 덧대기보다 모델 자체가 배워야 한다”는 주장의 배경으로 반영 |
| Moshi: speech-text foundation model for real-time dialogue | full-duplex 실시간 음성 모델 계열의 선행 사례 | full-duplex를 “동시 양방향 대화”로 번역 |
| SGLang PR #19171 | streaming session fast path가 실제 서빙 계층의 최적화 주제임 | “이어붙이는 라이브 세션”으로 설명 |
| Thinking Machines, “Defeating Nondeterminism in LLM Inference” | batch-invariant kernel / 비결정성 제거가 TML의 지속 주제 | trainer-sampler alignment 파트를 “결과 재현성” 중심으로 풀어씀 |

## v3 번역 스타일 가이드

1. 제목과 핵심 개념에는 **실시간 협업형 모델**을 쓴다.
2. 첫 등장에는 `실시간 협업형 모델(interaction model)`처럼 원문을 병기한다.
3. `harness`는 문맥에 따라 “하네스”만 쓰지 말고 **바깥 덧대기/연결 장치**로 풀어쓴다.
4. `micro-turn`은 “미세 턴”보다 **0.2초 단위 턴**을 기본으로 한다.
5. 기술 깊이가 필요한 독자는 Claude Code/Codex에 익숙하므로 `agentic`, `MoE`, `prefill/decode` 같은 원어는 삭제하지 말고, 쉬운 한국어 설명을 붙인다.
6. 글의 과감한 메시지는 살린다: **이건 음성 챗봇 개선이 아니라, AI 작업 인터페이스의 중심축을 ‘혼자 실행’에서 ‘실시간 공동작업’으로 되돌리는 선언**이다.
