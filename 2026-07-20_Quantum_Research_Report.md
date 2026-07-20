# Quantum Research Report — 2026-07-20 (Monday)

> **수집 기준**: 2026-07-17 (금) arXiv quant-ph 신규 논문 (월요일 실행 규칙: 지난 금요일 자료)
> **생성일**: 2026-07-20 (월)
> **수집 논문 수**: 81편 (2026-07-17 announced) — Top 5 심층 분석 + 대표 19편 요약 (총 24편 수록)
> **우선순위 키워드**: Quantum Communication, QKD, Entanglement Distribution, Quantum Network, Quantum Teleportation

> **비고**: `export.arxiv.org/api/query`(주 수집 경로)를 WebFetch로 조회한 결과, submittedDate 기준 2026-07-16까지의 데이터만 반환되고 2026-07-17 제출분이 누락되는 기존 known issue가 재현되었다. CLAUDE.md 지침에 따라 `arxiv.org/list/quant-ph/recent` 대체 경로로 전환, 페이지네이션(`?skip=`)을 통해 announcement-date 기준 2026-07-17(금) 목록 전체 81편(신규 제출 + 교차등재 포함)을 확보해 이를 이번 리포트의 기준 데이터셋으로 사용했다. 우선순위 키워드 매칭 논문(5편, Top 5 전량)과 하드웨어·QEC·알고리즘·이론 전반을 아우르는 대표 논문 19편을 선별해 초록을 확인·요약했다. 나머지 57편은 리포트 하단에 제목만 수록한다.

---

## Top 5 심층 분석

