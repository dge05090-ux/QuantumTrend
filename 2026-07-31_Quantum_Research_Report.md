# Quantum Research Report — 2026-07-31 (Friday)

> **수집 기준**: 2026-07-30 (목) arXiv quant-ph 신규 논문 (화~금요일 실행 규칙: 전날 자료)
> **생성일**: 2026-07-31 (금)
> **수집 논문 수**: 84편 (신규 제출 73편 + 교차등재 11편) — Top 5 심층 분석 + 대표 18편 요약 (총 23편 초록 확인), 나머지 61편은 제목 목록 수록
> **우선순위 키워드**: Quantum Communication, QKD, Entanglement Distribution, Quantum Network, Quantum Teleportation

> **비고**: `export.arxiv.org/api/query`(주 수집 경로)를 WebFetch로 조회한 결과 submittedDate 기준 2026-07-29까지의 데이터만 반환되는 기존 known issue가 재현되었다. CLAUDE.md 지침에 따라 `arxiv.org/list/quant-ph/recent?skip=0&show=100` 대체 경로로 전환, "Thu, 30 Jul 2026 (showing 84 of 84 entries)" 목록 전체(신규 73편 + 교차등재 11편)를 확보해 이를 이번 리포트의 기준 데이터셋으로 사용했다. 배치 조회(`id_list=...`)는 사용하지 않고 처음부터 개별 `arxiv.org/abs/<id>` 페이지를 병렬 WebFetch하여 초록을 수집했다. 이번 실행은 우선순위 키워드에 직접 매칭되는 논문이 5편 확보되어(QKD 3편, Quantum Communication 1편, Quantum Network 1편), Top 5 전체를 키워드 매칭 논문으로 구성했다 — 특히 QKD 관련 논문 3편이 동시에 발표되어 QKD 보안 이론·프로토콜 통합 연구가 이번 배치의 뚜렷한 축을 이뤘다.

---

## Top 5 심층 분석

