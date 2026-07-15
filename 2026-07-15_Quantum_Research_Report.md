# Quantum Research Report — 2026-07-15 (Wednesday)

> **수집 기준**: 2026-07-14 (화) arXiv quant-ph 신규 논문
> **생성일**: 2026-07-15 (수)
> **수집 논문 수**: 129편 (2026-07-14 제출분) — Top 5 심층 분석 + 대표 27편 요약 (총 32편 수록)
> **우선순위 키워드**: Quantum Communication, QKD, Entanglement Distribution, Quantum Network, Quantum Teleportation

> **비고**: `export.arxiv.org/api/query`(주 수집 경로)를 WebFetch로 조회한 결과, 검색 인덱스 지연으로 2026-07-13 제출분까지만 반환되어(2026-07-14 제출분 누락) CLAUDE.md 지침에 따라 `arxiv.org/list/quant-ph/recent` 대체 경로로 전환, 페이지네이션(`?skip=`)을 통해 2026-07-14 제출분 전체 129편의 목록을 확보했다. 이번 수집일은 평소(40~60편) 대비 논문 수가 이례적으로 많아(129편), 전량 초록 확보 대신 우선순위 키워드 매칭 논문(6편, Top 5 + 1편)과 하드웨어·알고리즘·이론 전반을 아우르는 대표 논문 27편을 선별해 초록을 확인·요약했다. 나머지 논문 목록은 리포트 하단에 제목만 전체 수록한다.

---

## Top 5 심층 분석

