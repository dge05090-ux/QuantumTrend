# Quantum Research Report — 2026-07-22 (Wednesday)

> **수집 기준**: 2026-07-21 (화) arXiv quant-ph 신규 논문 (화~금요일 실행 규칙: 전날 자료)
> **생성일**: 2026-07-22 (수)
> **수집 논문 수**: 124편 (2026-07-21 announced, 신규 제출 + 교차등재 포함) — Top 5 심층 분석 + 대표 16편 요약 (총 21편 초록 확인), 나머지 103편은 제목 목록 수록
> **우선순위 키워드**: Quantum Communication, QKD, Entanglement Distribution, Quantum Network, Quantum Teleportation

> **비고**: `export.arxiv.org/api/query`(주 수집 경로)를 WebFetch로 조회한 결과, submittedDate 기준 2026-07-20까지의 데이터만 반환되고 2026-07-21 제출분이 누락되는 기존 known issue가 재현되었다. CLAUDE.md 지침에 따라 `arxiv.org/list/quant-ph/recent` 대체 경로로 전환, 페이지네이션(`?skip=`)을 통해 announcement-date 기준 2026-07-21(화) 목록 전체 124편을 확보해 이를 이번 리포트의 기준 데이터셋으로 사용했다. 우선순위 키워드에 직접 매칭되는 논문은 총 9편(QKD 3편, Quantum Network 3편, Quantum Teleportation 1편, Quantum Communication/광링크 2편)으로 Top 5 전량을 우선순위 매칭 논문으로 채웠다. 이례적으로 많은 논문 수(평소 40~60편 대비 2배 이상)로 인해 대표 논문 21편(우선순위 매칭 9편 포함)만 초록을 확인·요약했으며, 나머지 103편은 리포트 하단에 제목만 수록한다. 배치 조회(`id_list=...`)는 이번에도 타임아웃으로 실패해 개별 `arxiv.org/abs/<id>` 페이지를 병렬 WebFetch하여 수집했다.

---

## Top 5 심층 분석

