# Quantum Research Trend Report — 2026-06-19

> **수집 기준**: 2026-06-18 제출 논문 (arXiv quant-ph)
> **우선순위 키워드**: Quantum Communication, QKD, Entanglement Distribution, Quantum Network, Quantum Teleportation
> **수집 논문 수**: 30편 이상

---

## 목차
1. [핵심 논문 Top 5 심층 분석](#핵심-논문-top-5-심층-분석)
2. [추가 논문 요약](#추가-논문-요약)
3. [트렌드 분석](#트렌드-분석)

---

## 핵심 논문 Top 5 심층 분석

---

### 1. Field Demonstration of a Multi-User Continuous-Variable Quantum Access Network for Quantum-to-the-Home

**arXiv:** [2606.18840](https://arxiv.org/abs/2606.18840)
**저자:** Junpeng Zhang, Xu Liu, Qijun Zhang, Yifeng Liang, Yue Yu, Peng Huang et al.
**소속:** (Guihua Zeng 연구그룹)
**제출일:** 2026-06-17

#### 요약
상용 광섬유 기반의 CV-QAN(Continuous-Variable Quantum Access Network)을 실제 현장에서 1:16 규모로 실증한 논문. QTTH(Quantum-to-the-Home) 구현에 있어 핵심 장애물인 **링크 비대칭 문제**를 다중 사용자 최적화 모델로 해결하였다.

#### 기술적 기여
- **다중 사용자 효용 모델(Multi-user utility model)** 설계: QLT(Quantum Line Terminal)와 16개 QNU(Quantum Network Unit) 사이의 글로벌 최적 변조 분산(modulation variance) 선택 가능
- **1:16 현장 시험(field trial)** 성공: 상용 FTTH 광섬유 인프라 위에서 Mbit/s급 점근적 보안 키 생성률(asymptotic secure key rate) 달성
- 강인한 디지털 신호 처리(DSP) 기술로 브로드캐스트 채널의 링크 다양성 극복
- 신뢰된 로컬 네트워크 도메인 내에서의 운영 모델 확립

#### 의의
CV-QAN은 BB84 기반 DV-QKD보다 상용 광 인프라 호환성이 높다. 이 연구는 이론 프로토콜과 현실 FTTH 인프라 사이의 간극을 처음으로 현장 규모에서 좁힌 사례로, **양자 인터넷의 라스트마일(last-mile) 접속** 문제 해결에 직접적 기여를 한다.

#### 응용 가능성
- ISP(인터넷 서비스 제공자) 기존 광섬유 망에 양자 보안 서비스 오버레이
- 스마트홈·의료·금융 분야 양자 보안 통신 보급
- 국가 양자 네트워크 인프라의 가입자망(access network) 표준 모델

---

### 2. Enhancing the Teleportation Fidelity of a Quantum Network Using Purification

**arXiv:** [2606.18743](https://arxiv.org/abs/2606.18743)
**저자:** Soumit Roy, Md Sohel Mondal, Siddhartha Santra, Indranil Chakrabarty
**제출일:** 2026-06-17

#### 요약
정규(regular) 및 랜덤 네트워크 위상을 포함한 다양한 양자 네트워크 토폴로지에서 **단일 경로 얽힘 스와핑** 대비 **다중 경로 얽힘 정제(purification)** 프로토콜의 우수성을 정량적으로 비교 분석한 논문.

#### 기술적 기여
- **평균 최대 텔레포테이션 충실도(average maximum teleportation fidelity)** 지표를 네트워크 자원성(resourcefulness) 척도로 활용
- **에지 사용량 및 경로 순서 제약 하에서** 이 지표를 추정하는 알고리즘 제시
- 정제 기반(purification-based) 프로토콜이 단순 스와핑 대비 **평균 텔레포테이션 충실도를 획기적으로 향상**시킴을 광범위한 토폴로지에서 입증
- 네트워크 토폴로지 선택이 분산 프로토콜 성능에 미치는 민감도 분석

#### 의의
단일 경로 경유 양자 중계기 프로토콜의 한계를 다중 경로 정제로 극복하는 일반 이론을 확립. 특히 랜덤 네트워크에서도 성능 향상이 유효함을 보여 **현실적 양자 인터넷 설계**에 중요한 지침을 제공한다.

#### 응용 가능성
- 도시 규모 양자 중계기 네트워크 토폴로지 최적 설계
- 분산 양자 컴퓨팅(distributed quantum computing)의 얽힘 분배 계층 설계
- 위성-지상 양자 네트워크의 다중 경로 활용 전략

---

### 3. Efficient Simulation of Noisy Entanglement Generation

**arXiv:** [2606.18808](https://arxiv.org/abs/2606.18808)
**저자:** Lorenzo Brevi, Federico Grasselli, Alessandro Caraceni, Massimiliano Proietti, Massimiliano Dispenza et al.
**제출일:** 2026-06-17

#### 요약
양자 네트워크 시뮬레이터 SeQUeNCe의 얽힘 생성 모듈을 개선하여, **다양한 현실적 노이즈 소스를 반영하면서 계산 시간을 60% 이상 단축**하는 해석적(analytic) 결과를 도출한 논문.

#### 기술적 기여
- 성공 확률, 출력 상태, 충실도를 **직접 반환하는 해석적 공식** 유도: 불완전 모드 매칭, 다크 카운트, 불완전 메모리 초기화 등 다양한 노이즈 반영
- 업그레이드된 **SeQUeNCe 시뮬레이터**에 통합: 계산 시간 60% 이상 감소
- 실제 실험 데이터와의 벤치마킹: 평균 얽힘 생성 시간 및 최종 상태 충실도 재현 성공
- **대규모 양자 네트워크 시뮬레이션** 가능성 크게 향상

#### 의의
현실적이고 확장 가능한 양자 네트워크 시뮬레이션 도구는 양자 인터넷 설계와 프로토콜 검증의 핵심 인프라. 이 연구는 시뮬레이션 정확도와 속도를 동시에 향상시켜 **대규모 양자 네트워크 공동 연구의 가속화**에 기여한다.

#### 응용 가능성
- 양자 중계기 네트워크 성능 사전 평가 및 최적화
- 분산 양자 컴퓨팅 클러스터 설계 검증
- 양자 인터넷 표준화 기구의 시뮬레이션 기준 도구

---

### 4. Covert Blockwise Coding with Sequential Detection over Thermal-Loss Bosonic Channels

**arXiv:** [2606.18666](https://arxiv.org/abs/2606.18666)
**저자:** Qipeng Qian, Yuntao Qian
**제출일:** 2026-06-17

#### 요약
열 손실 보소닉 채널(thermal-loss bosonic channel)에서 **수신자 중심의 블록 단위 순차 탐지 프레임워크**를 최초로 개발한 논문. 은닉 통신(covert communication)의 새로운 이론적 기반을 제시한다.

#### 기술적 기여
- **블록 = 이진 슈퍼 심볼** 구조: 탐지 세그먼트 최소 길이 도출로 Bob이 블록 종료 전 능동 블록 탐지 가능
- **정보 성장의 비대칭성** 활용: Bob의 사후 변화 정보 성장은 소신호 체계에서 선형적이나, Willie의 탐지 가능성은 양자 상대 엔트로피 법칙에 따라 이차(quadratic)적
- **CUSUM(Cumulative Sum) 탐지기**를 이용, 지수적 높은 확률로 동일 블록 내 임계값 초과 조건 도출
- **보소닉 은닉 통신, 순차 탐지, 블록 단위 시그널링** 사이의 구체적 연결 고리 확립

#### 의의
기존 보소닉 채널 은닉 통신 연구는 주로 송신자 중심이었으나, 이 연구는 수신자 측의 탐지 전략에 초점을 맞춘 최초의 프레임워크. **물리 계층 보안(physical-layer security)** 이론의 새 지평을 연다.

#### 응용 가능성
- 위성 및 자유 공간 양자 광 통신 채널의 은닉 통신 설계
- 양자 군사 통신 및 기밀 외교 통신 채널 프로토콜
- 양자 스텔스 네트워크의 탐지 임계 분석

---

### 5. All Reflective Field-widened Unbalanced Interferometer for Quantum Sensing and Communication Applications

**arXiv:** [2606.18358](https://arxiv.org/abs/2606.18358)
**저자:** Ramy Tannous, Dogan Sinar, Tabitha D. Arulpragasam, Thomas Jennewein
**제출일:** 2026-06-17

#### 요약
적응형 광학(adaptive optics) 없이 멀티모드 빔에서 **간섭 가시도(visibility) > 0.97**을 달성하는 전반사(all-reflective) 필드 확장 불균형 간섭계를 개발한 논문. 난기류 채널 및 시간-빈(time-bin) 인코딩 양자 시스템에 직접 적용 가능하다.

#### 기술적 기여
- **전반사 표면만 사용**하는 간섭계 구조: 색수차 제거 및 광대역 동작 가능
- **멀티모드 빔에서 0.97 이상 가시도** 실증: 대기 난기류 채널에서의 견고성 확보
- **시간-빈 인코딩 양자 시스템** 직접 호환성 확인
- 자유 공간 양자 통신 및 위성 기반 QKD 링크에 필요한 저비용·고성능 광 부품

#### 의의
기존 편광 기반 QKD는 대기 난기류에 취약하나 시간-빈 인코딩은 이에 강인하다. 이 간섭계는 시간-빈 QKD 시스템의 실용화를 위한 **핵심 광 부품**으로서, 드론/위성 기반 도심 양자 통신 인프라 구축을 앞당길 수 있다.

#### 응용 가능성
- 위성-지상 및 드론 기반 자유 공간 QKD 시스템 광 수신 모듈
- 도시 건물 간 시간-빈 인코딩 QKD 링크
- 양자 센싱(중력 측정, 관성 항법) 정밀 간섭계

---

## 추가 논문 요약

### 양자 통신 / 네트워크 관련

| # | arXiv ID | 제목 | 저자 | 주요 내용 |
|---|---|---|---|---|
| 1 | 2606.18720 | Memory-assisted advantage for state transfer in disordered quantum many-body scar system | Paranjoy Chaki, Ujjwal Sen | 다체 스카(scar) 시스템의 기억 있는 장애가 메모리 없는 경우보다 양자 상태 전송 성능 우수; 스카 정도가 높을수록 전송 향상 |
| 2 | 2606.18756 | Universal photon blockade via two-photon light-matter interaction at chiral exceptional points | Hai-Tao Dong, Meng-Long Song et al. | 카이럴 예외점에서 한 모드는 강한 광자 차단, 다른 모드는 아포이소닉 분포 발현; 선택적 양자 광원 생성 가능 |
| 3 | 2606.18515 | Towards an Optimally Distributed Quantum Fourier Transform Circuit | Zachary Vernec, Michael Silver, Hans-Arno Jacobsen | 분산 QFT 회로의 e-bit 수 최소화 파티셔닝 방법; 양자 하드웨어 검증 완료 |
| 4 | 2606.19180 | Quantum magic is necessary but not sufficient for wormhole-inspired teleportation | Sudhanva Joshi, Sunil Kumar Mishra | 웜홀 기반 텔레포테이션에서 양자 매직의 필요성과 불충분성 규명; 구조화된 매직 재분배가 성공 조건 |

### 양자 얽힘 / 센싱

| # | arXiv ID | 제목 | 저자 | 주요 내용 |
|---|---|---|---|---|
| 5 | 2606.18552 | Towards Entanglement-Enhanced Atom Interferometry Using Bow-Tie Cavities | Christian Mancini, Marco Malitesta et al. | 파이네스 5.7×10⁴ 나비넥타이 공진기로 피드백 24 dB, QND 측정 28 dB 스핀 스퀴징; 차세대 원자 간섭계 |
| 6 | 2606.18415 | Entanglement response to Temperature in Interacting Two-Qubit Thermal States | Zain H. Saleem, Iram Saleem | 두 큐비트 열 얽힘의 정확한 해석적 표현; 열 QFI가 온도에 대한 얽힘 변화율 경계 설정 |
| 7 | 2606.18361 | Universal entanglement probes of topological order and locally-achiral manifolds | Yarden Sheffer | 국소 아카이럴 다양체로부터 위상 분배 함수 추출; 2+1d 위상 위상의 보편적 성질 접근 |
| 8 | 2606.18871 | Sensitive endoscopic diamond magnetometer | Wesseler, Nagy | 6mm 내시경 다이아몬드 자력계, 91 pT/√Hz 감도; 의료·산업 한정 공간 측정 응용 |

### 양자 컴퓨팅 / 알고리즘

| # | arXiv ID | 제목 | 저자 | 주요 내용 |
|---|---|---|---|---|
| 9 | 2606.18339 | Ground state preparation of random all-to-all Hamiltonians using ADAPT-VQE | Sabhyata Gupta et al. | TETRIS-ADAPT-VQE가 SK 모델 18 사이트에서 99.9998% 충실도; 무작위 해밀토니안 기저 상태 준비 |
| 10 | 2606.18580 | Separation of Statistical Complexity and Trainability in Variational Quantum Circuits | Suman Mandal et al. | 회로 깊이 증가 시 통계적 무작위성 먼저 등장, 훈련 가능성은 유지; 바렌 평원 완화 전략 |
| 11 | 2606.18428 | Quantum algorithm for Valiant-Vazirani reduction | Patrick Kelly et al. | SAT → UNIQUE SAT 환원 양자 알고리즘; 비선형 양자 코프로세서에서 NP 다항 시간 풀이 가능 |
| 12 | 2606.18422 | Gatekeepers and Hallucinations: A Layered Evaluation Framework for LLM-Driven Quantum Circuit Generation | Christopher Coleman, Sharon Marfatia | LLM 기반 양자 회로 생성의 5가지 실패 유형 분류; 게이트키퍼 검증 필수성 실증 |
| 13 | 2606.18534 | Ground- and excited-state energies extraction via Trotterization on IBM quantum computers | Fernando Espinoza-Ortiz et al. | IBM 양자 컴퓨터에서 하다마드 테스트 + 트로터화로 6 스핀까지 고유에너지 추출 |
| 14 | 2606.18612 | Characterization of three-qubit controlled unitary gates of Schmidt rank three | Xiutao Zhang | 슈미트 랭크 3 세 큐비트 제어 게이트 필요충분 조건; W-클래스 출력 및 CNOT 3개 구현 가능 |

### 양자 광학 / 물성

| # | arXiv ID | 제목 | 저자 | 주요 내용 |
|---|---|---|---|---|
| 15 | 2606.19219 | Spontaneous parametric down-conversion pumped by spatiotemporal structured light | Lukas Montenegro, Rafael F. Barros | 펌프 빔의 공간·스펙트럼 구조화로 양자 얽힘 광자쌍의 이-광자 스펙트럼 상관관계 완전 제어 |
| 16 | 2606.19085 | Quantum Pump Depletion and Multicomponent Schrödinger-Cat-Like States in Doubly Pumped Kerr Microresonators | Ranjit Singh, Alexander E. Teretenkov | 이중 펌프 커 마이크로공진기에서 다성분 고양이 상태 생성; 위그너 함수 음수성 확인 |
| 17 | 2606.18605 | The quantum-advantage resource in multimode OPA light | Vitaly Kocharovsky, Kunwar Kalra | 혼합 다중모드 가우시안 상태의 양자 복잡도 자원 도입; 펄스 OPA 최적화 지침 제공 |
| 18 | 2606.18408 | Characterization of nested Walsh parity-check filters in a single-photon eight-mode register on a cloud photonic processor | Emma Tully, Jonathan Washburn, Megan Simons | Quandela Belenos 광자 프로세서에서 Walsh 패리티 체크 필터 특성화; 94-99% 선택성 확인 |
| 19 | 2606.18755 | Quantum simulation of neutrino oscillations with bosonic encoding | Sandeep Joshi | 공진기 보소닉 모드 인코딩으로 뉴트리노 진동 양자 시뮬레이션; 이론 예측과 높은 일치 |

### 기초 물리 / 기타

| # | arXiv ID | 제목 | 저자 | 주요 내용 |
|---|---|---|---|---|
| 20 | 2606.19027 | Nonequilibrium steady states induced by stochastic mid-circuit measurements and resets on a quantum computer | Jakob Murauer, Sabine Tornow, Gabriele Perfetto | 초전도 양자 프로세서에서 중간 회로 측정·리셋으로 비평형 정상 상태 구현; 양자 상전이 관련 교차 현상 |
| 21 | 2606.18991 | Measurement-enabled online quantum processing with amplitude encoding | Giacomo Franceschetto et al. | 부분 추적 역학 구현하는 진폭 인코딩 양자 저장소 컴퓨팅 프로토콜; 간접 측정으로 저장소 관측값 접근 |
| 22 | 2606.18340 | Chaos from quantum bath fluctuations | Ilan Baud, Tamoghna Ray et al. | 환경 양자 요동이 고전적으로 규칙적인 계에 혼돈 생성; 산란 딕케 모델에서 프랙탈 차원·양수 리야푸노프 지수 |
| 23 | 2606.18348 | Steady-state spectral kissing and dissipative phase transitions | Devesh Karthik et al. | 산란 커 파라메트릭 진동자에서 스펙트럼 키싱(energy level kissing); 산란 상전이에서 소멸 |
| 24 | 2606.18360 | Equilibration of generalized subsystems: a quantum-channel approach | Pedro S. Correia et al. | 양자 채널 접근법으로 시스템-환경 평형화 통합 프레임워크; 평형화 발생 조건 경계 도출 |
| 25 | 2606.18443 | Noncyclic geometric phase in three-level Ramsey interferometry for enhanced metrology | Zhifan Zhou, Yaxin Li | 3준위 램지 간섭계에서 비순환 기하학적 위상으로 감지 향상; 측지선 근방 신호 대 잡음비 증폭 |

---

## 트렌드 분석

### 1. 양자 인터넷 실용화 가속

오늘 수집된 논문들에서 가장 두드러진 흐름은 **양자 네트워크의 현장 실증(field demonstration)**이다. 2606.18840 논문은 상용 FTTH 광섬유 망 위에서 1:16 CV-QAN 현장 시험을 성공시키며, 양자 네트워크가 더 이상 실험실 수준에 머물지 않음을 보여준다. 동시에 2606.18808은 SeQUeNCe 시뮬레이터를 통해 대규모 네트워크 설계와 검증의 효율화를 도모하며 인프라 계층을 지원한다.

### 2. 다중 경로·정제 기반 얽힘 분배 부상

단일 중계기 경로에서 벗어나 **다중 경로 + 정제(purification) 결합** 전략(2606.18743)이 학술적으로 주목받고 있다. 네트워크 토폴로지 전반에 걸친 성능 우위가 입증됨에 따라, 차세대 양자 중계기 설계는 다중 경로 정제를 핵심 기능으로 채택하는 방향으로 전환될 것으로 예상된다.

### 3. 물리 계층 보안 이론의 심화

양자 채널에서의 **은닉 통신(covert communication)** 이론(2606.18666)과 **자유 공간 채널용 광 부품**(2606.18358) 개발이 동시에 진전되고 있다. 이는 물리 계층 보안과 실용 광학 구현이 병행 발전하고 있음을 시사한다.

### 4. 변분 양자 알고리즘의 성숙

ADAPT-VQE(2606.18339)와 통계적 복잡도-훈련 가능성 분리 연구(2606.18580)는 변분 양자 알고리즘(VQA) 분야가 이론적 한계를 명확히 이해하고 실용적 해결책을 모색하는 성숙 단계에 접어들었음을 보여준다.

### 5. 양자 광학과 정보 이론의 융합

자발 매개 하향 변환(SPDC) 제어(2606.19219), 고양이 상태 생성(2606.19085), OPA 다중 모드 자원(2606.18605) 등 양자 광학 연구들이 정보 처리 응용과 긴밀히 연결되며 **양자 광 정보 과학**의 통합적 발전을 나타낸다.

---

*리포트 생성: Claude Code (QuantumTrend 자동화 시스템)*
*데이터 소스: arXiv quant-ph (export.arxiv.org)*