### 1. Deploying and validating a metropolitan QKD secure network: architecture and field performance
**arXiv**: [2607.11727](https://arxiv.org/abs/2607.11727)
**저자**: Claudia De Lazzari, Nicola Biagi, Damiano Giani, Marco Russo, Fernando Chirici, Francesco Stocco, Saverio Francesconi, Giacomo Ferranti, Alessandro Soureal, Antonella Sanguineti, Bartolomeo Montrucchio, Christian Laurenzi, Oliviero Testa, Guglielmo Morgari, Antonio Manzalini, Tommaso Occhipinti, Alessandro Zavatta, Davide Bacco
**키워드**: QKD / Quantum Network (대도시 규모 QKD 상용망 구축·검증)

#### 기술적 기여
밀라노 데이터센터 간 실제 설치 광섬유망 위에 QKD 하드웨어, 표준 규격 키관리(KM), 중앙집중형 SDN 오케스트레이션을 통합한 계층형 아키텍처를 구축했다. 능동 광스위칭과 신뢰노드 라우팅을 통한 동적 경로 재구성으로 자동 장애복구를 구현했으며, 다양한 프로토콜·워크로드에 걸친 응용계층 검증으로 전체 시스템 구성요소의 상호운용성을 확인했다.

#### 의의
양자컴퓨터의 등장이 기존 공개키 인프라에 실존적 위협이 되는 상황에서, 대도시 규모 QKD망이 실험실 단계를 넘어 상용 배치가 가능한 기술·운영적 성숙도에 도달했음을 실증한 재현 가능한 청사진을 제시했다.

#### 응용 가능성
- 금융·정부기관용 대도시권 양자보안 통신 인프라
- SDN 기반 QKD망 오케스트레이션 표준화
- 다중 벤더 QKD 장비의 상호운용성 검증 플랫폼

---

### 2. Deployment of Entanglement-Based QKD in Financial Infrastructure
**arXiv**: [2607.11252](https://arxiv.org/abs/2607.11252)
**저자**: Mirela Selimović, Roman Solar, Jonathan Gruner, Sebastian Mair, Mario Wenzl, Thomas Heine, Matej Pivoluska, Rupert Ursin, Sebastian Philipp Neumann
**키워드**: QKD / Entanglement Distribution (얽힘기반 QKD의 금융 인프라 실증)

#### 기술적 기여
22km, 8dB 손실 광섬유로 연결된 두 데이터센터 간 편광 얽힘 기반 QKD를 4개월간 연속 운용해 평균 63.8kb/s의 보안키를 생성하고 이를 VPN 암호화 연결에 통합했다. 총 가동률 93.7%(양자광학 부품 기인 다운타임 0%), 측정기간의 97.4%에서 QBER 2% 미만을 능동 편광보정으로 유지했으며, 얽힘광자의 고유 타이밍 특성만으로 외부 기준신호 없이 300피코초 이하 정밀도의 동기화를 달성했다.

#### 의의
얽힘기반 QKD가 실험실이 아닌 실제 은행 운영 환경에서 장기간 안정적으로 작동함을 정량적으로 실증한 드문 사례로, 얽힘분배 기술의 상용 금융 인프라 적용 가능성을 구체적 수치로 뒷받침한다.

#### 응용 가능성
- 은행 간 데이터센터 보안 연결의 양자키 기반 VPN
- 외부 기준신호 없는 저비용 양자동기화 시스템
- 장기 무보정 운용이 필요한 상용 얽힘기반 QKD 장비

---

### 3. Asymmetry-aided measurement-based quantum repeaters and distributed quantum computing with a decoder-free client
**arXiv**: [2607.11238](https://arxiv.org/abs/2607.11238)
**저자**: Wooyeong Song, Sungyeon Kook, Wonhyuk Lee, IlKwon Sohn
**키워드**: Quantum Network / Quantum Communication (측정기반 양자중계기와 분산양자컴퓨팅 통합 설계)

#### 기술적 기여
손실이 큰 광네트워크를 통한 논리큐비트 전송과 분산 양자연산을 별개가 아닌 통합계로 취급, "측정기반 양자중계기는 전송축을 따라 폴딩된 2차원 부호"라는 통찰로 채널손실을 전송 섹터에 집중시키고 국소 측정 큐비트를 보호한다. 이 구조적 비대칭에 맞춘 직사각형 Bacon-Shor 부분계 부호를 사용해, 대륙 간 거리에서 [[48,6,8]] 벤치마크 부호 대비 약 10분의 1의 중계기 밀도, 동급 대칭 부호 대비 약 절반의 자원만으로 전송 효율을 크게 개선했다.

#### 의의
전송과 연산을 분리하지 않고 통합 설계함으로써 양자중계기 네트워크의 자원 효율을 근본적으로 개선했으며, 중앙집중형 디코딩을 통해 클라이언트측 처리 부담을 낮춘 양방향 통신 구조로 확장 가능성을 제시했다.

#### 응용 가능성
- 대륙 간 양자인터넷 백본의 중계기 자원 최적화
- 디코더 경량화가 필요한 클라이언트-서버형 분산양자컴퓨팅
- 코드레벨 스위치를 활용한 양방향 양자통신 아키텍처

---

### 4. Security of passive entanglement-based key distribution protocols
**arXiv**: [2607.10659](https://arxiv.org/abs/2607.10659)
**저자**: Shun Kawakami, Koichi Takasugi, Koji Azuma
**키워드**: QKD / Entanglement Distribution (수동형 측정기저 얽힘기반 QKD의 보안증명)

#### 기술적 기여
BBM92, QCKA 등 얽힘기반 키분배 프로토콜에서 널리 쓰이는 수동형(passive) 측정기저 선택 방식에 대해, 비대칭 기저 선호도를 갖는 경우까지 포함한 보안성을 증명했다. 기존 분석기법이 잘 적용되지 않던 이 설정에 대해 다자간 양자회의키합의로도 분석을 확장했으며, 수치해석으로 수동형 BBM92가 능동형과 대등한 키생성률을 달성함을 보였다.

#### 의의
실제 구현에서 선호되는 단순화된 수동형 측정 장치의 이론적 보안 공백을 메워, 얽힘기반 QKD의 실배치에 필요한 이론적 정당성을 제공했다.

#### 응용 가능성
- 능동 기저전환 장치가 불필요한 저비용 QKD 수신단 설계
- 다자간 양자회의키합의 프로토콜의 실용 구현
- 수동형 측정 기반 상용 얽힘분배 네트워크 노드

---

### 5. Noise Resilience of Quantum Key Distribution Protocols Secured Against Independent Attacks With One-Way Communication
**arXiv**: [2607.11857](https://arxiv.org/abs/2607.11857)
**저자**: Adam Bílek, Ryszard Kukulski, Paulina Lewandowska, Łukasz Pawela, Zbigniew Puchała
**키워드**: QKD (단일큐비트 QKD 프로토콜의 잡음 내성 비교)

#### 기술적 기여
독립 도청공격에 대해 단방향 고전통신으로 키 증류를 수행하는 단일큐비트 QKD 프로토콜(BB84, B92, E91, 6상태)의 환경잡음 내성을 평가하는 새로운 잡음기반 효율성 지표를 도입했다. 점근적으로 안전한 비밀키 증류가 가능한 잡음 임계값을 규명했으며, 6상태 프로토콜이 가장 높은 잡음 내성과 함께 다른 프로토콜보다 우수한 사후선택 효율을 동시에 달성함을 보였다.

#### 의의
QBER이라는 전통적 척도를 넘어선 새 잡음지표로 프로토콜 간 실질적 성능을 정량 비교함으로써, 잡음 환경에서의 QKD 프로토콜 선택에 실용적 근거를 제공했다.

#### 응용 가능성
- 잡음이 큰 실환경 채널에서의 QKD 프로토콜 선정 가이드라인
- 6상태 프로토콜 기반 고잡음 내성 QKD 시스템 설계
- QBER 대체 잡음지표를 활용한 QKD 성능 벤치마킹

---

## 추가 논문 요약 (27편)

| # | 제목 | arXiv ID | 주요 내용 | 분류 |
|---|------|----------|-----------|------|
| 6 | Device-independent certification of tripartite quantum networks with bilocal Bell inequalities | [2607.09933](https://arxiv.org/abs/2607.09933) | 두 독립 소스가 이분상태를 세 관측자에 분배하는 네트워크용 비선형 벨부등식 구성, 최대양자값의 해석적 결정 및 소스·측정 전체에 대한 최초의 순수 비국소성 기반 자체검증 결과 제시 | Quantum Network·디바이스독립 인증 |
| 7 | An efficient algorithm for approximate shadow Hamiltonian simulation | [2607.11882](https://arxiv.org/abs/2607.11882) | 그림자 해밀토니안 시뮬레이션에서 연산자대수의 불필요 원소를 가지치기해 목표 관측량에 중요한 연산자에 집중, 큐비트 레지스터 크기를 대폭 절감 | 양자시뮬레이션 알고리즘 |
| 8 | Trotter error compensation with polylogarithmic precision and nested-commutator scaling without ancillas | [2607.11856](https://arxiv.org/abs/2607.11856) | 보조큐비트 없이 회로크기에 대해 다중로그 정밀도를 갖는 HNCC 알고리즘 제안, 게이트수를 크게 절감하는 해밀토니안 시뮬레이션 기법 | 해밀토니안 시뮬레이션 |
| 9 | Optimal tomography of bosonic and fermionic Gaussian states | [2607.11847](https://arxiv.org/abs/2607.11847) | 보손·페르미온 가우시안 상태를 모드수에 이차식으로 스케일링하는 복사본 수만으로 학습 가능함을 규명, 순수/혼합 상태 및 에너지 제약 없이 성립하는 오랜 미해결 문제 해결 | 양자상태 토모그래피 |
| 10 | Optimal operating temperature for industry-compatible silicon spin quantum computing: colder is not necessarily better | [2607.11846](https://arxiv.org/abs/2607.11846) | 실리콘 스핀큐비트가 최저온이 아닌 유한한 최적온도(약 1K 부근)에서 최고 효율을 보임을 실측·모델링으로 규명, 대규모화를 위한 전력·오류정정 트레이드오프 제시 | 스핀 큐비트 실험 |
| 11 | Input-Aware Dynamic Backdoor Attack Against Quantum Neural Networks | [2607.11843](https://arxiv.org/abs/2607.11843) | 입력에 따라 적응적으로 변하는 트리거를 사용하는 최초의 입력인지형 동적 백도어 공격 Q-DIBA 제안, 고정패턴 탐지 방어를 우회 | 양자머신러닝 보안 |
| 12 | Multiparameter Quantum Metrology in Molecular Dimers | [2607.11831](https://arxiv.org/abs/2607.11831) | 쌍극자 상호작용 분자계에서 온도·디튜닝 동시추정이 개별추정보다 근공명·저온영역에서 우수함을 규명, 온도가 측정정밀도의 핵심 변수임을 확인 | 양자계측 |
| 13 | Private Capacity of Quantum Channels Induced by Non-stabilizer Environmental States | [2607.11793](https://arxiv.org/abs/2607.11793) | 안정자 환경상태를 가진 채널은 비밀통신용량이 0이지만 특정 마술상태는 0이 아닌 비밀용량을 가능케 함을 규명, 마술자원과 통신보안의 연결고리 제시 | 양자정보이론·통신용량 |
| 14 | Quantum Arithmetic Circuits in Public-Key Cryptography | [2607.11713](https://arxiv.org/abs/2607.11713) | 암호해독용 양자산술회로 설계를 종합 검토, 측정기반 비계산화 등 자원효율화 기법으로 공개키암호에 대한 양자위협을 현실적으로 평가 | 양자암호해독 |
| 15 | Multi-Stage Mamba-Based Architecture for Fast and Scalable Superconducting Qubit Readout | [2607.11668](https://arxiv.org/abs/2607.11668) | Mamba 모델 기반 큐비트 상태판별 기법으로 판독 충실도를 높이면서 모델 파라미터 수를 대폭 줄이고 입력 길이 변화에도 강건함을 실증 | 초전도큐비트 판독·머신러닝 |
| 16 | A diode nanocavity for fast, efficient and tunable emission of highly entangled photon pairs and Fourier-transform-limited single photons | [2607.11494](https://arxiv.org/abs/2607.11494) | 반도체 양자점 다이오드 나노공동으로 고얽힘 광자쌍과 구분불가능 단일광자를 고효율·저잡음으로 동시 생성하는 실용 플랫폼 구현 | 광자소스·양자광학 |
| 17 | Toward Quantum Utility in Correlated Topological Matter: Variational Preparation of Fractional Quantum Hall Manifolds | [2607.11380](https://arxiv.org/abs/2607.11380) | 근시일 양자프로세서에서 변분양자알고리즘으로 분수양자홀 상태를 준비·특성화, Haldane 구/원환면 기하에서 하이브리드 방법의 재구성 성능 검증 | 변분양자알고리즘·위상물질 |
| 18 | Barium-based Rydberg atom quantum technologies with long Rydberg coherence | [2607.11282](https://arxiv.org/abs/2607.11282) | 바륨 원자의 2광자 여기 리드버그 상태가 도플러 제한 결맞음저하를 극복하면서 강한 상호작용을 유지, 장수명 리드버그 폴라리톤 생성 | 리드버그원자 양자기술 |
| 19 | When cheap gradients fail: the measurement cost of attacking quantum classifiers | [2607.11095](https://arxiv.org/abs/2607.11095) | 양자측정잡음이 변분양자분류기를 경사도기반 공격으로부터 내재적으로 방어함을 규명, 차원의존 측정예산이 고전 최적화비용보다 급격히 증가해 화이트박스 공격비용을 높임 | 양자머신러닝 보안 |
| 20 | The quantum coherence as a phase property of the wave function | [2607.10958](https://arxiv.org/abs/2607.10958) | 결맞은 전자기장과 상호작용하는 다준위 드레스드 상태의 위상상관관계로 양자결맞음을 재해석, 실재/가상 성분 간 급속 진동 상관과 가상성분 간 정상 상관 두 유형 규명 | 양자기초론·결맞음 |
| 21 | Quantum-enhanced physical-layer threat detection in metropolitan-scale fiber networks | [2607.10799](https://arxiv.org/abs/2607.10799) | 압착광을 이용해 광신호에 양자적 특징을 내장, 고전적 분석만으로 위협을 탐지하는 실용적 네트워크 보안기법을 실제 대도시권 광망에 배치·검증 | 양자강화 네트워크보안 |
| 22 | Model-Driven Digital Twin Framework for Quantum Networks | [2607.10367](https://arxiv.org/abs/2607.10367) | 모델기반공학(MDE)으로 양자네트워크의 통합·재사용 가능한 디지털트윈 구축, SysML v2·QKD kit 활용 개념검증 사례 제시 | 양자네트워크 엔지니어링 |
| 23 | Fast and accurate AI-based pre-decoders for color codes | [2607.10058](https://arxiv.org/abs/2607.10058) | 삼각형 색부호용 신경망 기반 사전디코더로 코드거리 31에서 논리오류율 347배 개선, 실행시간 7.33배 단축을 동시 달성해 표면부호와의 성능격차 축소 | 양자오류정정·디코더 |
| 24 | Moment-Structured Block Encodings of Periodic Finite-Difference Operators | [2607.11596](https://arxiv.org/abs/2607.11596) | 병진불변 유한차분연산자의 블록인코딩을 증명 가능한 최적 부분정규화로 구성하는 프레임워크 제시, 기존 최적구성을 포괄하며 이중조화연산자 등 고차연산자로 확장 | 양자알고리즘·PDE |
| 25 | High-field Josephson effect enabled by a moiré Hofstadter spectrum | [2607.11721](https://arxiv.org/abs/2607.11721) | 모아레 패턴 그래핀 접합이 6테슬라까지 초전도 위상결맞음을 유지함을 실증, 모아레 퍼텐셜이 란다우준위를 분산띠로 변환해 양자홀 영역까지 조셉슨 간섭을 확장 | 초전도·모아레물리 |
| 26 | Layer-Resolved Topological Metals in the Bilayer Lieb Lattice | [2607.11009](https://arxiv.org/abs/2607.11009) | 양자화된 층분해 유사스핀 천수를 갖는 새로운 위상금속상을 이중층 Lieb격자에서 규명, 궤도각운동량 결합이 위상반금속을 층별 위상특성을 보존한 금속으로 전환 | 위상물질이론 |
| 27 | Quantum Chaos with a Macroscopic Zero-Mode Sector | [2607.09504](https://arxiv.org/abs/2607.09504) | 카이랄대칭을 갖는 제약형 스핀사슬에서 지수적으로 큰 대칭보호 완전제로모드 다양체가 카오스적 준위반발로 나머지 스펙트럼과 간극을 이룸을 규명, 카오스계 스펙트럼 조밀성 통념에 도전 | 양자카오스·다체이론 |
| 28 | Paraparticles intrinsically exhibit Hardy-space breakdown | [2607.11867](https://arxiv.org/abs/2607.11867) | 비유니터리 교환통계를 갖는 파라입자가 외부 욕조와 결합 시 메모리 커널의 Hardy공간 해석성(크라머스-크로니히 관계)을 근본적으로 위반함을 규명, 페르미온·보손과의 근본적 차이 규명 | 양자장론·통계이론 |
| 29 | Bounding Kirkwood-Dirac negativity of Gaussian processes | [2607.11854](https://arxiv.org/abs/2607.11854) | 가우시안 과정을 겪는 양자상태의 커크우드-디랙 음성도 상한을 유도, 가우시안 상태가 비고전성의 극단값 달성에 충분하며 직교좌표 고유상태가 이 한계를 포화함을 규명 | 양자기초론·비고전성 |
| 30 | Operational Concealment of Measurement Incompatibility by Quantum Channels | [2607.11762](https://arxiv.org/abs/2607.11762) | 측정 비호환성이 양자채널 통과 시 수학적으로는 유지되면서도 관측상 은폐될 수 있음을 인접커널 틀로 규명, 정량적 척도와 구조적 분류체계 제시 | 양자측정이론 |
| 31 | Connectivity-induced surface-loss penalty in superconducting qubit-coupler lattices | [2607.10743](https://arxiv.org/abs/2607.10743) | 격자구조 큐비트 연결이 표면유전손실을 1.3~1.8배 증가시킴을 시뮬레이션으로 규명, 다중큐비트 프로세서의 손실 최소화 설계지침 제시 | 초전도큐비트 하드웨어 |
| 32 | Interlocked Time Crystal in Coupled Spin-1/2 Ensembles under Local Dissipation | [2607.11717](https://arxiv.org/abs/2607.11717) | 펌프-감쇠 불균형이 반대인 두 스핀-1/2 앙상블을 결합해 복잡한 다준위 부분계 없이도 "결합형 시간결정" 진동질서를 생성 | 비평형양자상·시간결정 |

---

## 미수록 논문 목록 (제목만, 97편)

*(초록 미확인, 제목 기준 arXiv ID 순서. 상세 분석이 필요할 경우 개별 요청 시 추가 조사 가능)*

2607.11867, 2607.11856(수록), 2607.11854(수록), 2607.11831(수록), 2607.11829 Quantum probe advantage in learning many-body systems, 2607.11823 Multiparameter Quantum Estimation in a Raman-Coupled Two-Qubit System, 2607.11774 A new class of pure non-Gaussian quantum states, 2607.11759 Higher-order covariance matrices for non-Gaussian quantum states, 2607.11637 From Circuits to Hardware: Benchmarking Standard and Qubit-Efficient Quantum Optimization on Real Hardware, 2607.11580 Classical probabilistic realisation of quantum double-slit interference, 2607.11516 Quantum Simulation of Strongly Correlated Fermion-Phonon Models in Circuit QED, 2607.11514 States dressing analysis in a transmon-transmon-bus system, 2607.11490 AtomFlow: An End-to-End FPGA-Based Control Architecture for Neutral Atom Quantum Computers, 2607.11483 Strong Zero Modes in Supersymmetry-Inspired Quantum Circuits, 2607.11454 Tunable non-Hermitian skin effect and topological phases in ladders with staggered nonreciprocal inter-leg hopping, 2607.11410 Quantum algorithms for second-order boundary value problems, 2607.11401 From Leaves to Clusters: Depth-Efficient SAT-Oracle Synthesis Based on the HRSE Model, 2607.11393 Symmetry tests for cyclic groups with quantum linear optics, 2607.11369 Moment-based PPT criteria for random bipartite states, 2607.11315 Controlling the Inhomogeneous Broadening and Impedance Matching of a Spin Ensemble, 2607.11302 Information geometric quantification of effective privacy in quantum metrology, 2607.11284 Experimental Observation of Anomalous Complementary Weak Values from Correlated Pairwise Two-State Vectors, 2607.11273 Fixed-Protocol Amortized MPS Tomography with Conformalized Predictive Uncertainty, 2607.11234 Which Classicality? Incidence, Simplex, and Product-Rule Tests in Finite Quantum Logics, 2607.11217 Quantum Multiscale Modeling: A Hierarchy of Algorithms for Complex Chemical Systems, 2607.11216 Distributed Semantics for Distributed Quantum Computing, 2607.11206 Unique temporal scaling dimension for quantum criticality in open systems weakly coupled to environment, 2607.11201 Dynamics of two interacting dipolar two-level systems in a multi-mode electromagnetic cavity, 2607.11174 Lie-Algebraic Subspace Quantization for Zero-Shot Quantum Learning and Barren-Plateau Mitigation, 2607.11137 Decoherence of a quantum magneto-oscillator, 2607.11038 Many-Body Physics with Rydberg Atoms, 2607.11013 Overcoming Fourier Locking in Quantum Data Re-uploading Classifiers via Spectral Homotopy, 2607.10950 p-Form Gauge Dynamics and Digital Quantum Simulation, 2607.10946 Randomized Quantum Optimal Control, 2607.10899 Driven Quantum Stars as Controlled Primitives for Real-Time Spin Dynamics, 2607.10867 GroupFunctions.jl, 2607.10772 Demonstrating Quadratic Monte Carlo Speedup via Quantum Amplitude Estimation, 2607.10765 Spectral gap of Lee-Yang Hamiltonians, 2607.10714 Nonlocal nonstabilizerness for slightly entangled quantum many-body states, 2607.10707 MDQEC-QAS: Meta-Decoding for Quantum Error Correction, 2607.10704 Passive spectral-admittance bounds for quantum-memory interfaces, 2607.10656 Learning Topological Quantum Phases from Limited Subsystems, 2607.10632 Semiclassical asymptotics of multiphotonic scattering probabilities, 2607.10563 The Virtuous Cycle of Quantum-Classical Machine Learning, 2607.10550 Coherent Quantum Schrodinger Bridge, 2607.10518 General Quantum Limit for Minimum Measurable Frequency Shift in Lasers, 2607.10473 Quantum algorithm for Clifford multiplication, 2607.10414 Optimal Average Success Probabilities of Binary Quantum Random Access Codes, 2607.10360 Gram-Certified Resource Continuation for Quantum Representation Audits, 2607.10334 Static entanglement structure and adiabatic Bell-state preparation, 2607.10284 Rank-Refined Quantum-Behaved Particle Swarm Optimization, 2607.10283 Resolvent algebras and limit states of interacting canonical ensembles, 2607.10281 Nonlocal Manipulation of Backflow with Quantum Correlations, 2607.10280 Scaling Adaptive Non-Local Observable Quantum Super-Resolution, 2607.10274 Efficient Circuit Transpilation of Commuting Gates on 2D Grids, 2607.10273 Certified quantum supremacy in entanglement-assisted codes, 2607.10262 HSF-S: Speed-Optimized Compilation for Quantum Circuit Emulation, 2607.10249 Branch-resolved Pauli-block spectroscopy of two-qubit gates, 2607.10227 Code-space recovery for sample-based quantum diagonalization, 2607.10218 From local weight selection to Zeno slowdown in Su-Schrieffer-Heeger chain, 2607.10118 Hamiltonian Conditions for Dark Modes in Multimode Bosonic Systems, 2607.10083 Unified Phase-Space Mapping of Quantum Observables in Multi-Driven Vapor, 2607.10057 Quantum Circuit Vision: Cost-Aware Evaluation of Visual AI Agents, 2607.10055 Measurement-induced overconcentration in quantum generative models, 2607.09976 GPU-Accelerated Dead-Measurement Detection in Hybrid Programs, 2607.09927 Transferred QAOA Parameters and Penalty Scale Resonance, 2607.09912 Heterodyne position detection of an optomechanical system, 2607.09906 Depth-Efficient Quantum Topological Data Analysis for Financial Stress, 2607.09905 Quantum vs Classical Reservoir Computing Performance Comparison, 2607.09893 End-to-End Hybrid Quantum-Classical Sampling for Markov Fields, 2607.09882 Benchmarking Zero-Setup Quantum Circuit Simulators, 2607.09875 Revealing Entanglement-Growth Mechanisms through the Magic Barrier, 2607.09857 Gauge-invariant thermodynamics of a finite-time quantum Otto engine, 2607.09855 Ergotropic and passive contributions in Gaussian state geometry, 2607.09844 Hardware-efficient quantum simulation of intense-field QED, 2607.11768 Spacer-Mediated Gold Nanocube Arrays for Edge-Localized Excitonic Enhancement in Monolayer MoS2, 2607.11665 The Time-Space Complexity of Checking Multiple Assertions in Quantum Programs, 2607.11647 Anomalous Dissipation in Current Biased Josephson Systems, 2607.11641 Holographic Timelike Entanglement and Subregion Complexity in Localized AdS3*S3*T4 Black Holes, 2607.11554 Robust Spin Qubit Coupler via Minimal Kitaev Chain, 2607.11135 Molecular Dynamics-Derived Coloured Noise Mediates Anderson Localisation, 2607.11048 Spectroscopy of low-lying valley states in hot Si/SiGe quantum dots, 2607.11003 Ferroelectric--Superconducting Interaction in Epitaxial YBa2Cu3O7-δ/BaTiO3 Films, 2607.11000 Non-Abelian holonomic transformations in digitally coupled acoustic waveguides, 2607.10996 Analytical mobility edge in nonreciprocal quasiperiodic lattices, 2607.10924 A Cluster-Based Model of the Spectrum of Erbium-Doped GdVO4, 2607.10921 Krylov Complexity from Loschmidt Amplitude, 2607.10847 Thawed Gaussian Ehrenfest dynamics, 2607.10737 Accessing 100 GHz Mechanical Modes in Bulk Crystals at Cryogenic Temperatures, 2607.10663 Certified boundary-magic witness for state-dependent proto-area, 2607.10454 Krylov Complexity for Time-Dependent Hamiltonians, 2607.10415 Phase-controlled transport of Floquet-driven compact topological photonic states, 2607.10347 A Framework for Managing the Models of Engineered Quantum Systems, 2607.10181 Anyons and Inherently Complex F-symbols, 2607.09997 Scalar and vector bosons in a Bonnor-Melvin-Λ spacetime, 2607.09896 Dark Optical Trapping of Resonant Transition-Metal Dichalcogenide Particles, 2607.09819 The New Tractatus Program, 2607.09769 Challenges in the simulation of enzymatic transition states, 2607.09728 Quantum Thermodynamics of Electron Transport along Chains of Redox Centers

---

## 트렌드 요약

### 이번 주 주요 동향

1. **QKD·양자네트워크 논문의 이례적 급증과 "실배치 검증" 중심 이동**: 2026-07-14 제출분 129편 중 QKD/양자네트워크 직접 관련 논문이 6편 확인되었으며, 그중 상위 2편(2607.11727 밀라노 대도시 QKD망, 2607.11252 은행 인프라 얽힘기반 QKD)은 모두 실험실 시연이 아닌 실제 상용 인프라에서의 수개월 단위 현장 운용 데이터를 제시했다. QKD 연구의 무게중심이 "프로토콜 제안"에서 "현장 검증·상용화"로 이동하고 있음을 시사한다.

2. **양자중계기 설계 패러다임의 전환**: 측정기반 양자중계기 연구(2607.11238)는 전송과 연산을 분리된 문제로 다루던 기존 접근에서 벗어나 통합계로 재정식화, 비대칭 부호구조로 자원효율을 10배 가까이 개선했다. 양자인터넷 인프라 설계의 근본적 재검토가 진행 중임을 보여준다.

3. **수동형(passive) 측정 장치의 이론적 정당화 완성**: 얽힘기반 QKD의 수동형 기저선택 보안증명(2607.10659)은 실제 구현에서 선호되지만 이론적 공백이 있던 방식을 뒷받침해, 저비용 QKD 수신단 상용화의 이론적 걸림돌을 제거했다.

4. **양자머신러닝 보안(적대적 공격)의 양방향 연구 심화**: QNN 백도어 공격(2607.11843)과 QNN 분류기 경사도공격 방어(2607.11095)가 같은 날 나란히 발표되어, 양자머신러닝의 공격·방어 연구가 공진화하고 있음을 보여준다.

5. **디바이스독립 자체검증의 다자간 네트워크 확장**: 삼자간 양자네트워크에 대한 순수 비국소성 기반 최초의 자체검증 결과(2607.09933)는 벨부등식 위반만으로 소스와 측정장치 전체를 인증하는 디바이스독립 검증 이론이 점대점 통신을 넘어 네트워크 토폴로지로 확장되고 있음을 시사한다.

6. **실리콘 스핀큐비트의 "운용온도" 최적화 논의 부상**: 최저온이 최선이 아니라는 실측 결과(2607.11846)는 대규모 양자프로세서의 냉각비용·오류정정 트레이드오프를 재고하게 하는 실용적 함의를 갖는다.

---

*Tags: #QuantumCommunication #QuantumNetwork #EntanglementDistribution #QKD #QuantumTeleportation #QuantumCryptography #QuantumRepeater #DeviceIndependent #SpinQubits #SuperconductingQubits #arXiv #quant-ph*