### 1. Quantum Key Distribution Beyond Stationary Channels
**arXiv**: [2607.17690](https://arxiv.org/abs/2607.17690)
**저자**: Vaisakh Mannalath, Víctor Zapatero, Kiyoshi Tamaki, Marcos Curty
**키워드**: QKD

#### 기술적 기여
위성 링크처럼 "짧고, 손실이 크며, 강하게 변동하는 전송 윈도우로 인해 검출 이벤트가 희박한" 비정상(non-stationary) 채널에서의 QKD 보안 분석을 다룬다. 기존 non-IID 통계 분석 기법은 표본이 적을 때 성능이 나쁘거나 채널 모델 가정에 지나치게 의존하는 한계가 있었다. 이 연구는 혼합 마팅게일(mixture martingale) 기법을 도입하여, 채널 모델이 정확할 때는 날카로움을 유지하면서도 모델 불일치에는 강건한 밀집 집중 부등식(concentration inequality)을 개발했다.

#### 의의
위성 QKD 시뮬레이션에서 변동하는 손실 조건 하에 필요한 최소 전송 신호 수를 70% 이상 절감할 수 있음을 보였다. 정지 채널을 가정하는 기존 보안 증명 프레임워크의 실질적 한계를 극복하여, 비정상 채널 환경에서의 QKD 실용성을 크게 높인 결과다.

#### 응용 가능성
위성-지상 QKD 링크, 이동체(드론·차량) 기반 양자 통신, 대기 요동이 심한 자유공간 QKD 채널의 실시간 키 생성률 향상에 직접 적용 가능하다.

---

### 2. Intelligence-Guided Adaptive Purification for DDoS-Resilient Quantum Networks: A CUDA-Q based Study
**arXiv**: [2607.16276](https://arxiv.org/abs/2607.16276)
**저자**: Santanu Ganguly
**키워드**: Quantum Network

#### 기술적 기여
양자 리피터 네트워크에서 얽힘 생성률·종단간 충실도·정제(purification) 오버헤드·메모리 유도 지연을 동시에 고려하면서 사이버 공격에 견디는 제어 전략을 다룬다. CUDA-Q와 SeQUeNCe를 결합한 시뮬레이션 프레임워크를 개발하여 리피터 체인에서의 얽힘 정제를 모델링했다. DDoS 트래픽 공격 상황에서 공격을 인지하지 못하는 제어기는 목표 충실도 이상 전달률이 0.098에 그치는 반면, IDS 인지형 자원 적응 제어기는 정제 비중이 높은 마스크로 전환해 이를 0.344까지 끌어올렸다.

#### 의의
양자 네트워크 보안 연구가 암호학적 계층을 넘어 네트워크 제어·자원관리 계층의 사이버 위협 대응으로 확장되고 있음을 보여준다. 사이버보안 상태 정보를 얽힘 정제 제어에 통합하는 최초의 실증적 접근 중 하나다.

#### 응용 가능성
대규모 상용 양자 인터넷의 침입 탐지 연동형 자원 관리, 국가 기반시설급 양자 네트워크의 가용성 보장, 다중 사용자 환경에서의 서비스 품질(QoS) 차등 제어에 적용 가능하다.

---

### 3. GHZ-Equivalent State Distribution in Quantum Networks: Reducing Decoherence and Quantum Resource Consumption
**arXiv**: [2607.17101](https://arxiv.org/abs/2607.17101)
**저자**: Chun-Hsiang Wang, Chia-Wei Tsai
**키워드**: Quantum Network

#### 기술적 기여
리피터 기반 양자 네트워크에서 GHZ 등가 상태를 분배하는 새로운 방식을 제안하며, 전송 중 결어긋남 분석과 완화에 초점을 맞춘다. 원격 사용자들이 QKD·양자 비밀 공유 등 다양한 양자 통신 프로토콜에 활용 가능한 그래프 상태를 공유할 수 있게 한다. 기존 방식 대비 불필요한 중복 얽힘 구조 없이 O(N) 큐비트만으로 구현되며, 게이트 수와 큐비트 사용 모두에서 선형 스케일링하는 병합(merging) 절차를 갖는다. NetSquid 시뮬레이터로 검증했다.

#### 의의
다자간 얽힘 상태 분배의 자원 효율성 문제를 O(N) 큐비트로 해결한 실용적 프레임워크다. 대규모 그래프 상태 분배를 지원하여 다자간 양자 통신 프로토콜의 네트워크 계층 구현을 앞당긴다.

#### 응용 가능성
다자간 QKD, 양자 비밀 공유(QSS) 네트워크, 대규모 클러스터 상태 기반 분산 양자 컴퓨팅의 자원 배분 계층에 즉시 적용 가능하다.

---

### 4. Relativistic quantum teleportation protected by the anti-Unruh effect
**arXiv**: [2607.17216](https://arxiv.org/abs/2607.17216)
**저자**: Reza Hamzehofi, Davood Afshar, Mehrzad Ashrafpour
**키워드**: Quantum Teleportation

#### 기술적 기여
가속 관찰자(Rob)와 정지 관찰자(Alice) 간의 상대론적 양자 텔레포테이션을 Unruh-DeWitt 검출기 모델로 분석한다. 검출기 에너지 갭이 작을 때 가속도 증가에 따라 얽힘이 단조 증가하며, 갭이 클 때는 저가속에서 Unruh 효과로 얽힘이 감소했다가 고가속에서 anti-Unruh 효과에 의해 회복·강화됨을 보였다. 이는 유효 검출기 온도 감소와 연관되며, 장에 의해 손실됐던 양자 결맞음을 회복시킨다.

#### 의의
가속에 의한 양자 정보 열화가 항상 단조적이지 않으며, anti-Unruh 효과를 통해 텔레포테이션 충실도가 고가속 영역에서 1에 근접하도록 보호·회복될 수 있음을 최초로 보였다. 상대론적 양자 정보 이론과 실용 텔레포테이션 프로토콜을 연결하는 기초 연구다.

#### 응용 가능성
위성·우주 기반 양자 통신 링크에서 상대론적 효과(고속 이동체)를 고려한 텔레포테이션 프로토콜 설계, 극한 가속도 환경(우주 탐사체)에서의 양자 정보 보존 전략 수립에 이론적 토대를 제공한다.

---

### 5. Broadband Polarization Compensation with Link Segment Reconstruction for Quantum Optical Links
**arXiv**: [2607.17400](https://arxiv.org/abs/2607.17400)
**저자**: Qingyu Shi, Erwan Trad, Julien Chénedé, Tobias Vogl
**키워드**: Quantum Communication

#### 기술적 기여
넓은 파장 대역에서 임의의 편광 변환을 합성할 수 있는 4-파장판 보상기를 개발했다. 보상기 양측의 링크 세그먼트 뮤엘러 행렬을 재구성하는 8-스토크스 벡터 프로토콜을 제안하여, 설계 파장에서 100 nm 이상 벗어난 조건에서도 추가 최적화 없이 편광 유도 양자 비트 오류율을 1% 미만으로 낮췄다. 보조 파장 2개 측정과 결합하면 온도 변화에 따른 파장 민감 광섬유 성분의 변화도 추적 가능하다.

#### 의의
양자 광링크의 편광 드리프트 문제를 광대역·비최적화 조건에서 실용적으로 해결한 엔지니어링 성과다. 다중화된 양자 광네트워크에서 보상기 위치와 파장 선택의 유연성을 크게 높였다.

#### 응용 가능성
파장분할다중화(WDM) 기반 도시 규모 QKD 네트워크, 장거리 광섬유 얽힘 분배 링크, 온도 변화가 큰 야외 환경의 양자 통신 인프라 안정화에 직접 적용 가능하다.

---

## 추가 논문 요약 (16편)

| No. | arXiv ID | 제목 | 핵심 내용 | 분류 |
|-----|----------|------|-----------|------|
| 1 | 2607.17465 | The finite key effect of side-channel-secure QKD beyond post-selection technique | EUR·QLHL 기반 가변 길이 부채널 안전 QKD 보안 증명, 오류정정 후 키 길이 결정 조건 확장 | QKD |
| 2 | 2607.17960 | Fixed Point Exploration For CV-QKD IR QC-MET-LDPC Toward Hardware Implementation | CV-QKD LDPC 복호기의 고정소수점 SPA/MSA/NMS 비교, SPA+Q8.4가 신뢰성-하드웨어 효율 균형 최적 | QKD |
| 3 | 2607.16394 | Entanglement Entropy in Quantum Networks with Tunable Geometry | 조정 가능한 그래프 범위 파라미터로 얽힘 성장·수송 연구, 구조적 무질서 유도 Anderson 국소화 규명 | 양자 네트워크 |
| 4 | 2607.17321 | Locally Scrambled Quantum Memories for Loss-Tolerant Entanglement-Assisted Optical Interferometry | 국소 스크램블링 양자 메모리로 광간섭계 결맞음 보존, 결손된 절반 미만 메모리까지 정정 가능 | 얽힘 분배 |
| 5 | 2607.18204 | QuantiSpect: A Structure-Aware Lightweight 3D CNN Pre-Decoder for Surface Code QEC | 3분기 잔차 블록 구조로 파라미터 2.7배 절감하며 표면부호 오류정정 속도 대폭 향상 | 양자 오류 정정 |
| 6 | 2607.18196 | Hardware Robustness of Sample-Based Quantum Diagonalization | IBM Heron에서 SQD의 CCSD 진폭 섭동에 대한 강건성 및 노이즈 완화 설정별 수렴 특성 분석 | 양자 하드웨어 |
| 7 | 2607.17872 | Entanglement geometry separates circuit cutting, classical hardness, and trainability | MPS/TTN 회로의 얽힘 기하가 회로 절단·고전 시뮬레이션 난이도·학습가능성 간 상충 관계 규명 | 양자 알고리즘 |
| 8 | 2607.17714 | Formal Verification of Continuous-Variable Quantum Programs | 연속변수 양자컴퓨팅 최초의 Hoare 논리 및 기호적 최약전제조건 계산기 구현 | 양자 소프트웨어 |
| 9 | 2607.17705 | Image Classification on IBM Quantum Computers | 127큐비트 IBM Eagle에서 10클래스 MNIST 분류, 하드웨어 미세조정 정확도 향상 없음 확인 | 양자 머신러닝 |
| 10 | 2607.17562 | Temporal Diffraction Grating for Engineered Superconducting Qubit Dissipation | 펄스형 파라메트릭 변조로 초전도 큐비트 소산 스펙트럼을 N-슬릿 회절 유사 구조로 제어 | 양자 하드웨어 |
| 11 | 2607.17131 | Blind Transpiler: An open-source library for universally blind and homomorphic quantum computations | Qiskit 회로를 블라인드 양자계산 변형으로 변환하는 오픈소스 라이브러리, IRIS 분류기로 실증 | 양자 암호 |
| 12 | 2607.16575 | 80 Channel Photon Pair Source from a Thin-Film Lithium Niobate Racetrack Microresonator | TFLN 공진기에서 SPDC/SFWM으로 80채널 광자쌍 생성, 49.5 GHz 간격, 125.7 kHz/μW 생성률 | 양자 통신 인프라 |
| 13 | 2607.16503 | Holographic quantum codes with trapped ions | 트랩 이온으로 오각형·칠각형 홀로그래픽 코드 실험 구현, Ryu-Takayanagi 면적 법칙 검증 | 양자 오류 정정 |
| 14 | 2607.17204 | Heralded Leakage Detection with Preserved Computational-State Coherence in a Fixed-Frequency Transmon | 리드아웃 중 Rabi 구동으로 비파괴 누설 검출, 97.1% 검출 충실도·92.9% 상태 보존 | 양자 하드웨어 |
| 15 | 2607.18059 | Foundry CMOS platform for multimodal quantum materials characterization | 상용 65nm CMOS로 극저온 자기 특성·광검출 자기공명 등 다중 모달 양자 물질 특성평가 플랫폼 | 양자 센싱 |
| 16 | 2607.17023 | Rigorous characterization of continuous-variable quantum states via optical parametric amplifiers | 고이득 광 파라메트릭 증폭 기반 반정부호계획법으로 비가우스 상태 인증, 단일광자·고양이·GKP 상태 실증 | 양자 광학 |

---

## 나머지 논문 목록 (제목만 수록, 103편)

| arXiv ID | 제목 |
|----------|------|
| 2607.18137 | Phase-Sensitive Benchmarking of Composite Quantum Gates with Chiral-Interference Circuits on Quantum Hardware |
| 2607.18126 | CutBackdoor: A Circuit Cut Triggered Backdoor Attack on Variational Quantum Algorithms |
| 2607.18113 | Exponential Reduction of Mesh Dependence in Quantum Estimation of Parabolic PDE Observables |
| 2607.18105 | Topology of the Set of Entangled State |
| 2607.18050 | New bound on S1×S2-setting Bell locality of a nonseparable Werner state |
| 2607.17975 | Strong Quantum Mpemba Effect from Exact Slow-Mode Selection in Constrained Rydberg Chains |
| 2607.17936 | Noise structuring in fixed-depth Trotter simulation: stationary channels and observable-level depolarization |
| 2607.17934 | Variational non-gaussian approach to interacting spin-boson models |
| 2607.17920 | Sensing relativistic quantum fields with minimally perturbing local measurements |
| 2607.17894 | How the Quantum Sorites Phenomenon Strengthens the Bell Argument and How a Random-Matrix Collapse Dynamics Answers It |
| 2607.17886 | Unifying Charge-Learnability Transitions in U(1)-Symmetric Quantum Circuits through Informational Power of Local Measurement |
| 2607.17854 | High-frequency dual-channel lock-in detection via rapidly oscillating driving |
| 2607.17804 | Stochastic Pauli-path simulator for large-scale quantum optimization |
| 2607.17793 | Geometry-Resolved Projection of RF Imbalance to Ion Micromotion in a Same-Phase Dual-RF Blade Trap |
| 2607.17740 | Light-Cone Scaling of In-Circuit Noise in Randomized Measurements |
| 2607.17678 | Variance-Reduced Trajectory Unravelings for GPU Noisy Quantum-Circuit Simulation |
| 2607.17647 | Active Optical Frequency Measurements with Superradiance Prolonged by a Modulated Magnetic Field |
| 2607.17629 | Fully-connected three-mode squeezed vacuum: Gaussian entanglement, steering, and collective photon subtraction |
| 2607.17618 | Spatial nonlocality imaging via metasurface |
| 2607.17583 | Single-atom sensor for low-frequency electric field |
| 2607.17554 | Lie-Group Mode Connectivity in Quantum Machine Learning from a Dynamical Lie Algebra Perspective |
| 2607.17534 | Neural Gauge-P Representation for Open Quantum Dynamics of Interacting Bosons |
| 2607.17498 | LLM-Driven Cross-Paradigm Design for Quantum Optimal Control |
| 2607.17443 | Operator-centric Clifford algebra for variational eigensolvers and finite-shot adaptive selection |
| 2607.17327 | Interpreting Quantum Learning Models via Stochastic Processes |
| 2607.17320 | Scaling law for optimal excitation storage and superradiant release in waveguide QED systems |
| 2607.17319 | Constraints on recovering quantum information after erasure |
| 2607.17302 | Chiral Entangled-State Generation through Dissipative Quantum Dynamics |
| 2607.17295 | Truncated Wigner approximation for spins in continuous phase space |
| 2607.17273 | Continuous Time Quantum Walk Propagation for Irregular Temporal Graph Forecasting |
| 2607.17202 | Multi-level Random-Telegraph Noise Mitigation using a Single Spectator Qubit |
| 2607.17174 | QBism Logic |
| 2607.17086 | Against Many Worlds |
| 2607.17081 | quchip: A Differentiable Toolkit for Modeling Quantum Devices |
| 2607.16996 | Encoding Choices and Fault-Tolerant Resource Estimates for Digital Quantum Hamiltonian Descent |
| 2607.16988 | How many degrees of freedom describe a quantum N-particle state? |
| 2607.16960 | Entanglement Quantification via Symmetric Extensions: A Resource Theory Hierarchy |
| 2607.16951 | Operational Relation Between One-Time and Two-Time Work Protocols |
| 2607.16944 | Bound, Scattering, and Resonance States of Symmetric Woods-Saxon Potential |
| 2607.16928 | Response to Sheldon Goldstein Objection re: Relativistic Bohmian Models |
| 2607.16885 | Precision dynamics of resonantly enhanced optical parametric amplifiers |
| 2607.16878 | Bargmann invariants and local unitary equivalence |
| 2607.16869 | Correlation-Rank Limits and Clifford-Accessible Measurement |
| 2607.16866 | Certified Optimal Measurement Reduction over Quantum Context Landscapes |
| 2607.16861 | Experimental Nanoscale Thermodynamics |
| 2607.16857 | Universal Parent Hamiltonians for Adiabatic Warm Starts |
| 2607.16849 | Attosecond delay metrology via Hong-Ou-Mandel interferometry |
| 2607.16846 | Geometric Qubits in Programmable Atomic Trimers |
| 2607.16839 | Removing inhomogeneous broadening in cross-relaxation spectra via hole burning |
| 2607.16829 | Shortcuts to adiabaticity in five-level systems |
| 2607.16800 | Identity-Paired Progressive Depth Training |
| 2607.16765 | QNLP for Hindi Sentiment Classification |
| 2607.16702 | Reliability Is Not Free in Universal Quantum Work Extraction |
| 2607.16701 | Quantum Metrological Detection of the Unruh Effect |
| 2607.16672 | A projection-free approach toward mapping the structured polarization fields |
| 2607.16667 | Graph State Generation for Measurement-Based Quantum Computing |
| 2607.16653 | Mean-State Entropy Hierarchies and Classical Communication through Quantum Convolutions |
| 2607.16645 | Geometric Power Capacity of Coherent Ergotropy in Quantum Batteries |
| 2607.16642 | p-Body ≃ Range p-1: Exact Order-Range Mapping |
| 2607.16641 | Geometric quantum discord in the black hole quantum atmosphere |
| 2607.16592 | Quantum dynamics of a levitated ferromagnetic gyroscope |
| 2607.16541 | Efficient Exact Quantum Sampling from Sun-Wootters Distribution |
| 2607.16516 | Split-quaternionic structure and Bateman dual oscillator |
| 2607.16466 | Host-guest Crystal Engineering for Molecular Quantum Devices |
| 2607.16436 | Feynman Meets Turing: The Curse of Quantum Universality |
| 2607.16419 | Remote Infrared Absorption Spectroscopy with Undetected Photons |
| 2607.16410 | Quantum-Centric Geometry Optimization with Wave-Function-Based Embedding |
| 2607.16396 | Uncountably many inequivalent maximally entangled measurements |
| 2607.16391 | Dissipative Stabilization of Floquet-Engineered Many-Body Order |
| 2607.16389 | Sample-based quantum diagonalization for transition-metal complexes |
| 2607.16385 | The Norton Theorem for Quantum Circuits and Systems |
| 2607.16380 | Hamiltonian Lift of Bures-Wasserstein Covariance Dynamics |
| 2607.16376 | Quantum Correction to Gaussian Information Geometry |
| 2607.16281 | Novel Hybrid Quantum Reservoir Computing for Phase Transitions |
| 2607.16278 | Number Fluctuations and Entanglement-Spectrum Participation in Monitored Free Fermions |
| 2607.16277 | Hybrid Classical-Quantum Approach for Location Optimization |
| 2607.16275 | QR-SPPS: Quantum-Native Retail Supply Chain Risk Simulation |
| 2607.16271 | EPIC-CIM: Training Convolutional Neural Networks on a Coherent Ising Machine |
| 2607.16265 | Relativistic bound-state solutions for hyperbolic potential |
| 2607.18215 | Non-Abelian Gauge Field Mechanics |
| 2607.18179 | Semi-fractality and localization on a chiral Cayley tree |
| 2607.18028 | Universal Dynamic Scaling of 2D Quantum Ising Transition on the Fuzzy Sphere |
| 2607.17964 | Scanless quantum Fourier-transform mid-infrared spectroscopy for rapid high-sensitivity hyperspectral mapping |
| 2607.17871 | On the use of the Belopol'skaya-Daletskii representation of a diffusion on a Riemann manifold to construct path integrals |
| 2607.17734 | Depth Determination of Individual Shallow NV-Centers via Spin-Lock NMR |
| 2607.17417 | Grounded verification of chemical and materials reasoning: detection is the bottleneck |
| 2607.17408 | The History of Hilbert-Space Formulations of Classical Physics |
| 2607.17354 | Colored ΔT noise probes the topological character of edge modes |
| 2607.17352 | Self-Modifying Lean Proof Agents with Verifier-Grounded Benchmark Coevolution |
| 2607.17346 | The Information Content of Krylov Observables: A Machine Learning Approach |
| 2607.17334 | Coexistence of long- and quasi-long range spatial order in 1D quantum quasicrystals |
| 2607.17219 | Auditing Question-Order Effects in Large Language Models with the QQ Equality |
| 2607.16820 | Two-dimensional solitons in extended GPE models with Lee-Huang-Yang corrections |
| 2607.16520 | Bridging Relativistic Twisted Fermion Beams and Photonic OAM Flux in Gauged Hopf Lattices |
| 2607.16515 | Stroboscopic stability of a Floquet chiral spin liquid beyond the folding frequency |
| 2607.16500 | Observation of Critical Current Minimum in Super-Honeycomb Josephson Junction Arrays |
| 2607.16483 | Bond reconstruction and vacancy clustering in monolayer silicon carbide from first principles |
| 2607.16411 | Multibath Influence Matrices: Universal Scaling from Real-Time Dynamics |
| 2607.16403 | Universality of Magic in Local Quantum Field Theory |
| 2607.16399 | Eddy currents and current reversal in curved magnetic thin-film Josephson junctions |
| 2607.16374 | Theoretical adversarial collaboration: a template |
| 2607.16368 | Simulating neural network criticality and resource dynamics with Rydberg gases |
| 2607.16301 | Gaussian Reformulation of the Feynman Path Integral for Quantum Statistical Mechanics |

---

## 트렌드 분석

### 2026-07-22 주요 트렌드

1. **비정상(non-stationary) 채널 QKD 보안 증명의 실용화**: 2607.17690은 위성 링크와 같은 변동성 큰 채널에서 마팅게일 기법으로 필요 신호 수를 70% 이상 절감했다. 정지 채널 가정을 벗어난 QKD 보안 이론이 실제 위성·이동체 링크에 빠르게 다가서고 있다.

2. **양자 네트워크의 사이버보안 계층 확장**: 2607.16276의 DDoS 저항형 적응 정제 제어기는 양자 네트워크 보안 논의가 도청(암호학적 계층)을 넘어 가용성·서비스 거부 공격 대응(네트워크 제어 계층)으로 확장되고 있음을 보여준다. IDS 연동형 자원 관리라는 새로운 접근이 두드러진다.

3. **다자간 얽힘 자원 효율화**: 2607.17101의 GHZ 등가 상태 분배는 O(N) 큐비트만으로 대규모 그래프 상태 분배를 지원해, 다자간 QKD·양자 비밀공유의 네트워크 계층 실용성을 높였다.

4. **상대론적 효과를 이용한 양자 정보 보호**: 2607.17216은 anti-Unruh 효과가 가속 환경에서 텔레포테이션 충실도를 오히려 회복·강화할 수 있음을 보여, 상대론적 양자 정보 열화가 비단조적임을 규명했다. 위성·우주 기반 양자 통신의 이론적 토대 확장에 기여한다.

5. **양자 광링크 엔지니어링의 성숙**: 2607.17400(광대역 편광 보상)과 2607.16575(80채널 TFLN 광자쌍 소스)가 동시에 발표되며, 다중화된 양자 광네트워크 구축에 필요한 실용 광학 부품 기술이 빠르게 성숙하고 있다.

6. **표면부호 오류정정의 경량화**: 2607.18204의 QuantiSpect는 파라미터 2.7배 절감으로 확장 가능한 표면부호 사전 복호기를 제시했으며, 홀로그래픽 코드(2607.16503) 실험도 병행되어 결함허용 양자컴퓨팅 하드웨어·이론 양면에서 진전이 이어지고 있다.

### 우선순위 키워드 관련 논문 현황 (2026-07-21 기준)

| 키워드 | 관련 논문 수 | 주요 논문 |
|--------|------------|----------|
| Quantum Communication | 2편 | 2607.17400, 2607.16575 |
| QKD | 3편 | 2607.17690, 2607.17465, 2607.17960 |
| Entanglement Distribution | 2편 | 2607.17321, 2607.16394 |
| Quantum Network | 3편 | 2607.17101, 2607.16276, 2607.16394 |
| Quantum Teleportation | 1편 | 2607.17216 |

---

*본 보고서는 WebFetch 도구를 이용하여 2026-07-22(수)에 생성되었습니다. `export.arxiv.org/api/query`가 2026-07-20까지의 데이터만 반환하는 known issue로 인해 `arxiv.org/list/quant-ph/recent` 대체 경로(페이지네이션)로 전환하여 2026-07-21(화) 제출·교차등재 논문 124편 전체 목록을 확보했다. 평소 대비 2배 이상의 논문 수로 인해 우선순위 키워드 매칭 9편 전량과 대표 논문 12편, 총 21편의 초록을 확인·요약했으며 나머지 103편은 제목만 수록했다.*
