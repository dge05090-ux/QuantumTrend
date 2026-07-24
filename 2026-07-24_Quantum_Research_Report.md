# Quantum Research Report — 2026-07-24 (Friday)

> **수집 기준**: 2026-07-23 (목) arXiv quant-ph 신규 논문 (화~금요일 실행 규칙: 전날 자료)
> **생성일**: 2026-07-24 (금)
> **수집 논문 수**: 67편 (신규 제출 50편 + 교차등재 17편) — Top 5 심층 분석 + 대표 18편 요약 (총 23편 초록 확인), 나머지 44편은 제목 목록 수록
> **우선순위 키워드**: Quantum Communication, QKD, Entanglement Distribution, Quantum Network, Quantum Teleportation

> **비고**: `export.arxiv.org/api/query`(주 수집 경로)를 WebFetch로 조회한 결과 submittedDate 기준 2026-07-22까지의 데이터만 반환되는 기존 known issue가 재현되었다. CLAUDE.md 지침에 따라 `arxiv.org/list/quant-ph/recent` 대체 경로로 전환, "New submissions"·"Cross-lists" 섹션에서 announcement-date 기준 2026-07-23(목) 목록 전체 67편(신규 50 + 교차등재 17)을 확보해 이를 이번 리포트의 기준 데이터셋으로 사용했다(첫 WebFetch 응답의 상단 요약 텍스트가 "Cross-lists 0편"이라 표기하면서도 하단 목록에는 51~67번을 cross-list로 명시하는 자기모순을 보여, `arxiv.org/list/quant-ph/recent?skip=0&show=100` 재조회로 "Thu, 23 Jul 2026 (showing 67 of 67 entries)" 헤딩과 신규 50편/교차 17편 구분을 재확인했다). 이번 실행은 특히 우선순위 키워드에 직접 매칭되는 논문이 5편(Entanglement Distribution/Quantum Network 1편, Quantum Teleportation 1편, QKD 1편, Quantum Communication 1편, Quantum Network 1편) 확보되어, 별도의 일반 하이라이트 없이 Top 5 전체를 우선순위 키워드 매칭 논문으로 구성했다. 배치 조회(`id_list=...`)는 사용하지 않고 처음부터 개별 `arxiv.org/abs/<id>` 페이지를 병렬 WebFetch하여 초록을 수집했다.

---

## Top 5 심층 분석