### 1. Dynamic Entanglement Distribution for Multi-User and Multi-Protocol Quantum Networking
**arXiv**: [2607.15262](https://arxiv.org/abs/2607.15262)
**저자**: Rui Wang, Marcus J. Clark, Obada Alia, Sima Bahrani, Djeylan Aktas, Matej Peranić, Mario Stipčević, Martin Lončarić, John Rarity, Siddarth K. Joshi, Dimitra Simeonidou
**키워드**: Entanglement Distribution / Quantum Network (다중사용자·다중프로토콜 얽힘분배 네트워크)

#### 기술적 기여
양자 재구성형 광 애드-드롭 다중화기(q-ROADM)를 이용해 광대역 편광얽힘 광자쌍을 배포된 캠퍼스·대도시 광섬유망 위 6명의 사용자에게 동적으로 라우팅하는 시스템을 구현했다. 완전메시·부분메시·서브네트워크 슬라이싱 등 유연한 네트워크 구성을 지원하며, 6사용자 완전메시 구성에서 150시간 이상 연속 안정 운용을 실증했다. 보안 프로토콜과 다중경로 네트워크 플러딩을 결합한 안전한 사용자 온보딩까지 검증했다.

#### 의의
얽힘분배를 개별 링크 단위가 아닌 "서비스 지향형 재구성 가능 네트워크" 단위로 운용 가능함을 실증했다. 기존 광통신 인프라 위에서 링크 상태와 서비스 요구에 따라 얽힘자원을 동적으로 재배분하는 실용적 아키텍처를 제시했다.

#### 응용 가능성
- 다기관 양자네트워크의 서비스지향형 슬라이싱 운영
- 도시권 얽힘분배 인프라의 상용 광통신망 통합
- 다중 QKD·양자센싱 프로토콜의 동시 지원 플랫폼

---

### 2. High-rate continuous-variable quantum key distribution coexisting with Tb/s coherent classical transmission in hollow-core fiber
**arXiv**: [2607.14704](https://arxiv.org/abs/2607.14704)
**저자**: Xitao Ji, Siyu Chen, Peng Li, Mingming Zhang, Yilun Chen, Jun Gao, Rui Lin, Bacco Davide, Siqi Yan, Ming Tang
**키워드**: QKD (고속 CV-QKD·초고용량 고전전송 공존)

#### 기술적 기여
반사방지형 중공코어 광섬유와 잔류반송파 보조 이산변조 CV-QKD를 결합해, 39개 파장분할다중화 채널을 통한 7.6 Tb/s 고전데이터 전송과 동시에 153.22 Mb/s의 비밀키율을 달성했다. 24.3km 광링크에서 광필터링 없이도 고전신호 고출력 조건에서 양의 암호화율을 유지했다.

#### 의의
양자키분배와 초고용량 고전통신의 실질적 공존 가능성을 입증해, 별도 전용 광섬유 없이 기존 대용량 광통신망에 QKD를 직접 통합할 수 있는 경로를 제시했다.

#### 응용 가능성
- 상용 WDM 광통신망 내 CV-QKD 직접 통합
- 중공코어 광섬유 기반 차세대 양자보안 백본망
- 데이터센터 간 고용량 링크의 양자보안 강화

---

### 3. Emulation of Entanglement Distribution Networks on a Quantum Computer
**arXiv**: [2607.14260](https://arxiv.org/abs/2607.14260)
**저자**: Ashley N. Tittelbaugh, Jerry Horgan, Rohan Bali, Marco Ruffini, Daniel C. Kilper, Shelbi L. Jenkins, Boulat A. Bash
**키워드**: Entanglement Distribution / Quantum Teleportation (양자컴퓨터 상 얽힘분배 네트워크 에뮬레이션)

#### 기술적 기여
양자컴퓨터를 이용해 실제 하드웨어 제약(열화된 얽힘, 통신지연)이 텔레포테이션 기반 분산 다자간 얽힘상태 구성에 미치는 영향을 시뮬레이션했다. 불완전한 벨쌍 소스를 탈분극 잡음채널로, 통신지연을 열이완으로 모델링했으며, Stinespring dilation·무작위 파울리오류·준확률분해 세 가지 잡음구현 방식을 비교했다.

#### 의의
수학적으로 동등한 잡음모델이라도 실제 하드웨어 구현 방식에 따라 결과가 크게 달라질 수 있음을 밝혀, 양자네트워크 에뮬레이션 연구에서 엄밀한 실험적 방법론의 필요성을 강조했다.

#### 응용 가능성
- NISQ 컴퓨터를 활용한 양자네트워크 프로토콜 사전검증
- 텔레포테이션 기반 얽힘분배 프로토콜의 잡음 강건성 평가
- 양자중계기 네트워크 설계를 위한 저비용 에뮬레이션 플랫폼

---

### 4. Limits on Broadcasting Genuine Multipartite Entanglement in Quantum Networks
**arXiv**: [2607.14864](https://arxiv.org/abs/2607.14864)
**저자**: Pritam Roy, William John Munro, Shashank Gupta
**키워드**: Quantum Network / Entanglement Distribution (다자간 얽힘 브로드캐스팅의 근본적 한계)

#### 기술적 기여
N명의 당사자가 빔스플리터 상호작용을 이용한 최적 국소 1→2 복제를 수행하는 프로토콜로, GHZ·W·클러스터 상태의 브로드캐스팅 충실도 공식을 유도했다. 충실도는 시스템 크기에 따라 지수적으로 감소하며, 두 복제본이 표준 충실도 기반 검증체계 내에서 동시에 "진정한 다자간 얽힘"으로 인증될 수 없다는 근본적 장벽을 증명했다.

#### 의의
얽힘이 네트워크를 통해 쉽게 분배될수록 그 진정한 다자간 얽힘성을 검증하기는 더 어려워진다는 근본적 긴장관계를 규명해, 양자네트워크 얽힘분배의 이론적 한계를 명확히 했다.

#### 응용 가능성
- 다자간 얽힘분배 프로토콜의 검증 가능성 사전평가
- 양자네트워크 자원할당 시 브로드캐스팅 한계 반영
- 얽힘 인증 프로토콜의 새로운 검증 프레임워크 설계 기반

---

### 5. Adaptive Entanglement Management in Quantum Multi-Core Architectures
**arXiv**: [2607.14592](https://arxiv.org/abs/2607.14592)
**저자**: Rajeswari Suance P S, Anubhab Dutta, Ruchika Gupta, John Jose
**키워드**: Quantum Network / Quantum Teleportation (양자 Network-on-Chip 얽힘관리)

#### 기술적 기여
양자 Network-on-Chip으로 상호연결된 다중코어 프로세서에서 반응형·선제적·적응형 얽힘생성 세 방식을 비교하고, 코어 간 통신패턴을 관측해 얽힘생성 확률을 동적으로 조정하는 적응형 지속생성 방식을 제안했다. 메시기반 아키텍처 테스트에서 텔레포테이션 지연시간을 유의미하게 단축했으며, 배경 사전생성으로 인한 충실도 저하는 얽힘정제로 지연시간에 미미한 영향만 주며 복원했다.

#### 의의
칩 내부 양자네트워크에서도 트래픽 패턴 기반 적응형 자원관리가 통신효율을 크게 개선함을 보여, 대규모 양자컴퓨팅 시스템의 확장성 문제에 네트워크 공학적 해법을 제시했다.

#### 응용 가능성
- 대규모 다중코어 양자컴퓨터의 온칩 얽힘자원 스케줄링
- 텔레포테이션 기반 코어간 게이트 연산 지연 최소화
- 양자 NoC 아키텍처의 트래픽 적응형 얽힘정제 정책

---

## 추가 논문 요약 (19편)

| # | 제목 | arXiv ID | 주요 내용 | 분류 |
|---|------|----------|-----------|------|
| 6 | Superadditivity for Entanglement-Assisted Communication | [2607.15151](https://arxiv.org/abs/2607.15151) | 얽힘보조 채널정보량이 α∈[1/2,1) 전 구간에서 초가법적일 수 있음을 증명, 얽힘분리 채널에서도 신뢰도 향상 가능 | Quantum Communication·정보이론 |
| 7 | Locality of deep thermalisation through the lens of entanglement teleportation | [2607.15276](https://arxiv.org/abs/2607.15276) | 측정유도 얽힘텔레포테이션이 심층열화의 국소성을 제약, 일반 국소상호작용계에서는 로그스케일 국소성 창발 | Quantum Teleportation·다체물리 |
| 8 | Quantum Remote Implementation of Hybrid Operations on Hyperstates Using Hyperentangled States | [2607.14819](https://arxiv.org/abs/2607.14819) | 편광·공간 자유도를 동시 활용한 하이퍼얽힘자원으로 단일광자 2큐비트 하이퍼상태에 원격연산 구현 | Quantum Teleportation 인접·하이브리드 통신 |
| 9 | Syndrome-as-Header: A Quantum Label-Switching Architecture via Uncorrectable Error Injection | [2607.14484](https://arxiv.org/abs/2607.14484) | 오류정정 신드롬 구조에 라우팅 정보를 내장해 페이로드 측정 없이 양자 라벨스위칭 수행, NSFNet 벤치마크 검증 | Quantum Network·라우팅 |
| 10 | Local Variance-Based Calibration of Programmable Photonic Interferometer Meshes | [2607.14759](https://arxiv.org/abs/2607.14759) | 세기측정만으로 위상보정점을 찾는 분산최소화 교정법, 실리콘질화물 하드웨어에서 Clements 분해 검증 | 광자 양자통신 하드웨어 |
| 11 | LDGM-Based Quantum Codes for Fault-Tolerant Quantum Computation | [2607.15159](https://arxiv.org/abs/2607.15159) | 저밀도생성행렬 기반 CSS 코드로 유연한 양자율 설계, 이산화 밀도진화로 최적화된 메시지전달 디코딩 | 양자오류정정 |
| 12 | Quantum XYZ Stabilizer Codes | [2607.14988](https://arxiv.org/abs/2607.14988) | X·Y·Z 세 안정자를 모두 활용하는 비-CSS 코드 프레임워크 제안, XYZ² 육각코드 포함해 CSS qLDPC 대비 성능우위 실증 | 양자오류정정 |
| 13 | Towards logical entanglement creation in trivalent planar architectures | [2607.15044](https://arxiv.org/abs/2607.15044) | 3가 평면 큐비트망 격자수술로 큐비트·2큐비트게이트 자원을 O(d) 절감, 플럭소니움 실험조건서 최대 25% 충실도 개선 | 양자오류정정·하드웨어 |
| 14 | Collapse and Inversion of the Josephson Potential in a Strongly Driven Superconducting Circuit | [2607.14344](https://arxiv.org/abs/2607.14344) | 초고출력 마이크로파 구동 시 조셉슨 포텐셜이 0으로 붕괴 후 반전, 역진자형 동역학적 안정화 상태 실증 | 초전도큐비트 하드웨어 |
| 15 | Nonplanar qubit with tunable gauge symmetry | [2607.14229](https://arxiv.org/abs/2607.14229) | 3×3 크로스바 조셉슨배열 비평면 큐비트로 플럭스가변 Z₃ 조합게이지대칭 구현, 격자게이지이론 회로 QED 탐구 개시 | 초전도큐비트·게이지이론 |
| 16 | Towards a monolithic platform for coupling superconducting circuits to low-loss microwave phonons in AlScN on 4H-SiC | [2607.14319](https://arxiv.org/abs/2607.14319) | AlScN-4H-SiC 집적 압전플랫폼으로 알루미늄 공진기 2.9μs 결맞음시간, 포논수명 7.6μs·전기기계결합 4.3% 달성 | 초전도-포논 하이브리드 하드웨어 |
| 17 | Backpropagating Pauli Propagation | [2607.15184](https://arxiv.org/abs/2607.15184) | 파울리전파 시뮬레이션 기반 역전파 경사법으로 메모리를 O(n_param) 절감, 상태준비·시간전개압축 최적화에 적용 | 양자회로 시뮬레이션·최적화 |
| 18 | Efficient quantum algorithm for Heisenberg spin systems | [2607.14401](https://arxiv.org/abs/2607.14401) | Suzuki-Fisher 하이젠베르크 스핀계가 Lee-Yang 반경 1 텐서임을 증명, 스펙트럼 간극 하한으로 효율적 단열 바닥에너지 알고리즘 도출 | 양자알고리즘·다체물리 |
| 19 | Principles of Quantum Optimization for Constrained Problems | [2607.14227](https://arxiv.org/abs/2607.14227) | 제약조합최적화의 계산지연이 얽힘 재구조화에서 비롯됨을 통합 스펙트럼이론으로 규명, 제약인지형 동역학 설계 근거 제시 | 양자최적화 |
| 20 | Machine-Learning-Empowered Quantum Sensing of the Plaquette Phase in a Three-Level Delta System | [2607.15040](https://arxiv.org/abs/2607.15040) | STIRAP 전달효율 데이터로 다층퍼셉트론 학습, 3준위 델타계 게이지불변 플라켓위상 추정에 성공 | 양자센싱·머신러닝 |
| 21 | Real-Time Detection of Charge Jumps in Superconducting Qubits with a Convolutional Neural Network | [2607.14293](https://arxiv.org/abs/2607.14293) | 팽창인과 CNN을 FPGA에 배치해 방사선유도 전하점프를 마이크로초 지연으로 실시간 검출, 오프라인 알고리즘과 동등 성능 | 초전도큐비트·실시간 제어 |
| 22 | Benchmarking quantum simulation at scale | [2607.14212](https://arxiv.org/abs/2607.14212) | 안정자 스카 상태를 이용한 비평형 양자시뮬레이션 검증법 제안, 현실적 오류조건서 양자우위 벤치마크로 활용 가능성 제시 | 양자시뮬레이션 벤치마킹 |
| 23 | A Geometric Theory of Fermion-to-Qubit Encodings | [2607.14883](https://arxiv.org/abs/2607.14883) | Bravyi-Kitaev·Xia-Bian-Kais 인코딩을 가중 하이퍼그래프로 표현, 두 기하학적 보편성부류 규명 및 다중모형 적용 | 페르미온-큐비트 인코딩 이론 |
| 24 | A magnetic monopole in a superfluid bubble | [2607.15093](https://arxiv.org/abs/2607.15093) | 구형 초유체 껍질의 양자와류 역학이 단극자장 속 하전입자처럼 거동함을 실증, 목성극지 다각형 패턴과 유사한 적도와류목걸이 관측 | 양자유체·기초물리 |

---

## 미수록 논문 목록 (제목만, 57편)

*(초록 미확인, 리스트 순서 기준. 상세 분석이 필요할 경우 개별 요청 시 추가 조사 가능)*

2607.15252 Coulomb blockade in microscopic material defects as a source of decoherence and noise in solid-state quantum circuits, 2607.15210 Counterexamples to additivity of minimum output p-Rényi entropy of quantum channels for p>3/4 and 0≤p<1/4, 2607.15201 Entanglement Detection for Two-Qubit and Three-Qubit Pure States via Unitary Transformations and Ancilla State Measurements, 2607.15160 Parameter-Shift Rules for Gradients in Boson Sampling Experiments, 2607.15132 Periodic orbits and quantum many-body scars in integrable spin chains, 2607.15124 On the origin of finite entanglement scaling, 2607.15121 Quantum Lock-In Detection via Successive Adiabatic Evolution, 2607.15089 An experimental pathway towards an exact theory of strong coupling, 2607.15076 SQD-Enabled Circuit Compression for Resource-Efficient Quantum Chemistry, 2607.15030 Implicit differentiation of tensor network algorithms, 2607.14973 Pareto-optimal work extraction and the thermodynamic cost of precision in quantum information engines, 2607.14931 Strong O-valued contextuality: ruling out discrete nondeterministic alternatives to quantum theory, 2607.14920 A Three-Point Continuous-Variable Quantum MacWilliams Identity, 2607.14884 Evolution-Level Quantum Optimal Control of Single-Qubit Gates with Physics-Informed Neural Networks, 2607.14861 Binary Gauss Stabilizers for Abelian Lattice Gauge Theories, 2607.14797 Robustness of periodicity in Grover walks under a magnetic vector potential, 2607.14755 Moment Optimization in the Navascués-Pironio-Acín Hierarchy, 2607.14687 Electrons Hopping across a Molecular Network: Spectra and Symmetries, 2607.14663 Tuning the universality class of a quantum process by Trotterization, 2607.14650 Worst-Case Quantum Algorithm for Optimal Polynomial Intersection Beyond Decoded Quantum Interferometry, 2607.14629 Emergence and Recovery of (logical) Kochen-Specker Contextuality via Hamilton Extension, 2607.14583 Exact No Signaling in Time without Temporal Classicality, 2607.14569 No Finite NPA Level Characterizes the Complete Quantum Set in the Simplest Bell Scenario, 2607.14518 Structure-Aware Variational State Preparation for Quantum Basket Option Pricing, 2607.14501 Geometric Mode Steering of the Quantum Mpemba Effect, 2607.14477 A generalized variational quantum linear solver on photonic platform, 2607.14469 Perturbation Analysis of Maximal Quantum Leakage, 2607.14462 Quantum correlations of tripartite mixed states in the black hole quantum atmosphere, 2607.14441 Improving Dynamical Decoupling for Trapped-Ion QCCD Quantum Computers, 2607.14435 Imaginarity as a Resource within Quantum Coherence: Geometric Decomposition and Operational Conversion, 2607.14384 Circuit complexity lower bounds for quantum spin glasses, 2607.14376 State-independent uncertainty relations on multipartite spin 1/2-systems, 2607.14370 Unified monogamy and polygamy relations for multipartite systems, 2607.14311 General theory of monitored Quantum Reservoir Computing, 2607.14308 An end-to-end quantum algorithm for weakly nonlinear plasma physics with superquadratic speedup, 2607.14296 Disorder-enhanced compressibility of Floquet random quantum circuits, 2607.14282 Worldline-Susceptibility Scheduling for Quantum Annealing Beyond Local-Adiabatic Evolution, 2607.14239 Fock-state preparation based on amplitude amplification in cavity QED, 2607.14231 A Compass on the Quantum State Sphere: The Hopf Ansatz for Arbitrary Pure-State Optimization, 2607.14223 Quantum many-body mixed phase space revealed by hybrid feedback control, 2607.14222 Magic Without Entanglement: Exact Revivals and Their Fisher Information Origin, 2607.14217 Analytic gradients for low-rank quantum optimal control, 2607.14175 Transducer leakage error suppression using invariant-based shortcut, 2607.15169 Driven-dissipative superconductivity in moiré heterostructure without attraction, 2607.15158 Fast two-dimensional tensor-network contraction via subspace iteration, 2607.15086 Residual-Based Time Discretization on Nonlinear Approximation Manifolds: Analysis and Gaussian Applications, 2607.15070 Casimir effect for a massive scalar field confined between parallel plates with a spatially varying effective mass, 2607.14917 Star-triangle duality estimates for triangular and honeycomb permutation models, 2607.14874 Fermion-doubling problem in Chiral discretizations of Quantum field theory: Definitive proof, Fixing, and Computation of two-point correlation function, 2607.14567 Phase coherence control of a programmable high-Tc superconductor created by light, 2607.14558 Spin-Resolved Decay of Axion-Like Particles into Electron–Positron Pairs in Strong Electromagnetic Fields, 2607.14392 Unified Uncertainty Quantification Framework Bridging Noisy Quantum Backends Across Variational Quantum Algorithms and Quantum Signal Processing, 2607.14343 Quantum Markov Chains for an Asymmetric Mixed Ising-XY Model on a Cayley Tree, 2607.14284 Non-Hermitian Holographic Flows to Little Rip Cosmologies, 2607.14220 Non-perturbative saturation of Krylov complexity, and its implications in quantum gravity, 2607.14150 Tensor Network Methods for Advection-Diffusion-Reaction Systems Using Quantum-Inspired Representations, 2607.12015 Decoherence and More Coherence in the Radiative Decay of the Z Boson

---

## 트렌드 요약

### 이번 주 주요 동향

1. **얽힘분배 네트워크의 "운영 규모" 단계 진입**: 다중사용자·다중프로토콜 q-ROADM 기반 얽힘분배(2607.15262)가 6사용자 완전메시 구성으로 150시간 연속 운용을 실증하며, 실험실 소자검증을 넘어 실제 도시권 광섬유망 위에서의 서비스 운영 단계로 진입했음을 보였다.

2. **QKD와 초고용량 고전통신의 실질적 공존**: 중공코어 광섬유 기반 CV-QKD가 7.6 Tb/s 고전전송과 동시에 153 Mb/s급 비밀키율을 달성(2607.14704)하면서, QKD 상용화의 핵심 장벽이던 "고전-양자 신호 공존" 문제에 실질적 해법이 제시됐다.

3. **얽힘분배와 검증 가능성의 근본적 긴장**: 다자간 얽힘 브로드캐스팅의 충실도-검증 트레이드오프(2607.14864)와 텔레포테이션 기반 분산 얽힘구성의 하드웨어 의존성(2607.14260)이 같은 날 함께 등장해, 얽힘분배 네트워크의 "확장성"과 "검증 가능성"이 서로 상충하는 근본 제약임을 재확인했다.

4. **양자 네트워크 공학의 하위계층 정교화**: 온칩 다중코어 얽힘관리(2607.14592)와 신드롬기반 양자 라벨스위칭(2607.14484)은 각각 칩 내부와 광역망 라우팅 계층에서 양자네트워크를 "일반 통신망처럼 엔지니어링"하려는 흐름을 보여준다.

5. **양자오류정정의 부호구조 다변화**: LDGM 기반 CSS 코드(2607.15159), 비-CSS XYZ 안정자 코드(2607.14988), 3가 평면 격자수술 아키텍처(2607.15044)가 동시에 발표되며 오류정정 부호설계 공간의 탐색이 계속 확장되고 있다.

---

*Tags: #QuantumCommunication #QuantumNetwork #EntanglementDistribution #QKD #QuantumTeleportation #QuantumErrorCorrection #SuperconductingQubits #PhotonicQuantum #arXiv #quant-ph*
