# Quantum Research Report — 2026-07-17 (Friday)

> **수집 기준**: 2026-07-16 (목) arXiv quant-ph 신규 논문
> **생성일**: 2026-07-17 (금)
> **수집 논문 수**: 72편 (2026-07-16 announced) — Top 5 심층 분석 + 대표 19편 요약 (총 24편 수록)
> **우선순위 키워드**: Quantum Communication, QKD, Entanglement Distribution, Quantum Network, Quantum Teleportation

> **비고**: `export.arxiv.org/api/query`(주 수집 경로)를 WebFetch로 조회한 결과, submittedDate 기준 2026-07-16 제출분(2607.15xxx~2607.14484 구간, 46편 확인) 수집 중 반복 조회에서 `HTTP 429 Too Many Requests`가 발생해 전체 목록 확보에 실패했다. CLAUDE.md 지침에 따라 `arxiv.org/list/quant-ph/recent` 대체 경로로 전환, 페이지네이션(`?skip=`)을 통해 announcement-date 기준 2026-07-16(목) 목록 전체 72편(신규 제출 + 교차등재 포함)을 확보해 이를 이번 리포트의 기준 데이터셋으로 사용했다. 우선순위 키워드 매칭 논문(6편, Top 5 포함)과 하드웨어·QEC·알고리즘·이론 전반을 아우르는 대표 논문 19편을 선별해 초록을 확인·요약했다. 나머지 48편은 리포트 하단에 제목만 수록한다. 이번 수집일은 QKD/양자네트워크 직접 매칭 논문이 평소보다 적어(6편), 우선순위 인접 분야(QRNG 보안, 거리제한 프로토콜 보안)까지 포함해 Top 5를 구성했다.

---

## Top 5 심층 분석

