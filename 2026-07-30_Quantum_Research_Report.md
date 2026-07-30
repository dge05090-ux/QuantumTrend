# Quantum Research Report — 2026-07-30 (Thursday)

> **수집 기준**: 2026-07-29 (수) arXiv quant-ph 신규 논문 (화~금요일 실행 규칙: 전날 자료)
> **생성일**: 2026-07-30 (목)
> **수집 논문 수**: 88편 (신규 제출 63편 + 교차등재 25편) — Top 5 심층 분석 + 대표 18편 요약 (총 23편 초록 확인), 나머지 65편은 제목 목록 수록
> **우선순위 키워드**: Quantum Communication, QKD, Entanglement Distribution, Quantum Network, Quantum Teleportation

> **비고**: `export.arxiv.org/api/query`(주 수집 경로)를 WebFetch로 조회한 결과 submittedDate 기준 2026-07-28까지의 데이터만 반환되는 기존 known issue가 재현되었다. CLAUDE.md 지침에 따라 `arxiv.org/list/quant-ph/recent?skip=0&show=100` 대체 경로로 전환, "Wed, 29 Jul 2026 (showing 88 of 88 entries)" 목록 전체(신규 63편 + 교차등재 25편)를 확보해 이를 이번 리포트의 기준 데이터셋으로 사용했다. 배치 조회(`id_list=...`)는 사용하지 않고 처음부터 개별 `arxiv.org/abs/<id>` 페이지를 병렬 WebFetch하여 초록을 수집했다. 이번 실행은 우선순위 키워드에 직접 매칭되는 논문이 7편 확보되어(제목 기준: Quantum Communication 2편, QKD 2편, Entanglement Distribution 2편, Quantum Network·Quantum Teleportation 각 2편, 일부 중복), Top 5 전체를 키워드 매칭 논문 중 실험적·이론적 기여가 가장 두드러진 5편으로 구성했다 — 특히 동일 연구그룹(중국과학기술대·조창 그룹으로 추정)이 청두(Chengdu) 중공심 광섬유(hollow-core fibre) 네트워크에서 텔레포테이션과 QKD를 각각 필드 실증한 두 편이 동시에 발표된 점이 특징적이다.

---

## Top 5 심층 분석