### 1. Enhancing the security of coherent one-way quantum key distribution using CHSH correlations
**arXiv**: [2607.26856](https://arxiv.org/abs/2607.26856)
**저자**: Mahdi Shaban, Farnaz Farman, Alireza Bahrampour
**키워드**: QKD

#### 기술적 기여
상용화된 QKD 프로토콜인 coherent one-way(COW)는 최근 공격으로 안전 전송 거리가 20km 미만으로 제한된다는 문제가 지적되어 왔다. 이 논문은 COW의 보안 검증 방식을 기존의 결맞음(coherence) 모니터링에서 벨 부등식(CHSH) 위반 여부를 추적하는 방식으로 전환해, 더 넓은 범위의 공격을 탐지할 수 있도록 프로토콜을 수정했다. 시뮬레이션 결과 이 접근으로 최대 안전 전송 거리를 약 259km까지 확장할 수 있음을 보였다.

#### 의의
상용 COW-QKD 시스템의 실질적 보안 취약점을 CHSH 상관관계라는 양자 비국소성 검증 도구로 해결한 점에서, 이론과 실용화 사이의 간극을 직접 메운 연구다. 안전 거리를 10배 이상 확장했다는 점은 기존 배치된 인프라의 수명을 크게 늘릴 수 있는 실질적 성과다.

#### 응용 가능성
기존 COW-QKD 상용 장비의 펌웨어/프로토콜 업그레이드를 통한 보안 강화, 장거리 도시간 QKD 백본망 설계, 벨 비국소성 기반 보안 검증을 다른 QKD 프로토콜에 이식하는 후속 연구에 활용 가능하다.

---

### 2. Enforcing IID structure on time-bin encoded QKD protocols via coarse-graining
**arXiv**: [2607.26772](https://arxiv.org/abs/2607.26772)
**저자**: Shlok Nahar, Shihong Pan, Norbert Lütkenhaus
**키워드**: QKD

#### 기술적 기여
많은 QKD 보안 증명은 수신자(Bob)의 측정이 각 라운드에서 텐서곱 구조, 나아가 독립동일분포(IID) 조건을 만족할 것을 요구한다. 그러나 시간 인코딩(time-bin) 프로토콜은 인접 라운드 간 광 모드 간섭에 의존하는 간섭계를 사용하기 때문에 이 조건을 직접 만족시키기 어렵다. 연구진은 라운드 간 결맞음에 민감한 검출기 결과를 제거하는 고전적 후처리만으로 IID 조건을 만족하는 POVM 구조를 복원할 수 있음을 증명했다. 이를 Mach-Zehnder 간섭계 및 IID 버전 COW 검출 구조에 적용해, 기존 연구에서 필요했던 추가 진공 펄스 없이도 더 높은 키 생성률을 달성했다.

#### 의의
Lütkenhaus 그룹(QKD 보안증명 분야의 대표 그룹)이 시간 인코딩 프로토콜의 오랜 이론적 난제였던 IID 조건 미충족 문제를 순수 고전 후처리로 해결한 점에서, 보안 증명과 실제 하드웨어 구현 사이의 괴리를 좁힌 기초 이론 연구다.

#### 응용 가능성
시간 인코딩 기반 QKD 시스템(COW, DPS 등)의 키 생성률 개선, 진공 펄스 등 추가 하드웨어 없이 기존 보안 증명 프레임워크를 적용하는 실장비 최적화, QKD 보안 증명 표준화 작업의 기술적 근거로 활용 가능하다.

---

### 3. Reconfigurable Optical Platform for One-way Quantum Communication Complexity
**arXiv**: [2607.27181](https://arxiv.org/abs/2607.27181)
**저자**: Francesco Mazzoncini, Hugo Defienne, Romain Alléaume, et al.
**키워드**: Quantum Communication

#### 기술적 기여
다중모드 광섬유와 파면 정형(wavefront shaping) 기술을 이용해, 지수적 양자-고전 통신 격차가 알려진 일방향(one-way) 양자 통신 복잡도 문제를 실험적으로 구현하는 재구성 가능한 광학 플랫폼을 제시했다. 실험과 시뮬레이션을 통해 이 아키텍처가 추가 하드웨어 없이도 다른 통신 과제로 확장 가능하며, 고차원 구현 또한 가능함을 보였다.

#### 의의
양자 통신 복잡도라는 이론적으로 잘 정립된 양자 우위 영역을, 재구성 가능한 단일 광학 플랫폼으로 실증 가능하게 만든 점이 핵심이다. 특정 프로토콜 전용 하드웨어가 아닌 범용 플랫폼이라는 점에서 후속 프로토콜 실증의 진입장벽을 낮춘다.

#### 응용 가능성
양자 우위 실증 실험 플랫폼의 범용화, 통신 복잡도 이외의 다양한 양자 정보처리 과제로의 플랫폼 재활용, 다중모드 광섬유 기반 양자 통신 장비의 상용화 가능성 탐색에 활용된다.

---

### 4. Optimization of C-band quantum traffic coexisting with O-band classical traffic: preliminary results
**arXiv**: [2607.26905](https://arxiv.org/abs/2607.26905)
**저자**: Laura d'Avossa, Elena Montella, Marco Grillo, et al.
**키워드**: Quantum Network

#### 기술적 기여
양자 신호와 고전 신호가 동일 광섬유 인프라를 공유할 때 핵심 잡음원인 자발 라만 산란(spontaneous Raman scattering)을 상용 광트랜시버와 표준 광섬유를 이용해 실험적으로 분석했다. 광원 종류에 무관하게 라만 산란 프로파일을 예측할 수 있는 소형·범용 모델을 개발해, C-band 양자 채널 중 O-band 고전 트래픽과의 간섭이 최소화되는 최적 채널을 결정할 수 있도록 했다.

#### 의의
기존 도시 광섬유망을 그대로 활용하는 실용적 양자 네트워크 배치를 위한 채널 선정 방법론을 제시했다는 점에서, 실험실 수준 실증을 넘어 통신사업자 인프라 재사용이라는 실질적 배치 문제를 다뤘다.

#### 응용 가능성
기존 도시 광통신망에서의 QKD/양자통신 채널 공존 설계, 통신사업자와의 협력을 통한 상용 양자 네트워크 구축 로드맵 수립, 다양한 광원에 범용 적용 가능한 라만 잡음 예측 도구의 실장비 통합에 활용 가능하다.

---

### 5. QKD-Integrated Quantum Noise Stream Cipher: An Overview
**arXiv**: [2607.26550](https://arxiv.org/abs/2607.26550)
**저자**: Umesh Kumar Chandra, Avinash Kote, Neha Pathania, et al.
**키워드**: QKD

#### 기술적 기여
양자 잡음과 비직교 코히런트 상태 변조를 이용한 물리계층 암호화 기술인 Quantum Noise Stream Cipher(QNSC)와, 정보이론적으로 안전한 키 교환을 제공하는 QKD를 결합하는 통합 시스템을 리뷰했다. QKD가 QNSC에 지속적으로 신선한 암호키를 공급하는 구조를 제안하고, 동작 원리·다양한 공격 시나리오에 대한 보안 분석·실험적 진전 상황을 종합했다.

#### 의의
QNSC의 씨앗 키 관리 취약점을 QKD로 보완하는 결합형 접근을 체계적으로 정리한 리뷰로, 물리계층 암호화와 양자 키 분배라는 서로 다른 두 보안 기술의 상호보완 관계를 명확히 했다.

#### 응용 가능성
완전 양자 보안 광통신망의 대규모 상용 배치 전략 수립, QNSC-QKD 통합 시스템의 실장비 설계 참고자료, 물리계층-키분배 계층을 아우르는 통신 보안 표준화 논의에 활용 가능하다.

---

## 추가 논문 요약 (18편)

| No. | arXiv ID | 제목 | 핵심 내용 | 분류 |
|-----|----------|------|-----------|------|
| 1 | 2607.27204 | Fault-Tolerant Logical Operations and Efficient State Preparation in Modular Quantum Architectures with Noisy Interfaces | 모듈 간 인터페이스가 모듈 내부보다 한 자릿수 높은 노이즈를 견딜 수 있음을 회로수준 시뮬레이션으로 증명, 분산 GHZ 상태 준비를 vertex-cover 문제로 환원해 다항시간 휴리스틱 제시 | 분산양자컴퓨팅/QEC |
| 2 | 2607.27195 | Very Strong Irreversibility of Quantum Entanglement | 순수 얽힘 없이는 생성 불가하지만 순수 얽힘을 전혀 산출하지 못하는 혼합 얽힘 상태 존재를 증명, Lami-Regula 추측 해결 | 양자정보이론 |
| 3 | 2607.27171 | OQRAM: Oblivious Quantum Random Access Memory for Securing Delegated Quantum Queries | 암호화·셔플된 데이터베이스와 코히런트 주소 마스킹으로 위임 양자 컴퓨팅의 프라이버시를 보호하는 프레임워크, 완전 블라인드 양자컴퓨팅 대비 자원 소모 대폭 절감 | 양자암호/위임컴퓨팅 |
| 4 | 2607.27144 | Parity-Based Time-Bin Encoding Enabling SWAP Between Polarization and Time-Bin Qubits | 짝수/홀수 시간 간격으로 논리상태를 인코딩해 편광-시간빈 큐비트 간 결정론적 교환을 구현하는 새 인코딩 방식 제안 | 광양자정보 |
| 5 | 2607.27123 | Hardware-efficient erasure-error detection with an integer fluxonium | 단일 정수 플럭소니움 큐비트로 추가 큐비트 없이 소거오류 검출, 상태수명 8.4배·결맞음시간 1.38배 향상 | 초전도큐비트/QEC |
| 6 | 2607.27094 | Native CCZ Gate with Fluxonium Qubits and a Microwave-Driven Coupler | 플럭소니움 3큐비트 프로세서에서 99.39% 충실도의 네이티브 CCZ(토폴리 등가) 게이트를 65ns에 구현 | 초전도큐비트 |
| 7 | 2607.27015 | Reliability Functions of Quantum Soft Covering and Privacy Amplification via a Mixed-Order Rényi Divergence | 혼합차수 Rényi 발산을 도입해 양자 소프트 커버링과 프라이버시 증폭의 신뢰도 함수를 최초로 정확히 특성화 | 양자정보이론 |
| 8 | 2607.27013 | Finite size scaling of bitstring probability distributions for Rydberg arrays | Rydberg 사다리 시스템의 비트스트링 확률분포가 시스템 크기 증가에 따라 페르미함수 형태로 수렴, 진공 관측량 계산의 지수적 샷 수 증가 규명 | 리드버그원자/양자시뮬레이션 |
| 9 | 2607.27009 | Embedded quantum computing for many-body surface reaction | 양자컴퓨팅+밀도범함수 임베딩(QC-DFET)으로 구리 표면 촉매 반응(수소해리·CO흡착·포름산 수소화) 3종을 Zuchongzhi 프로세서로 검증 | 양자화학시뮬레이션 |
| 10 | 2607.26957 | Two-photon interference from as-grown InAsP/InP quantum dots under detuned excitation | 32meV 비공진 여기로 산란광 억제, 통신대역 단일광자원의 광자 비구별성 검증(HOM 가시성 0.09~0.11) | 양자광학/단일광자원 |
| 11 | 2607.26745 | High-fidelity multiqubit gates with Rydberg atoms via level-crossing-free Rapid adiabatic passage | 레벨교차 없는 급단열통과로 Bell·3큐비트 W·4큐비트 GHZ·6큐비트 벌집 W 상태를 0.9997 이상 충실도로 생성 | 리드버그원자/얽힘생성 |
| 12 | 2607.26477 | Finding diagonal logical gates in CSS codes and circuits | CSS 부호에서 transversal·국소성보존·folding 게이트로 구현 가능한 모든 대각 논리게이트를 탐색하는 O(n³) 알고리즘 제시 | 양자오류정정 |
| 13 | 2607.26293 | Optimal Interaction Free Localization with Multipath Interferometers | d-경로 간섭계 기반 3단계 프로토콜로 다중 후보 위치 동시 탐색, 순차스캔·밝은포트재활용·제논간섭을 단일 최적화 틀로 통합 | 양자광학/상호작용없는측정 |
| 14 | 2607.26242 | Precise 2D electric field density simulations for superconducting quantum devices | 경계적분방정식 솔버로 초전도 큐비트 유전손실 시뮬레이션을 2자릿수 가속(오차 10⁻⁷), 금속-공기 계면과 측벽의 손실 민감도 규명 | 초전도큐비트/시뮬레이션 |
| 15 | 2607.26161 | A two-dimensional piezo-optomechanical transducer | 밴드구조 엔지니어링 기반 2차원 압전-광기계 변환기, 10mK에서 강한 전기기계 결합과 0.85% 내부효율 달성, 원거리 초전도 프로세서 연결용 | 양자변환기/분산컴퓨팅 |
| 16 | 2607.26154 | Graph Theoretic Approach to Quantum Nonstabilizerness | 제한된 파울리 측정만으로 매직(nonstabilizerness) 검출, 프러스트레이션 그래프의 클리크 수와 검출 능력의 관계 규명 | 양자자원이론 |
| 17 | 2607.26131 | Neural quantum states for non-Abelian lattice gauge theories with dynamical fermions | 신경망 파동함수+게이지공변 페르미온 보정으로 동적 페르미온이 결합된 SU(2) 격자게이지이론의 바닥상태 탐색, sign-problem-free | 양자시뮬레이션/격자게이지이론 |
| 18 | 2607.26086 | Malleability of transformations on the ciphertext in noisy Quantum public key encryption | Malavolta-Walter 양자공개키암호에 잡음을 도입해 위조가능성(malleability)을 분석, Gentle Measurement Lemma로 trace distance 상한 도출 | 양자암호이론 |

---

## 나머지 논문 목록 (제목만 수록, 61편)

| arXiv ID | 제목 |
|----------|------|
| 2607.27206 | Practical Quantum Topological Data Analysis with Applications to High-Dimensional Feature Extraction and Time Series Analysis |
| 2607.27185 | Sharp Bounds on Ground State Energy of the SYK Model |
| 2607.27184 | Robust quantum state certification and uncertainty principles for total influence |
| 2607.27173 | Classical and Quantum MacWilliams Transforms as Spin Kinematics |
| 2607.27168 | Training Quantum Dragons |
| 2607.27153 | Improved Methods for Determining Quantum Error Correcting Code Performance and Fault Tolerance |
| 2607.27117 | The Keyl-Werner algorithm is not optimal for spectrum estimation |
| 2607.27116 | Ky Fan majorization for binary tensor products |
| 2607.27111 | Effective Hamiltonians for Predictive Quantum Control |
| 2607.27075 | Adaptive Multi-Backend Simulation of Near-Clifford Quantum Circuits via Spatial Stabilizer-Frame Partitioning |
| 2607.27060 | Optimising Trotter-Suzuki Simulations of Markovian Open Quantum Systems via Classical Search |
| 2607.27051 | Quasi-polar Decomposition of Quantum Neural Networks via Adaptive Non-local Observables |
| 2607.27028 | Unconventional Thermalization of a Three-Wave-Mixing Model |
| 2607.27025 | Quantum random-number generator with non-demolition measurements: semi-device-independent implementation |
| 2607.26999 | Two-state generator extraction: property currents and a two-layer arrow of time in pre- and post-selected quantum dynamics |
| 2607.26978 | Mean-field Pulse Adaptation for the Circulatization of Interacting Rydberg Atoms |
| 2607.26925 | Sparse Quantum Voxel Encoding for Readout-Efficient Molecular Geometry Reconstruction on NISQ Devices |
| 2607.26898 | Revival of transport reciprocity via quantum interference in asymmetric nonlinear devices |
| 2607.26880 | Calibrated Pressure-Observable Born and Hessian Actions for Quantum-Assisted Waveform Inversion |
| 2607.26867 | Analytical Series Expansion for Efficient Gradient Evaluation in Multi-Qubit Optimal Control |
| 2607.26771 | Hybrid quantum-classical end-to-end pipeline for solving MILPs: a vehicle routing case study |
| 2607.26761 | PhD thesis: Modes, States, and Symmetries in quantum Optics for quantum Information and Metrology |
| 2607.26756 | Label and Recover Coherent Errors: Randomized Compiling Does Not Destroy Coherent-Error Information |
| 2607.26716 | Coherent electric field manipulation of nuclear spin qudit |
| 2607.26711 | Generative AI Beyond Tokens: Quantum Resource Consumption of IQP Circuits |
| 2607.26707 | Microscopic study of topological phase transitions: Percolation point of view |
| 2607.26672 | Relational Quantum Causal Processes: Exact Models, Continuum Limits, and the Boundary of Emergent Gravity |
| 2607.26669 | Quantum model reduction based on Oja's flow |
| 2607.26502 | Converting Quantum Sensing Noise into Erasures |
| 2607.26486 | Quantum random number generation using spatial quantum noise of light |
| 2607.26480 | Feedback stabilization of multi-qubit Hamiltonian parameters enabled by single-shot measurement-based sequential Monte Carlo |
| 2607.26478 | Explicit Separations for One-Query Unitary Synthesis |
| 2607.26474 | Phase Retrievability of Super Operators and Measurements |
| 2607.26445 | Lattice Quantum Chromodynamics for Quantum Simulations |
| 2607.26438 | Quantum Optical Reinforcement Learning via Spectrum-Resolved Hong-Ou-Mandel Interference |
| 2607.26436 | Molecular triplets and other metastable states for excitonic quantum batteries |
| 2607.26431 | The Klein-Gordon-Fock theory as a one-particle relativistic quantum mechanics |
| 2607.26351 | On $R$-parastatistics I: Foundation |
| 2607.26349 | Hardware-Aware QUBO Reformulation of Constrained Binary Optimization via the Walsh-Fourier Transform |
| 2607.26225 | Supermartingales in Quantum Resources Theories: Where do quantum resources go when you're watching? |
| 2607.26214 | Minimal Counterexamples of the MacWilliams Extension Theorem for Stabilizer Codes |
| 2607.26157 | Algebraic paradoxes in adaptive quantum computation |
| 2607.26156 | Role of flavor degrees of freedom in quantum simulations of disorder-free localization |
| 2607.26146 | Lindbladian quantization of mechanical systems with nonholonomic constraints |
| 2607.26145 | Contextual advantage implies limited distinguishability in any physical theory |
| 2607.26142 | State preparation and detection for quantum simulation of particle collisions |
| 2607.26139 | Linear Algebra of Generalized Contextuality in All Prepare-Transform-Measure Scenarios |
| 2607.26123 | Quantum Information Decoupling Beyond Finite Dimensions |
| 2607.26122 | Qubit-qubit-qutrit quantum correlations in $H \to f \bar f V$ |
| 2607.26093 | Exact Finite-Dimensional Evaluation of Homodyne Quantum Trajectories for Single-Quadrature Hamiltonian |
| 2607.26080 | Quantum mechanics on the line with two origins |
| 2607.27067 | A Degenerate Singlet-Triplet Qubit with All-Electrical Orthogonal Control (cross-list from cond-mat.mes-hall) |
| 2607.27045 | Temporal Interference from Topological Transitions in Monitored Quantum Dynamics (cross-list from cond-mat.stat-mech) |
| 2607.26919 | Quantum Fisher information of the Klein--Gordon, $\phi^4$, and Dirac vacua (cross-list from hep-th) |
| 2607.26620 | Critical non-thermal fixed point and the dynamical condensation phase transition (cross-list from cond-mat.quant-gas) |
| 2607.26413 | Machine-Checked Certificates for the Geometric Half of the Minimum Kochen-Specker Bound (cross-list from cs.LO) |
| 2607.26331 | Quantum Turing Patterns (cross-list from math-ph) |
| 2607.26208 | MEDA: Measurement-Efficient Disorder-Aware Majorana Zero Mode Detection in Realistic Devices (cross-list from cs.ET) |
| 2607.26132 | Quantum Phase Diagram of the $2+1$D Untruncated SU$(2)$ Lattice Gauge Theory with Dynamical Fermions (cross-list from hep-lat) |
| 2607.26126 | Iterative Gauging is Deconstruction (cross-list from hep-th) |
| 2607.26116 | Where to Find ICEC? - Screening 2442 Systems for Interparticle Coulombic Electron Capture (cross-list from physics.chem-ph) |

---

## 트렌드 분석

### 2026-07-30 주요 트렌드

1. **QKD 보안·통합 연구 3편 동시 발표**: COW-QKD의 CHSH 기반 보안 강화(2607.26856), 시간빈 인코딩 프로토콜의 IID 구조 이론 증명(2607.26772), QNSC-QKD 통합 리뷰(2607.26550)가 함께 게재되어, 이번 배치는 QKD 프로토콜의 실용화(보안 확장·이론 정합성·시스템 통합)라는 공통 축을 형성했다. 특히 2607.26772는 QKD 이론의 대표 그룹(Lütkenhaus)이 발표한 기초 보안 증명 연구다.

2. **플럭소니움 큐비트 하드웨어 진전 클러스터**: 소거오류 검출(2607.27123)과 네이티브 CCZ 게이트(2607.27094) 두 편이 플럭소니움 플랫폼에서 발표되며, 초전도 큐비트 중 플럭소니움이 오류 억제와 다중큐비트 게이트 양면에서 동시에 진전을 보이고 있음을 시사한다.

3. **Rydberg 원자 얽힘 생성 연구 지속**: 유한크기 스케일링 분석(2607.27013), 레벨교차 없는 급단열통과 다중큐비트 게이트(2607.26745), 평균장 펄스 적응(2607.26978) 등 3편이 Rydberg 배열의 얽힘상태 생성·특성분석을 다뤘다.

4. **양자-고전 광인프라 공존 연구**: C-band/O-band 공존 채널 최적화(2607.26905, Quantum Network 매칭), 재구성 가능 광학 통신복잡도 플랫폼(2607.27181, Quantum Communication 매칭), 통신대역 양자점 단일광자원(2607.26957)이 함께 발표되어, 기존 광통신 인프라 위에서 양자 프로토콜을 구현하려는 실용적 방향이 이어지고 있다.

5. **원거리 큐비트 연결을 위한 변환기·인터페이스 연구**: 노이즈 인터페이스를 가진 모듈형 아키텍처의 결함허용 임계값 분석(2607.27204)과 2차원 압전-광기계 변환기(2607.26161)가 함께 발표되어, 분산 양자컴퓨팅을 위한 모듈 간 연결 기술이 이론(오류정정 임계값)과 하드웨어(변환기 소자) 양면에서 병행 발전하고 있다.

### 우선 키워드 관련 논문 현황 (2026-07-30 공지 기준)

| 키워드 | 관련 논문 수 | 주요 논문 |
|--------|------------|----------|
| Quantum Communication | 1편 | 2607.27181 |
| QKD | 3편 | 2607.26856, 2607.26772, 2607.26550 |
| Entanglement Distribution | 0편 | 해당 없음 (2607.27195는 얽힘 조작/증류 이론이나 "분배" 프로토콜은 아님) |
| Quantum Network | 1편 | 2607.26905 |
| Quantum Teleportation | 0편 | 해당 없음 |

---

*본 보고서는 Claude Code의 WebFetch 도구를 이용하여 2026-07-31(금)에 생성되었습니다. 조회 시점 기준 arXiv 최신 공지 배치가 2026-07-30(목) 제출분으로 확인되어 해당 배치를 수집·분석하였습니다.*