### 1. A Measurement Plane for Quantum Networking
**arXiv**: [2607.13291](https://arxiv.org/abs/2607.13291)
**저자**: Abderrahim Amlou, Amar Abane, Anouar Rahmouni, Mheni Merzouki, Abdella Battou, Ahmed Lbath, Ya-Shian Li-Baboud, Oliver Slattery, Thomas Gerrits
**키워드**: Quantum Network / Entanglement Distribution (양자네트워크 측정 전용 아키텍처 계층)

#### 기술적 기여
기존 양자네트워크 테스트베드에 결여된 "측정 전용 평면(measurement plane)"을 제어·데이터 평면과 별도로 설계했다. 애플리케이션·실험조정·기능·자원에이전트의 4계층 분산 프레임워크를 컨테이너화된 마이크로서비스와 발행-구독(pub/sub) 통신으로 구현하고, 2노드 테스트베드에서 동시계수 측정과 얽힘분배 실험 조율을 검증했다. 최대 98%의 간섭 가시도(visibility)를 달성하며 실시간 측정 피드백을 제공했다.

#### 의의
양자네트워크 연구가 개별 소자 실증 단계를 넘어 "측정 인프라의 표준화·모듈화" 단계로 진입하고 있음을 보여준다. 실험 조율과 측정을 운영 평면에서 분리함으로써 서로 다른 하드웨어·프로토콜 간 상호운용성을 높이는 실용적 기반을 제공한다.

#### 응용 가능성
- 다기관 양자네트워크 테스트베드 간 표준 측정 인터페이스
- 얽힘분배 실험의 실시간 품질 모니터링 시스템
- 양자중계기 네트워크의 운영-측정 계층 분리 아키텍처

---

### 2. Fibre-Integrated SPDC Heralded Single-Photon Source Using Zn-Indiffused PPLN Ridge Waveguides at Telecom Wavelengths
**arXiv**: [2607.13215](https://arxiv.org/abs/2607.13215)
**저자**: Peter Iveson, Paolo L. Mennea, Goronwy Tawy, Rex H. S. Bannerman, Noe Palomar-Davidson, Lewis D. Wright, Patrick M. Ledingham, Peter G. R. Smith, James C. Gates, Corin B. E. Gawith
**키워드**: Quantum Communication (통신파장대 광섬유 결합 단일광자원)

#### 기술적 기여
상용 Zn-확산 MgO:PPLN 리지 도파로에서 Type-0 축퇴 SPDC를 이용해 광섬유 결합형 단일광자원을 구현했다. 통신 C·L밴드에 걸친 약 70nm 광대역 스펙트럼과 9.1×10⁹ pairs/(s·mW)의 절대 밝기를 달성했으며, 손실 보정 후 내부 헤럴딩 효율 58%, 우연동시계수 대비 동시계수비 9×10⁴ 이상, 헤럴드 2차상관함수 g⁽²⁾_h(0) = (5.53±0.46)×10⁻⁴의 고품질 단일광자 특성을 입증했다.

#### 의의
기존 광통신 인프라와 직접 호환되는 파장대에서 파장다중화가 가능한 고밝기·고순도 광자원을 상용 부품으로 구현했다는 점에서, 양자네트워크 노드의 저비용·대량생산 가능성을 높였다.

#### 응용 가능성
- 파장다중화 기반 QKD·양자중계기 광자원
- 통신망 직접 통합형 양자네트워크 노드
- 온칩 집적 가능한 헤럴디드 단일광자 플랫폼

---

### 3. Precoding-based protocols for entanglement assisted linear computation over a quantum many-to-one network
**arXiv**: [2607.13756](https://arxiv.org/abs/2607.13756)
**저자**: Ruoyu Meng, Aditya Ramamoorthy
**키워드**: Quantum Network (얽힘보조 다자간-단일수신 양자네트워크 계산)

#### 기술적 기여
k명의 송신자(Alice)가 각자 유한체 위의 데이터벡터를 보유하고 수신자(Bob)가 이들의 선형결합을 계산하는 many-to-one 양자네트워크 모델에서, 기존 N-Sum Box 프로토콜보다 더 넓은 범주의 선형변환 계산을 지원하는 새 프로토콜을 제안했다. 송신자에게 추가 큐디트와 프리코딩 능력을 부여해 통신비용을 기존 대비 동등 이하로 유지하면서, 두 선형함수를 동시에 계산하는 것이 개별 계산보다 비용이 낮은 부가합성(subadditive) 통신 특성을 입증했다.

#### 의의
양자네트워크에서 통신과 계산을 결합하는 "양자 네트워크 코딩"의 적용 범위를 확장했으며, 다자간 얽힘자원을 활용한 분산 계산의 자원효율성을 이론적으로 개선했다.

#### 응용 가능성
- 다자간 양자센서 네트워크의 분산 함수계산
- 양자보안 다자간 연산(MPC)의 통신비용 절감
- 양자중계기 네트워크 상의 선형결합 라우팅 프로토콜

---

### 4. Effects of coherent and incoherent measurement imperfections on multipartite quantum nonlocality and quantum key distribution
**arXiv**: [2607.13645](https://arxiv.org/abs/2607.13645)
**저자**: Qiong Wang, Wen-Long Qiao, Qing Chen, Liu-Jun Wang
**키워드**: QKD (다자간 비국소성·QKD에 대한 측정오차 영향)

#### 기술적 기여
n분할 GHZ 상태에 대한 Mermin·Svetlichny·MABK 부등식을 이용해 결맞음 각도오정렬과 비결맞음 결과반전이라는 두 유형의 측정오차가 다자간 벨 비국소성에 미치는 영향을 분석했다. 결맞음 오차는 파티수가 늘어날수록 폭이 좁아지는 주기적 위반 구간을 만들며, "비밀키 생성이 비국소성 인증보다 측정오차에 더 엄격한 제약을 부과한다"는 사실을 규명했다.

#### 의의
디바이스 독립(DI) 양자프로토콜에서 비국소성 검증만으로는 QKD 보안 요구조건을 담보하지 못한다는 것을 정량적으로 보여, DI-QKD 실험설계에 실질적 벤치마크를 제공한다.

#### 응용 가능성
- 다자간 DI-QKD 프로토콜의 측정오차 허용범위 설계
- 실험 하드웨어의 각도정렬·검출오차 규격 수립
- 다자간 비밀키 합의 프로토콜의 강건성 평가 기준

---

### 5. Security Evaluation of Laser-Phase-Noise Quantum Random Number Generators with Intrinsic Correlations
**arXiv**: [2607.13521](https://arxiv.org/abs/2607.13521)
**저자**: Y. Gao, J.H Li, J.L. Liu, M. Wu, L.J. Liu, H. Wang, Y. Pan, W. Huang, Y. Li, J. Yang, B.J. Xu
**키워드**: QKD 인접 (양자난수생성기의 내재적 상관성 보안분석)

#### 기술적 기여
레이저 위상잡음 기반 QRNG의 원시데이터에 존재하는 상관성을 정식화하는 이론모델을 개발하고, 이러한 실측조건 하에서 조건부 최소엔트로피 표현식을 유도했다. 시뮬레이션·실험 검증 결과 이론과 "우수한 일치"를 보였으며, 내재적 상관성을 무시할 경우 추출 가능한 난수량을 통상적 운용조건에서 약 46% 과대평가하게 됨을 정량적으로 밝혔다.

#### 의의
QKD 시스템의 신뢰성은 난수원의 보안성에 직결되는데, 본 연구는 실제 QRNG 하드웨어의 숨은 상관성을 무시한 기존 보안분석이 체계적으로 안전성을 과대평가해왔음을 보여 QKD 전체 보안사슬의 취약점을 드러냈다.

#### 응용 가능성
- 소형·고성능 QRNG의 엄밀한 보안 인증 절차
- QKD 시스템 통합용 난수원의 실시간 상관성 모니터링
- 상용 QRNG 제품의 최소엔트로피 재산정 기준

---

## 추가 논문 요약 (19편)

| # | 제목 | arXiv ID | 주요 내용 | 분류 |
|---|------|----------|-----------|------|
| 6 | Security evaluation of quantum distance-bounding protocols via semidefinite programming | [2607.13464](https://arxiv.org/abs/2607.13464) | 양자 거리제한 프로토콜의 거리사기·마피아사기 공격을 볼록최적화로 환원, SDP로 엄밀한 공격성공확률과 인증서를 도출 | QKD 인접·프로토콜 보안 |
| 7 | SiMOS quantum-dot spin qubits enabled by extreme-ultraviolet lithography | [2607.13121](https://arxiv.org/abs/2607.13121) | 300mm 반도체 파일럿라인의 EUV 리소그래피로 실리콘 스핀큐비트 웨이퍼 균일성과 99% 이상 게이트 충실도 동시 달성 | 스핀큐비트·양산기술 |
| 8 | Precision quantum simulation of magnon spectra and interactions | [2607.13301](https://arxiv.org/abs/2607.13301) | 97큐비트 초전도 프로세서로 2차원 양자자석의 마그논 스펙트럼·비선형 상호작용을 시뮬레이션, MPS 시뮬레이션 한계 영역에서 우위 입증 | 양자시뮬레이션·응집물질 |
| 9 | A versatile laser-machined rf trap for arrays of 100+ ions | [2607.13342](https://arxiv.org/abs/2607.13342) | 정밀가공 용융실리카 웨이퍼 적층형 rf트랩으로 100개 이상 이온의 1차원·2차원 배열을 유연하게 구성, 설계파일 공개 | 트랩이온 하드웨어 |
| 10 | Wireless millikelvin interconnects for superconducting quantum hardware | [2607.13834](https://arxiv.org/abs/2607.13834) | 초전도 마이크로파 공진기를 밀리켈빈 환경에서 무선으로 동작시켜 극저온 배선 병목 해소 가능성을 실증 | 초전도큐비트·극저온 배선 |
| 11 | Building Shor's Algorithm in Lean: An Agentic Formalization of Quantum Attacks on RSA-2048 and P-256 | [2607.14082](https://arxiv.org/abs/2607.14082) | LLM 에이전트가 Lean에서 Shor 알고리즘을 형식화, RSA-2048·P-256에 대한 기계검증된 논리자원 추정치 제시 | 양자암호분석·형식검증 |
| 12 | Quantum Algorithm for Elliptic Curve Discrete Logarithms with Space-Efficient Point Addition | [2607.13816](https://arxiv.org/abs/2607.13816) | 256비트 타원곡선 이산로그 문제를 835 논리큐비트로 해결하는 공간효율적 모듈러 역원·점덧셈 회로 설계 | 양자암호분석·PQC |
| 13 | Foliated Quantum Error Correction for Qudits | [2607.13784](https://arxiv.org/abs/2607.13784) | 파울리 기반 QEC를 소수차원 큐디트로 확장, 광자기반 측정기반양자계산용 큐디트 토릭코드 등 다수 코드 예시 제시 | 양자오류정정·큐디트 |
| 14 | Clifford-Only Quantum Reed-Solomon Codes and a Tornado Concatenation for Biased-Noise Cat Qubits | [2607.13105](https://arxiv.org/abs/2607.13105) | 편향잡음 cat qubit용 [7,3,5] RS코드 기반 [[21,9,6]] 비트반전 코드와 2계층 Tornado 결합코드로 논리오류율 p⁶ 스케일링 달성 | 양자오류정정·보손큐비트 |
| 15 | Pair-Partition Constructions for CPM-Based Quantum LDPC Codes | [2607.14091](https://arxiv.org/abs/2607.14091) | 순환치환행렬 기반 CSS 양자LDPC 코드를 쌍분할 구조로 구성, girth-6 코드율 0.349·0.440 사례 제시 | 양자오류정정·LDPC |
| 16 | Tensor Network decoding under inter-qubit correlated errors | [2607.13570](https://arxiv.org/abs/2607.13570) | 상관오류 환경에서 다중지표 텐서네트워크 최대우도 디코더를 구성해 기존 MWPM 디코더 대비 우수한 임계값 달성 | 양자오류정정·디코딩 |
| 17 | StreamingQEC: Streaming Quantum Error Correction in Tightly Integrated Quantum-Classical Systems via Certified Recurrence | [2607.13351](https://arxiv.org/abs/2607.13351) | 판독·신드롬전송·디코딩·피드백 자원경쟁을 모델링하는 시스템레벨 QEC 시뮬레이터, 인증된 재귀압축으로 24배 가속 | 양자오류정정·시스템시뮬레이션 |
| 18 | Universal Quantum Computation with Multi-Mode Schrödinger Cat States Stabilized by Non-Local Dissipation Engineering | [2607.13975](https://arxiv.org/abs/2607.13975) | 커 비선형 발진기와 비국소 소산공학으로 다중모드 cat qubit용 범용 게이트셋을 제안, 현실적 매개변수에서 고충실도 검증 | 보손 양자계산 |
| 19 | Deterministic single-electron trapping on solid neon using engineered dielectric surface geometry | [2607.13448](https://arxiv.org/abs/2607.13448) | 네온 표면 아래 유전체층을 선택적 식각해 전자큐비트를 결정론적으로 포획하는 원자평탄 계면 설계, Schrödinger-Poisson 시뮬레이션으로 검증 | 전자큐비트·신규플랫폼 |
| 20 | A robust and modular cesium magneto-optical trap using diverging laser beams | [2607.13145](https://arxiv.org/abs/2607.13145) | 발산형 냉각빔과 모듈형 광섬유 결합 설계로 4×10⁸개 세슘원자 포획, 10μK 이하 온도 달성 | 냉원자·양자센싱 인프라 |
| 21 | Quantum memory advantage for quantum process tomography | [2607.13476](https://arxiv.org/abs/2607.13476) | 결맞음(양자메모리 활용) 프로토콜이 비결맞음 프로토콜 대비 양자채널 학습 쿼리복잡도를 이차적으로 개선함을 증명 | 양자정보이론·토모그래피 |
| 22 | Loophole-Robust Certification of Quantum Advantage | [2607.13090](https://arxiv.org/abs/2607.13090) | "벤치마크 의존성" 개념으로 고전 성능상한을 일반화, IBM 하드웨어 CHSH·Mermin-GHZ 실험에 적용해 인증된 점수 산출 | 양자우월성 인증 |
| 23 | Reshaping quantum annealing landscapes with diagonal catalysts | [2607.14063](https://arxiv.org/abs/2607.14063) | 소규모 좌절없는 부분문제의 바닥상태 패턴으로 ZZ-촉매를 구성, 짧은 어닐링 사이클에서 근접해 확률을 향상 | 양자어닐링 |
| 24 | Events as Spacetime Anchors: Local Irreversibility at the Interface of Quantum Field Theory and Relativity | [2607.13096](https://arxiv.org/abs/2607.13096) | 양자-환경 상호작용이 만드는 국소적 비가역 "사건"을 통해 양자역학과 상대성이론을 잇는 사건중심 프레임워크 제안 | 양자기초론·QFT |

---

## 미수록 논문 목록 (제목만, 48편)

*(초록 미확인, 리스트 순서 기준. 상세 분석이 필요할 경우 개별 요청 시 추가 조사 가능)*

2607.14089 Sail membranes for optomechanical accelerometry, 2607.14085 Benchmarking trigonometric continuous-variable gate primitives with trapped ions, 2607.14083 Cluster-configurational study of G-center in Silicon, 2607.13989 Nonreciprocal Relaxation Acceleration, 2607.13937 Quantum observables for probabilistic classical particles, 2607.13887 A Reservoir Computing Approach to Quantum Gate Synthesis, 2607.13872 Continuous limit of the square well problem in quantum mechanics, 2607.13865 A Lie-algebraic approach to non-Markovian quantum dynamics, 2607.13847 Quantum Topological Data Encoding, 2607.13842 Post-Critical Meson Dynamics of Kibble-Zurek Excitations in a 5,564-Qubit Quantum Annealer, 2607.13827 Inherent interpretability provides inherent value in quantum machine learning, 2607.13809 Markovian evolution from a novel scheme, 2607.13790 Bridging Frustration and Non-Hermiticity via COMPASS: An Adaptive Biorthogonal Neural Quantum State Framework, 2607.13774 A phase transition in the exactness of the NPA hierarchy at the critical doubly-tilted CHSH functional, 2607.13762 No finite level of the NPA hierarchy is exact for the doubly-tilted CHSH functional near the critical tilt, 2607.13722 Towards quantum machine learning for assessing the resilience of post-quantum cryptography, 2607.13699 Machine learning development for quantum computing and neutrino physics, 2607.13641 The potential of quantum computers for Particle Image Velocimetry, 2607.13630 Separating Geometry From Interference in Constrained Quantum Optimization, 2607.13580 Filon Methods for Highly Oscillatory Controlled Quantum Systems, 2607.13512 Basis-Independent Coherence Dynamics of Tripartite States under Pure Dephasing, 2607.13422 Suppressing Detuning-Induced Bias in Ramsey Magnetometry with Composite Pulses, 2607.13404 Deterministic Quantum Phase Estimation with Linear Circuit Complexity in a Photonic System, 2607.13374 A Physics-Grounded QUBO Encoding of Irrigation Scheduling for QAOA, 2607.13366 Quantum annealing in SU(3) multiplet space with nonlocal drivers, 2607.13267 Quantum Motion from Local Transition Susceptibility, 2607.13244 Let the Qudit Do the Jacobi: A Structured Quantum Algorithm for Spectral Decomposition, 2607.13223 Comparing the three W-like states with the W state, 2607.13198 An Information-Theoretic Characterization of Optimal Value-Readout in Response-Register Quantum Oracles, 2607.13191 Two-Tower Quantum Matrix Chain Multiplication: Trading Qubits for Depth, 2607.13166 Robust Nonperturbative Trapped-Ion Quantum Logic, 2607.13150 Emulating XX catalysts for quantum annealing via self-consistent transverse fields, 2607.13135 Classical and quantum mechanics across representations: an operational reading of the Wigner Weyl correspondence, 2607.13131 Ultraviolet structure of entanglement harvesting from energy density and other quadratic couplings, 2607.13062 The verifier side of speculative window decoding: a predictability bracket, a machine-checked blast-radius bound, and a decoder-agnostic recover loop, 2607.13053 On multipoles, their decomposition by time-reversal symmetry, and the electric toroidal monopole, 2607.14056 Acoustic Firewalls: Analogue Gravity Perspective on the AMPS Paradox, 2607.14012 Temporal Entanglement from Twist Correlators in 2d Conformal Field Theory and Holography, 2607.13957 Temporal Fourier Optics Reveals Hidden Hybridized Light-Matter States, 2607.13870 Phonon down-conversion by normal metals for superconducting devices, 2607.13725 An exact algorithm for U(N) matrix models in the gauge-invariant singlet sector, 2607.13664 Direct observation of photon-induced vortices in superconducting films, 2607.13466 PQFA: Parallel Quantum Feature Augmentation of Fused Representations for Multimodal Classification, 2607.13352 HybridQC: Hardware-Grounded Simulation of Tightly Integrated Hybrid Quantum-Classical Systems, 2607.13325 A Reality Check on Quantum Optimisation: Evidence from an Industrial Case Study, 2607.13287 Exactly Solvable Diffraction-Grating Scattering Problems for TE and TM waves, 2607.13134 Magic without a phase: phase-independent stabilizer Rényi entropy in gluon scattering, 2607.09408 Circuit and Krylov complexity of primordial perturbations of modified gravity in inflation

---

## 트렌드 요약

### 이번 주 주요 동향

1. **QKD 보안 사슬의 "약한 고리" 재조명**: 이번 수집일 QKD 관련 논문들은 프로토콜 자체보다 주변 구성요소의 보안 허점에 집중했다. QRNG의 내재적 상관성이 난수량을 46% 과대평가하게 만든다는 결과(2607.13521)와, 다자간 비국소성 인증보다 비밀키 생성이 측정오차에 더 취약하다는 분석(2607.13645)은 모두 "프로토콜 증명은 안전해도 구현 요소가 전체 보안을 무너뜨릴 수 있다"는 공통 메시지를 던진다.

2. **양자네트워크의 인프라·툴체인 성숙**: 측정 전용 평면 아키텍처(2607.13291), 통신파장대 광섬유 결합 단일광자원(2607.13215), 다자간-단일수신 네트워크의 얽힘보조 계산 프로토콜(2607.13756)이 같은 날 함께 등장했다. 개별 소자 실증을 넘어 "네트워크 운영·측정·계산 계층"을 각각 표준화하려는 흐름이 뚜렷하다.

3. **양자오류정정의 다각화**: LDPC(2607.14091), 큐디트 foliated 코드(2607.13784), cat qubit용 Clifford-only RS 코드(2607.13105), 상관오류 대응 텐서네트워크 디코더(2607.13570), 시스템레벨 QEC 시뮬레이터(2607.13351)까지 부호구조·디코딩·시스템통합 전 영역에서 동시다발적 진전이 있었다.

4. **하드웨어 확장성 경쟁**: 300mm 파일럿라인 EUV 리소그래피 실리콘 스핀큐비트(2607.13121), 100개 이상 이온 배열용 범용 rf트랩(2607.13342), 97큐비트 초전도 프로세서 마그논 시뮬레이션(2607.13301)이 각기 다른 플랫폼에서 "대규모화"를 핵심 화두로 다뤘다.

5. **AI 보조 양자암호분석의 부상**: LLM 에이전트가 Lean에서 Shor 알고리즘을 형식화하고 RSA-2048 공격의 기계검증된 자원추정치를 제시한 연구(2607.14082)는, 형식검증과 양자암호분석이 AI 에이전트 워크플로우로 결합되는 새로운 방법론을 시사한다.

---

*Tags: #QuantumCommunication #QuantumNetwork #EntanglementDistribution #QKD #QuantumTeleportation #QRNG #QuantumErrorCorrection #SpinQubits #TrappedIon #SuperconductingQubits #arXiv #quant-ph*