### 1. Quantum teleportation over a field-deployed hollow-core fibre network
**arXiv**: [2607.25352](https://arxiv.org/abs/2607.25352)
**저자**: Ri-Yao Song, Ya-Zhou Zhao, Yun-Ru Fan, Yang-Bin Ma, Yan-Yu Wei, Si Shen, Hao Li, Li-Xing You, Kai Guo, Guang-Can Guo, Qiang Zhou
**키워드**: Quantum Teleportation / Quantum Network

#### 기술적 기여
청두(Chengdu) 3개 지점을 잇는 실제 배치된 중공심(hollow-core) 광섬유 네트워크에서 양자 텔레포테이션을 실증했다. 중공심 광섬유의 약한 빛-물질 상호작용과 낮은 노이즈 특성을 활용해, 고전 데이터 트래픽과 공존하는 상황에서도 광자 큐비트의 상태 충실도를 유지하는 핵심 난제를 해결했다. 최대 160mW의 고전 신호 출력과 동시에도 견고한 텔레포테이션이 가능하며, 라만 노이즈는 표준 솔리드코어 광섬유 대비 약 3자릿수 낮게 측정되었고 별도의 능동 안정화 장치 없이도 광자 큐비트 품질을 유지했다.

#### 의의
실험실 데모를 넘어 실제 도시 인프라에 배치된 광섬유에서, 고전 통신과 양자 텔레포테이션이 동일 채널에서 공존 가능함을 보인 최초 사례 중 하나다. 중공심 광섬유가 기존 광통신 인프라와 양자 네트워크의 공존이라는 오랜 난제에 실질적 해법을 제시한다.

#### 응용 가능성
기존 광통신 인프라를 재활용한 도시 규모 양자 네트워크 구축, 고전-양자 하이브리드 채널 설계, 양자 인터넷 백본망의 실용적 배치 전략 수립에 직접 활용 가능하다.

---

### 2. Entanglement-based quantum key distribution with data in hollow-core fiber
**arXiv**: [2607.25331](https://arxiv.org/abs/2607.25331)
**저자**: Yue Luo, Sheng Liu, Yun-Ru Fan, Da-Wei Ge, Zhi-Yang Liu, Hao Li, Si Shen, Zi-Chang Zhang, Hai-Zhi Song, Li-Xing You, Tao Zhou, Kai Guo, Guang-Can Guo, Qiang Zhou
**키워드**: QKD / Quantum Network

#### 기술적 기여
18km 중공심 광섬유 링크에서 암호화 키와 고전 데이터를 동시 전송하는 얽힘 기반 QKD를 실증했다. 시간 인코딩 방식으로 이론적 데이터 용량 2.3Tbps를 확보하면서, 24시간 연속 운용 시 평균 10.56kbps의 비밀키 생성률을 달성했다. 저손실 광섬유 설계 적용 시 200km 이상 거리에서도 135kbps 이상의 성능이 가능할 것으로 전망했다.

#### 의의
1번 논문과 동일 연구그룹이 같은 중공심 광섬유 플랫폼으로 QKD를 실증한 자매 연구로, 하나의 물리적 인프라가 텔레포테이션과 QKD 양쪽 모두에 적용 가능함을 보여준다. 테라비트급 고전 데이터와 킬로비트급 양자 키가 동일 채널에서 장시간(24시간) 안정적으로 공존한다는 점에서 실용화 단계에 근접한 결과다.

#### 응용 가능성
기존 통신사업자 광섬유망을 활용한 QKD 상용 서비스 구축, 데이터센터 간 보안 통신과 암호키 분배의 단일 인프라 통합, 도시-광역 QKD 네트워크의 저손실 광섬유 로드맵 수립에 활용 가능하다.

---

### 3. Quantum Teleportation toward the Quantum Internet: A Concise Review
**arXiv**: [2607.25395](https://arxiv.org/abs/2607.25395)
**저자**: Yang-Bin Ma, Yun-Ru Fan, Ri-Yao Song, Ya-Zhou Zhao, Yi-Ye Liu, Si Shen, Zi-Hao Zhan, Yan-Yu Wei, Kai Guo, Guang-Can Guo, Qiang Zhou
**키워드**: Quantum Teleportation / Quantum Network

#### 기술적 기여
양자 텔레포테이션이 얽힘과 고전 통신을 결합해 미지의 양자 상태를 장거리 전송하는 원리를 정리하고, 다양한 물리 플랫폼(광자, 원자, 초전도 큐비트 등)에서의 실험적 구현 현황을 총망라했다. 양자 리피터 프로토콜을 중심으로 확장 가능한 양자 인터넷 인프라 구축의 과제와 방향을 제시했다.

#### 의의
1·2번 논문과 동일 연구그룹이 자신들의 실증 연구를 포함한 분야 전체를 조망하는 리뷰로, 양자 네트워크 구성요소로서의 텔레포테이션의 역할을 체계적으로 정리했다. 실험 그룹이 직접 작성한 리뷰라는 점에서 최신 필드 실증 결과들이 균형 있게 반영되어 있다.

#### 응용 가능성
양자 인터넷 연구 로드맵 수립을 위한 참고 자료, 신규 연구자의 온보딩 교육 자료, 양자 리피터 표준화 논의의 기술적 배경 문헌으로 활용 가능하다.

---

### 4. Co-transmission of classical data and continuous-variable entanglement over a single quantum channel
**arXiv**: [2607.25179](https://arxiv.org/abs/2607.25179)
**저자**: Nicholas Zaunders, Timothy C. Ralph
**키워드**: Quantum Communication / Entanglement Distribution

#### 기술적 기여
기존의 변위 기반 동시 양자-고전 통신(SQCC) 프로토콜은 얽힘 분배나 리피터 기반 QKD 같은 대부분의 양자 통신 방식과 호환되지 않는다는 근본적 한계를 지적하고, 고전 신호를 변조하는 방식으로 연속변수 가우시안 얽힘과 고전 정보를 동시에 분배할 수 있는 새로운 프로토콜을 제안했다. 분배된 얽힘 상태의 품질을 분석하고 리피터 기반 네트워크에의 적용 가능성, 그리고 점대점(point-to-point) 프로토콜 대비 비밀키 생성률을 계산했다.

#### 의의
동일 채널에서 얽힘 분배와 고전 데이터 전송을 양립시키는 이론적 틀을 제시함으로써, SQCC의 근본적 제약을 완화하고 리피터 기반 양자 네트워크와의 호환성을 확보한 점이 핵심 기여다.

#### 응용 가능성
고전-양자 공존 채널 기반 리피터 네트워크 설계, 연속변수 얽힘 분배 프로토콜의 실용적 확장, 통신사업자 인프라 재사용을 전제로 한 양자 네트워크 프로토콜 표준화에 참고 가능하다.

---

### 5. Remote entanglement of massive oscillators via wire-mediated Coulomb interaction
**arXiv**: [2607.25341](https://arxiv.org/abs/2607.25341)
**저자**: Lorenzo Papa, Onur Hosten, Carlos Gonzalez-Ballestero
**키워드**: Entanglement Distribution

#### 기술적 기여
대전된 거시적 역학 진동자 사이의 쿨롱 상호작용을, 인근에 배치한 도체 구조(전선)를 이용해 증폭하는 방법을 제안했다. 거시적 양자전기역학을 이용해 도체 내 영상전하(image charge)가 정전기적 상호작용의 거리 의존성을 자유공간의 1/D³에서 점근적으로 1/(D ln²D)로 완화시킴을 보였으며, 이 과정에서 저주파 진동자에 대한 추가 결어긋남은 무시할 만한 수준임을 확인했다. 연속 위치 측정과 결합해, 밀리그램급 진동자에서 자유공간 대비 한 자릿수 이상 먼 수백 마이크론 거리에서도 정상상태 운동 얽힘을 관측할 수 있을 것으로 예측했다.

#### 의의
거시적 물체 간 얽힘 분배의 근본적 제약인 거리에 따른 급격한 상호작용 감쇠 문제를, 도체를 매개로 한 새로운 메커니즘으로 완화한 참신한 접근이다. 순수 광학적 방법이 아닌 전기적 매개를 통한 원거리 얽힘 분배라는 점에서 기존 얽힘 분배 연구와 차별화된다.

#### 응용 가능성
거시적 양자 얽힘 실증 실험의 거리 한계 확장, 정밀 힘·가속도 센싱을 위한 얽힘 기반 진동자 네트워크 설계, 매크로스코픽 양자역학 검증 플랫폼 구축에 활용 가능하다.

---

## 추가 논문 요약 (18편)

| No. | arXiv ID | 제목 | 핵심 내용 | 분류 |
|-----|----------|------|-----------|------|
| 1 | 2607.24855 | Information-theoretic limits on undetectable parameter-estimation attacks in continuous-variable quantum key distribution | 가우시안 CV-QKD 위조 인증서의 탐지 가능성을 정보이론적으로 분석, Stein 지수 기반 유한크기 보안 한계 제시 | QKD 보안 |
| 2 | 2607.25702 | Benchmarking Optical Receivers for Quantum Communication and Randomness Certification | 연속변수·광자계수·하이브리드 수신기의 반-기기독립적 무작위성 인증 성능 비교 분석 | 양자통신 장치 |
| 3 | 2607.25865 | OmniQEC: discovering practical quantum error-correcting codes by an AI scientist | LLM 기반 자기진화 추론 워크플로로 QEC 부호 자동 발굴, 벤치마크 부호 대비 논리오류 억제 개선 | 양자오류정정/AI |
| 4 | 2607.25834 | Lowering the implementation barrier of neutral-atom quantum computing with agentic workflows | 에이전트 워크플로로 이론 연구를 중성원자 QPU 실행으로 자동 변환, 633편 논문 실행가능성 분석 포함 | 양자하드웨어/AI |
| 5 | 2607.25941 | Sampling hard circuits with verifiably high fidelity | 하드니스 보장과 오류정정을 결합한 구조화 회로, 70큐비트 실험서 신뢰도 하한 0.284(95% 신뢰수준) 달성 | 양자컴퓨팅 벤치마크 |
| 6 | 2607.24907 | Fault-tolerant distributed quantum computing with a single nucleus per node | 노드당 단일 핵스핀만으로 결함허용 분산양자컴퓨팅 구현, 통신오류를 측정오류로 변환해 자원요구량 대폭 축소 | 분산양자컴퓨팅 |
| 7 | 2607.24968 | Universal Optimization and Tighter Fidelity Bounds for Approximate Quantum Error Correction | 근사양자오류정정 최적화에 PCA 기반 차원축소 적용, 33배 속도 향상과 더 타이트한 충실도 하한 동시 달성 | 양자오류정정 |
| 8 | 2607.25109 | Exceptional-point braiding with native controls | 실험적으로 접근 가능한 제어만으로 예외점 브레이딩 구현, 분산 트랜스몬 실험 조건에서 검증 | 비에르미시안 물리 |
| 9 | 2607.25812 | Optimal Quantum Eigenvalue Transformation via Linear Combinations of Hermitian Matrices | 에르미트 행렬 선형결합 기반 비정규 행렬 고유값 변환, Θ(d) 최적 회로깊이와 거의 최적 게이트 수 달성 | 양자알고리즘 |
| 10 | 2607.25795 | Efficient Lindbladian Learning from Constant-Time Pauli Responses | 국소 파울리 응답을 선형방정식으로 취급해 개방양자계의 결맞음·소산 성분을 분리 학습하는 두 알고리즘 제시 | 양자시스템 특성분석 |
| 11 | 2607.25306 | Loss-induced anomalous generalized bunching in multiphoton interference | 손실과 광자 생존 조건이 결합될 때 나타나는 일반화된 광자 뭉침의 비단조 이상현상을 3광자 간섭계에서 규명 | 양자광학 |
| 12 | 2607.25145 | Agentic AI for Scientific Reasoning in Autonomous Quantum Sensing Experiments | NV센터 자율 실험을 수행하는 LLM 에이전트 워크플로, T2* 측정 및 탄소-13 상호작용 조사 실증 | 양자센싱/AI |
| 13 | 2607.24992 | A Model Predictive Control-Inspired Quantum Algorithm | 모델예측제어 기법을 결합한 하이브리드 양자-고전 알고리즘, 레이어별 되먹임 최적화로 FQA 이상 성능 보장 | 양자알고리즘 |
| 14 | 2607.25062 | A broadband, individually addressing two- and three-dimensional photonic integrated circuit for trapped-ion qubit control | 405~880nm 파장 대역 개별 이온 주소지정 온칩 광집적회로, 칼슘·바륨 이온 실증 | 이온트랩 하드웨어 |
| 15 | 2607.24946 | Numerical Modeling of Quasiparticle-Induced Dissipation in Fluxonium Qubits | 방사선 유발 준입자가 플럭소니움 큐비트의 "보호된" 바이어스 지점에도 민감하게 작용함을 수치 시뮬레이션으로 규명 | 초전도큐비트 |
| 16 | 2607.25501 | Automated discovery of high-probability heralded schemes for path-entangled states | AI 기반 선형광학 헤럴드 구성 자동 발굴, 기존 설계를 포함하며 지수적으로 개선된 확장 가능 패밀리 제시 | 양자광학/AI |
| 17 | 2607.25704 | Verifiable blind probabilistic error cancellation | 완전 악의적 적대자에도 안전한 최초의 검증가능 양자오류완화(QEM) 프로토콜 VBPEC 제시 | 양자오류완화/보안 |
| 18 | 2607.24851 | Unitary designs from perturbed time evolutions of a chaotic Hamiltonian | 단일 카오스 해밀토니안의 시간전개와 중간 유니터리 섭동을 결합해 유니터리 디자인을 생성하는 프로토콜 | 양자무작위성 |

---

## 나머지 논문 목록 (제목만 수록, 65편)

| arXiv ID | 제목 |
|----------|------|
| 2607.26029 | Path integral approach to the truncated Wigner approximation of driven-dissipative spins |
| 2607.25998 | Observable Estimation in the Absence of Classical Verification |
| 2607.25954 | Equi-Entropic Maps for Four-Partite Quantum States |
| 2607.25900 | Effect-valued measurement models and contextuality |
| 2607.25899 | Consistent Quantum States over Spacetime without a Common Quantum Process |
| 2607.25838 | Bipartite Bound Information Exists |
| 2607.25805 | On some potentials based on exponential functions |
| 2607.25779 | Exponential de Finetti Theorems for Fermionic Gaussian States |
| 2607.25746 | Classically Augmented Zero-Noise Extrapolation |
| 2607.25699 | Counterfactual Quantum Sensing: What Interaction-Free Measurement Can and Cannot Buy |
| 2607.25684 | Landau Levels on the Surface of a Cube |
| 2607.25678 | Engineering a Quantum Thermal Diode with Floquet Driving |
| 2607.25661 | Discrete power-law decay of subsystem distance after a quantum quench |
| 2607.25643 | Nonlocal Magnonic Cat States in Hybrid Magnon-Qubit Architectures |
| 2607.25638 | Coherent control of subradiant excitations in atomic rings |
| 2607.25627 | Theory of Cubic-Phase Dynamics in the Linear Potential |
| 2607.25561 | Interaction-Endowed PT-Symmetry and its Effects on Decoherence, Einselection, and Non-Markovianity in a Central Spin Model |
| 2607.25547 | Collective states of multi-level emitters: The role of multi-level interferences |
| 2607.25496 | Asymmetric information scrambling and eigenstate thermalization in inhomogeneous XXZ spin chains |
| 2607.25427 | A General First- and Second-Order Numerical Solver for Non-Markovian Quantum State Diffusion |
| 2607.25345 | Detecting quantum phase transitions via shallow variational quantum circuits |
| 2607.25307 | Actualization, Records, and the Emergence of Entropic Time |
| 2607.25176 | Dissipation Enables Strongly Detuning-Dependent Interference in Pulsed Dynamical Decoupling |
| 2607.25170 | QUBO-Based Optimization of Social Indicator Configurations for Working-Age Population Growth |
| 2607.25162 | Quantum Transformer BSDE Solver via Multi-Layer Fully-Connected Variational Quantum Circuits |
| 2607.25101 | Covariant Quantum Measurements and Stochastic Dynamics on Representation Space |
| 2607.25005 | Invariant-based master equation applied to driven qutrit coupled to a bath and a leaky cavity |
| 2607.24988 | Maximal complementarity in the n-qubit Pauli group |
| 2607.24987 | An algebraically closed family of informational n-qubit purity invariants |
| 2607.24976 | Quantum reference frames beyond subsystems: a reconstruction and generalization of the perspective-neutral framework |
| 2607.24972 | A Kernel-Based Density of States Estimator for Quantum Computing |
| 2607.24961 | Non-Hermitian entropy production from fluctuation theorems |
| 2607.24947 | Realizing Error Suppression in Partially Fault-Tolerant Quantum Simulations with IBM Quantum Computers |
| 2607.24937 | Resolving Structure in Prethermal Floquet Dynamics with Precision Quantum Computation |
| 2607.24924 | Efficient computation of real-time correlators using Pauli Propagation |
| 2607.24858 | Topology-dependent relativistic degradation of multipartite entanglement |
| 2607.24853 | Wave-functional formulation of dissipative CSL models |
| 2607.24842 | Closed-Form Expectation Values of the Damped Kerr Oscillator |
| 2607.24837 | A Difference Operator Approach to Quantum Random Walks: Parseval Identity, Krawtchouk Matrices, and Hermite Limits |
| 2607.24836 | Can a quantum circuit detect the Unruh effect? |
| 2607.26028 | A Spectral Proof of the Hypergraph Moore Bound |
| 2607.26019 | Predicting the Slow Drift of Nuclear Spin Noise in Semiconductor Spin Qubits |
| 2607.26011 | Krylov-Space Memory Cores |
| 2607.25969 | Solvable Quantum Circuits with non-Markovian Influence Matrices |
| 2607.25938 | Interacting hydrodynamic modes in spinless fermions with dephasing noise |
| 2607.25833 | Curved momentum space and finite Landau spectrum in κ-Minkowski spacetime |
| 2607.25783 | Deterministic loading of molecular arrays by microwave-assisted collisions |
| 2607.25777 | Tunable state-dependent interactions in collisionally stable mixtures of polar molecules |
| 2607.25774 | Ro-vibrational van der Waals interaction between ultracold polar molecules |
| 2607.25647 | KQFuzz: Knowledge-Guided Fuzzing for Quantum Libraries via Large Language Models |
| 2607.25625 | Entanglement asymmetry in the gapped XYZ spin-½ chain |
| 2607.25445 | Quantum estimates for classical polynomial optimization |
| 2607.25437 | Repositories, Contributors, and Continuity: An Empirical Study of Foundational Quantum Software |
| 2607.25434 | Don't truncate, decompose: mean-field dynamics of long-range quantum systems from strongly correlated states |
| 2607.25358 | QCOEM: Quantum Cloud Orchestration with Evolutionary Multi-Objective Optimization |
| 2607.25267 | Tuning Density and Spin Ordering of Degenerate Fermi Gases in an Optical Cavity |
| 2607.25256 | Anomalous entanglement scaling from eigenvector nonorthogonality in critical non-Hermitian free fermions |
| 2607.25245 | Structured High-Angular-Momentum Coulomb Tensors from Real and Complex Solid-Harmonic Integral Engines: A Perspective |
| 2607.25034 | Quantum detection of CP violation in the tt̄ system: tomography |
| 2607.25029 | Quantum detection of CP violation in the tt̄ system: production |
| 2607.24967 | Spin-cQED with bulk germanium spin qubits |
| 2607.24925 | Effective Field Theory of Operator Scrambling from Strong-to-Weak Symmetry Breaking |
| 2607.24906 | Probing nonlocal superconducting fluctuations with covariance noise magnetometry |
| 2607.24807 | A Path Integral Model of Cognition |
| 2509.03588 | Dissociation of bulk and entanglement phase transitions in the Haldane phase |

---

## 트렌드 분석

### 2026-07-29 주요 트렌드

1. **동일 그룹의 중공심 광섬유 필드 실증이 텔레포테이션·QKD 양쪽에서 동시 발표**: 2607.25352(텔레포테이션)와 2607.25331(QKD)이 같은 청두 중공심 광섬유 인프라를 사용해 각각 실증되었으며, 리뷰 논문(2607.25395)까지 함께 게재되어 한 그룹의 연구 성과가 한 번에 집중적으로 공개된 흐름을 보였다. 고전 트래픽과의 공존이라는 실용적 난제를 정면으로 다룬 점이 공통적이다.

2. **에이전틱 AI가 양자 연구 전 영역에 걸쳐 확산**: QEC 부호 발굴(2607.25865), 중성원자 QC 실행 자동화(2607.25834), 자율 양자 센싱 실험(2607.25145), 헤럴드 얽힘 상태 설계 자동 발굴(2607.25501)까지 4편의 논문이 LLM 기반 에이전트를 연구 워크플로에 직접 통합했다. 특히 2607.25834는 에이전트가 두 차례 결정적 오류를 범했고 인간 전문가 검증이 필수적이었음을 명시해, 자동화 확산과 동시에 그 한계도 함께 보고되는 추세다.

3. **얽힘 분배의 물리적 매개체 다변화**: 2607.25341은 광학적 방법이 아닌 도체 매개 쿨롱 상호작용으로 거시적 진동자 간 원거리 얽힘을 실현하는 새로운 메커니즘을 제안했으며, 2607.25179는 고전-양자 공존 채널에서의 연속변수 얽힘 분배 이론을 정교화했다. 얽힘 분배 연구가 광자 기반을 넘어 다양한 물리 플랫폼으로 확장되고 있음을 보여준다.

4. **양자 오류정정·완화 기법의 다각적 심화**: 근사 QEC 최적화(2607.24968), 검증 가능한 블라인드 오류완화(2607.25704), 노드당 단일 핵스핀 기반 결함허용 분산양자컴퓨팅(2607.24907)이 동시에 발표되며, 오류정정 연구가 이론적 최적화·보안·분산 아키텍처 등 다방면으로 세분화되고 있다.

5. **CV-QKD 보안의 정보이론적 정교화**: 2607.24855는 연속변수 QKD의 위조 인증서 공격에 대한 탐지 가능성을 Stein 지수 기반으로 정량화해, 실용적 CV-QKD 배치에 필요한 composable 보안 보장을 강화했다.

### 우선 키워드 관련 논문 현황 (2026-07-29 공지 기준)

| 키워드 | 관련 논문 수 | 주요 논문 |
|--------|------------|----------|
| Quantum Communication | 2편 | 2607.25702, 2607.25179 |
| QKD | 2편 | 2607.25331, 2607.24855 |
| Entanglement Distribution | 2편 | 2607.25341, 2607.25179 |
| Quantum Network | 2편 | 2607.25395, 2607.25352 |
| Quantum Teleportation | 2편 | 2607.25395, 2607.25352 |

---

*본 보고서는 Claude Code의 WebFetch 도구를 이용하여 2026-07-30(목)에 생성되었습니다. 조회 시점 기준 arXiv 최신 공지 배치가 2026-07-29(수) 제출분으로 확인되어 해당 배치를 수집·분석하였습니다.*