### 1. Distributed Entanglement Distribution Using Multiple Entanglement Sources in WDM-based Quantum Optical Networks
**arXiv**: [2607.19849](https://arxiv.org/abs/2607.19849)
**저자**: Anuj Agrawal, Abhay Singh Dulta, Bhaskar Kanseri
**키워드**: Entanglement Distribution / Quantum Network

#### 기술적 기여
기존의 단일 얽힘원을 파장분할다중화(WDM)로 라우팅하는 방식에서 벗어나, 다중 광자쌍 소스를 분산 배치해 더 많은 노드쌍에 동시에 얽힘을 전달하는 방법을 제시했다. 실제 자체 제작한 두 개의 얽힘원으로 실험을 수행하고, 다양한 얽힘 품질·수요 조건을 가진 네트워크를 시뮬레이션해 광섬유 거리·홉 수에 따른 신호 열화를 분석했다.

#### 의의
단일광자(OP)와 양광자(BP) 얽힘 분배를 결합한 하이브리드 접근이 더 높은 유연성을 제공하며, 다중 소스 기반 분산 방식이 중앙집중형 방식보다 우수한 자원 활용도를 달성함을 실증했다. 얽힘 분배 네트워크 설계를 중앙집중식에서 분산식으로 전환하는 실용적 근거를 제시했다.

#### 응용 가능성
도시 규모 양자 광네트워크의 확장 가능한 얽힘 분배 인프라 설계, 다중 사용자 QKD 네트워크의 자원 스케줄링, WDM 기반 양자-고전 통신 공존 네트워크 구축에 직접 활용 가능하다.

---

### 2. Latency-Constrained Encoded Quantum Teleportation with Punctured Codes
**arXiv**: [2607.19770](https://arxiv.org/abs/2607.19770)
**저자**: Mahmoud Saad Abouamer, Jakob Kaltoft Søndergaard, Petar Popovski
**키워드**: Quantum Teleportation

#### 기술적 기여
저장 중 열화되는 얽힘쌍과 자원 획득 지연 사이의 상충 관계를 분석하고, 코드 펑처링(puncturing)을 이용해 지연시간 영역에 따라 유효 부호 길이를 유연하게 조정하는 부호화 텔레포테이션 기법을 제시했다. IEEE QCE26에 채택되었다.

#### 의의
적절히 선택된 펑처드 부호가 다양한 시간 제약 조건에서 성능을 개선하며, 동일한 자원 획득 지연 조건 하에서 부호화 전송이 비부호화 방식을 크게 능가함을 입증했다. 실용적 자원 제약을 고려한 양자 네트워크 설계의 필요성을 강조했다.

#### 응용 가능성
지연시간에 민감한 분산 양자컴퓨팅 노드 간 텔레포테이션, 실시간 양자 네트워크 프로토콜의 적응형 부호 설계, 얽힘 자원 저장·소모 스케줄링 최적화에 적용 가능하다.

---

### 3. Robust logical Bell nonlocality based on quantum error correction codes
**arXiv**: [2607.19728](https://arxiv.org/abs/2607.19728)
**저자**: Qi Zhang, Jia-Wei Ying, Cheng Liu, Lan Zhou, Yu-Bo Sheng
**키워드**: QKD

#### 기술적 기여
물리적 큐비트가 아닌 스태빌라이저 부호화 부분공간 내에 "논리적 벨 부등식"을 구성해 벨 비국소성을 결어긋남에 강인하게 보존하는 방법을 제시했다. [[3,1,1]], [[7,1,1]] 반복부호를 적용해 비트반전 오류 하에서 충실도 임계값을 82.8%에서 66.35%까지 크게 개선했다.

#### 의의
이 접근이 기기독립적(device-independent) QKD의 노이즈 내성 임계값을 최적 조건에서 10.64%에서 23.36%로 끌어올려, DI-QKD의 실용적 배치를 가로막던 핵심 장벽 중 하나인 노이즈 취약성을 정면으로 해소했다.

#### 응용 가능성
확장 가능한 논리 양자시스템에서의 강인한 벨 비국소성 구현, 잡음이 많은 실제 채널에서의 기기독립적 QKD 프로토콜, 다자간 시스템으로의 확장을 통한 양자 네트워크 보안 강화에 기여한다.

---

### 4. Construction of a Class of Communication-Efficient Quantum Secret Sharing Schemes
**arXiv**: [2607.19891](https://arxiv.org/abs/2607.19891)
**저자**: Chenhao Li, Zhihui Li, Jiansheng Guo, Yixin Chen, Yewei Wang
**키워드**: Quantum Communication

#### 기술적 기여
기존 램프(ramp) 양자 비밀공유 방식에서 중간집합(intermediate set)으로부터 정보가 누설되는 문제를 해결하기 위해 중간집합 탐지 방법을 도입하고, 도청 탐지 기능을 갖춘 통신 효율적 완전 양자 비밀공유 방식을 제안했다.

#### 의의
참여자 수에 따른 통신 비용 변화를 분석해 재구성 통신 비용을 최소화하는 최적 참여자 범위를 규명함으로써, 효율성과 보안성을 동시에 만족하는 양자 비밀공유 설계 지침을 제시했다.

#### 응용 가능성
다자간 양자 통신 네트워크에서의 안전한 비밀 분산, 도청에 강인한 분산 키 관리 시스템, 통신 오버헤드가 제한된 환경에서의 양자 보안 프로토콜 구축에 응용 가능하다.

---

### 5. Qoreo: Choreographic Programming for Quantum Distributed Systems
**arXiv**: [2607.20391](https://arxiv.org/abs/2607.20391)
**저자**: Jennifer Paykin, Steven Baldasty, Joseph P. Near, Christian Skalka
**키워드**: Quantum Network

#### 기술적 기여
여러 참여자가 조율하는 양자 시스템을 개별 프로세스가 아닌 단일 전역 프로그램("안무", choreography)으로 표현하는 프로그래밍 언어 Qoreo를 제시했다. 무복제 원리를 강제하는 선형타입 기반 양자 계산 계층, 양자·고전 통신을 관리하는 안무 계층, 개별 네트워크 노드용 프로세스 언어를 결합했다.

#### 의의
타입 안전성을 증명하고, 안무를 독립적 네트워크 프로세스로 자동 변환하는 엔드포인트 프로젝션 메커니즘이 건전하고 완전함을 입증했다. 특히 "타입이 올바른 모든 안무는 교착상태 없는 프로세스망으로 프로젝션된다"는 따름정리를 확보했다. 전체 이론체계는 Rocq 증명보조기로 정식화되었다.

#### 응용 가능성
NetQASM 시뮬레이션·배치를 지원하는 추출 기능을 갖춰, 분산 양자컴퓨팅·양자 네트워크 프로토콜의 정형 검증된 소프트웨어 개발, 교착상태 없는 다자간 양자 통신 프로토콜 설계에 직접 활용 가능하다.

---

## 추가 논문 요약 (18편)

| No. | arXiv ID | 제목 | 핵심 내용 | 분류 |
|-----|----------|------|-----------|------|
| 1 | 2607.20143 | Biased-noise qubits: a guide to efficient fault-tolerance using the hierarchy of errors | 편향 노이즈 큐비트에서 CX 게이트 편향보존 활용, 위상반전은 고임계값 부호로 비트반전은 연접부호로 계층적 처리 | 양자오류정정/결함허용 |
| 2 | 2607.19852 | Optimal Lower Bounds for Hamiltonian Simulation | 게이트·질의 복잡도의 점근적으로 타이트한 하한 제시, composite qDRIFT 상한과 정합 확인 | 양자알고리즘/복잡도이론 |
| 3 | 2607.20195 | Mesoscopic mechanical superpositions by gluing individual quantum systems | 광부양 나노입자 표면에 단일전자 시간빈 상태를 부착해 "기계적 슈뢰딩거 고양이" 생성 프로토콜 제안 | 옵토메카닉스/양자기초 |
| 4 | 2607.20107 | Intermittency in Quantum Graviton-Phonon Conversion | 공진 바 검출기의 중력자-포논 변환을 정확히 풀어, 결맞은 상태에서 간헐적 협대역 버스트 현상 규명 | 양자중력현상론 |
| 5 | 2607.20409 | Efficiently Simulable Pauli Correlation Encoding | 매치게이트·IQP 회로 기반 고전 시뮬레이션 가능 PCE로 MaxCut 등 최적화 문제에서 경쟁력 있는 해 도출 | 양자 최적화 |
| 6 | 2607.20060 | Physics-Informed Graph Neural Networks for Surface Code Decoding via Discrete Exterior Calculus | 이산 푸아송 방정식 기반 물리 정보 GNN 디코더, 경계별 전류 배수 차이로 논리오류 신호를 위상학적으로 규명 | 양자오류정정 |
| 7 | 2607.20045 | PN-QNN: Harnessing Physical Noise as a Native Regularizer in Photonic Hybrid Quantum Neural Networks | 물리적 노이즈가 티호노프형 정규화 항으로 작용, 데이터셋 의존적으로 성능 개선(단순 데이터셋 한정) | 양자머신러닝/포토닉 |
| 8 | 2607.19715 | Structured-light-mediated hybrid entanglement between photon polarization and electronic orbital angular momentum | 반도체 양자디스크에서 구조광 매개로 광자 편광-전자 궤도각운동량 하이브리드 얽힘 생성 제안 | 양자광학 |
| 9 | 2607.19602 | Quantum Gravity Simulation: Quantum simulation with a minimum length based on the generalised uncertainty principle | 최소 격자간격을 도입한 1차원 양자 시뮬레이션으로 일반화 불확정성원리(GUP) 유도, 양자중력 탐구 경로 제안 | 양자중력시뮬레이션 |
| 10 | 2607.19596 | Intelligent qubits | 위그너의 친구·프라우히거-레너 사고실험의 관찰자를 "지능형 큐비트"로 대체, 불리언 은닉변수 암묵적 치환 문제 지적 | 양자기초/측정문제 |
| 11 | 2607.19574 | Quantum codes from classical annealing | 적응형 담금질 알고리즘으로 CSS·SWEL 부호 탐색, 50큐비트까지 양자 길버트-바르샤모프 한계에 근접·상회 | 양자오류정정 |
| 12 | 2607.19533 | High-purity entanglement mediated by magnons despite weak coupling | 마그논이 계산기저 밖 전이에만 결합하도록 해 약결합에서도 충실도 0.99(이상)/0.91(비이상)의 벨쌍 생성 | 양자정보/스핀큐비트 |
| 13 | 2607.19499 | A unified framework for anomalous boson bunching | 후선택 출력상태의 총 비구별성으로 이상 번칭 현상 통합 설명, 순열 관련 추측의 반례 연결 | 양자광학/보손샘플링 |
| 14 | 2607.19477 | Quantum resonance-enhanced performance of quantum battery | 킥 프로토콜 자유회전자에서 양자공명이 충전전력 선형 증가·효율 근접 1을 동시 달성함을 실증 | 양자열역학 |
| 15 | 2607.20130 | Learning to Decode Quantum LDPC Codes via Cluster-Based Sequential Belief Propagation | 노드를 클러스터로 묶어 병렬 갱신하는 강화학습 기반 BP 스케줄링, 지연-병렬성 트레이드오프로 실용성 확보 | 양자오류정정/ML |
| 16 | 2607.19984 | A framework for separating dephasing from decoherence in matter-wave Bell interferometers | 슈윙거 SU(2) 매핑으로 물질파 벨 간섭계의 기하학적 위상이완·환경 결어긋남·검출 효과를 분리하는 프레임워크 | 양자계측/원자간섭계 |
| 17 | 2607.19832 | Toroidal Transitions in Hydrogenic and Alkali Atoms | 강자기장 내 원자 토로이달 전이 관측 난이도를 반자성 결합 혼입 효과로 재평가, 저주양자수계 관측 제안 | 원자물리 |
| 18 | 2607.19763 | Energy Flux as an Entanglement Current in Moving-Mirror Radiation | 이동거울 아날로그 호킹복사에서 비단조 가속 궤적이 음의 에너지 플럭스를 정보채널로 활용해 얽힘 접근성 증가 | 양자장론/호킹복사 아날로그 |

---

## 나머지 논문 목록 (제목만 수록, 44편)

| arXiv ID | 제목 |
|----------|------|
| 2607.20388 | Arnold–Nielsen Geometry for Complexity-Deformed Noncommutative Transport |
| 2607.20377 | Statevector-Referenced Geometry Survival of a Four-Qubit ZZ Quantum Kernel on IBM Quantum Hardware |
| 2607.20333 | Collective Electronic Entanglement via Infrared Cavity-Induced Vibronic Transduction |
| 2607.20311 | Quantum-state block texture and its quantification |
| 2607.20292 | Microwave-driven same-species sympathetic cooling for trapped ions |
| 2607.20266 | Identifying local unitary equivalence based on reduction of quantum states |
| 2607.20264 | Dynamical redistribution of quantum resources in tree-level Bhabha scattering |
| 2607.20236 | Entanglement dynamics through electromagnetic interactions in single-electron traps |
| 2607.20234 | Coupling phase interference effects in a multimode cavity magnonics system |
| 2607.20231 | Lattice quantum electrodynamics of a molecular emitter in a topological gap |
| 2607.20225 | DQAOA-GPT: AI-Accelerated Distributed Quantum Optimization for Combinatorial Problems |
| 2607.20198 | Observable Geometry for Effective Quantum Circuits |
| 2607.20104 | Schrödinger's real-valued equation revisited |
| 2607.20042 | Slack-Free Deep-Unfolded Combinatorial Optimization Solver for Inequality Constraints |
| 2607.19884 | Propagation dynamics of high-gain vortex beams in symmetry-broken media via forward and backward three-wave mixing |
| 2607.19872 | Nonreciprocal phonon blockade in spin quadratic optomechanical systems |
| 2607.19871 | A reduction scheme for general-order Ising-like Hamiltonians in quantum heuristic solvers |
| 2607.19870 | Emergent boundary-memory from unitarity constraints in a minimal two interacting quantum particles |
| 2607.19861 | A Multi-Resolvent Hierarchy for the ETH Smooth Function |
| 2607.19853 | Generation of vortex-squeezed light in a coherently prepared medium |
| 2607.19782 | A Multiclass Quantum Aligned Centroid Kernel |
| 2607.19737 | The Quantum Adiabatic Theorem for Non-Hermitian Dynamics |
| 2607.19702 | Exact Closed-Form Quantum Correlations of Maximally Entangled Qudit States under Arbitrary Non-Markovian Pure Dephasing |
| 2607.19611 | On Solutions of the Killingbeck Potential and Clarifying Comments on a Related Analytical Approach |
| 2607.19601 | Bound states of the hydrogen-like atomic systems in plasma environments |
| 2607.19582 | Measurement-Selective Dynamical Symmetry Breaking |
| 2607.19577 | Rank-Adaptive Matrix-Free Atomic Quantum State Tomography |
| 2607.19563 | Machine-learned syndrome post-selection for reliable quantum error correction |
| 2607.19543 | Simple, accurate lumped-element models of distributed resonators for superconducting quantum circuits |
| 2607.19506 | Hybrid LLM-Guided Search for Quantum Reservoir Architecture Design |
| 2607.19447 | Hardware-in-the-Loop Syndrome-to-Decoder Validation for Repetition, Surface, CSS-LDPC, and Digitized-GKP Codes |
| 2607.19446 | Decoder Comparability Across Quantum Software Stacks: Repeated-Round Surface and Digitized-GKP Syndrome Replay |
| 2607.20412 | Fermionic pairs, from the surface to the bulk |
| 2607.20329 | Anticoncentration of the Permanent in Ginibre Ensembles |
| 2607.20283 | Angular Momentum Quantization of a Charge-flux Composite: Quantum Electrodynamic Approach |
| 2607.20168 | Quantum Kernels and the Cross-Section of Stock Returns: Anatomy of a Vanishing Advantage |
| 2607.19807 | Multi-Criticality and RG Topology in the Charge-Kondo-Breakdown Scenario in the Cuprates |
| 2607.19732 | A Thermodynamic Pinning Criterion for Two-Dimensional Structural Superlubricity |
| 2607.19698 | Analytical Retrieval of Material Parameters in Monolayer Transition-Metal Dichalcogenides Based on a Solvable Exciton Model |
| 2607.19680 | Nuclear Quantum Effects as a Denoising Problem |
| 2607.19649 | On the global well-posedness for the nonlocal Fokas-Lenells equation with the weighted Sobolev initial data on the line |
| 2607.19542 | Synthesizing superoscillations with just two frequencies |
| 2607.19468 | Confinement Versus Screening in the Schwinger Model on AdS₂ from Bosonization and Tensor Networks |
| 2606.26066 | All-electrical dephasing-protected spin qubits in altermagnets |

---

## 트렌드 분석

### 2026-07-23 주요 트렌드

1. **기기독립적 QKD의 노이즈 내성 장벽 해소**: 2607.19728은 물리 큐비트 대신 스태빌라이저 부호화 부분공간에 논리적 벨 부등식을 구성해, DI-QKD의 노이즈 내성 임계값을 10.64%에서 23.36%로 끌어올렸다. 오류정정과 비국소성 검증을 결합해 "실험실 조건에서만 성립하는 DI-QKD"라는 오랜 제약을 정면으로 공략한 결과다.

2. **양자 광네트워크의 중앙집중식→분산식 전환**: 2607.19849는 단일 얽힘원을 WDM으로 라우팅하던 기존 방식을 다중 소스 분산 배치로 전환해 자원 활용도와 노드쌍 커버리지를 동시에 개선했다. 이는 도시 규모 양자 네트워크 인프라 설계가 실험실 데모를 넘어 실용적 토폴로지 최적화 단계로 이동하고 있음을 보여준다.

3. **지연시간·자원 제약을 고려한 실용적 프로토콜 설계로의 수렴**: 2607.19770(펑처드 코드 기반 지연 적응형 텔레포테이션)과 2607.20391(교착상태 없는 프로세스망을 보장하는 안무형 프로그래밍 언어 Qoreo)은 모두 "이상적 조건"이 아닌 실제 네트워크 운영 제약(지연시간, 다자간 조율 복잡성)을 정면으로 설계에 반영한다는 공통점을 가지며, 양자 네트워크 스택이 물리 계층을 넘어 프로토콜·소프트웨어 계층에서도 성숙해지고 있음을 시사한다.

4. **양자 비밀공유의 통신 효율-보안 동시 최적화**: 2607.19891은 램프 양자 비밀공유의 중간집합 정보 누설 문제를 도청 탐지 메커니즘과 결합해 해결하고, 참여자 수에 따른 최적 통신비용 구간을 규명해 실용적 배치 지침을 제공했다.
