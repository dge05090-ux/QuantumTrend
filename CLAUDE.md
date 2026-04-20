# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with this repository.

## Project Overview

**QuantumTrend**는 arXiv 양자물리(quant-ph) 카테고리의 최신 논문을 수집·분석·정리하는 연구 트렌드 추적 시스템입니다.

- **데이터 소스**: arXiv export API (`export.arxiv.org`)
- **출력물**: Markdown 형식의 날짜별 연구 리포트
- **지식 관리**: Obsidian 볼트 기반

## Claude의 역할

### 1. 연구 수집
- `export.arxiv.org`에서 quant-ph 카테고리 최신 논문 수집
- 우선순위 키워드로 필터링: **Quantum Communication, QKD, Entanglement Distribution, Quantum Network, Quantum Teleportation**

### 2. 논문 분석 및 요약
- Top 5 논문 심층 분석 (기술적 기여, 의의, 응용 가능성)
- 추가 20여 편 논문 요약 및 분류

### 3. 리포트 생성
- 파일명 규칙: `YYYY-MM-DD_Quantum_Research_Report.md`
- 형식: Markdown (Obsidian 호환)

## 자동 실행 시스템

**트리거 ID**: `trig_01XZDMi8fvd5cLNQpTSrpK2r`
**스케줄**: 월~금 오전 10시 (Seoul) / `0 1 * * 1-5` (UTC)
**관리**: https://claude.ai/code/scheduled/trig_01XZDMi8fvd5cLNQpTSrpK2r

### 수집 기준
| 실행 요일 | 수집 대상 날짜 |
|---|---|
| 월요일 | 지난 금요일 자료 |
| 화~금요일 | 전날 자료 |

### 실행 흐름
1. arXiv API에서 quant-ph 논문 200편 수집
2. 우선순위 키워드로 필터링
3. Top 5 심층 분석 + 추가 20편 이상 요약
4. `YYYY-MM-DD_Quantum_Research_Report.md` 생성
5. `git commit -m "research trend analysis"` 후 push

## 현재 상태

- 자동 실행 트리거 활성화됨 (2026-04-20 설정)
- GitHub 연동 완료: `https://github.com/dge05090-ux/QuantumTrend.git` (push 정상)
- 전체 프로세스 테스트 완료 (2026-04-20)
- 데이터 저장 및 검색: Markdown 파일 + Obsidian 볼트 기반 운용 중
- 생성된 리포트: `2026-04-18_Quantum_Research_Report.md`, `2026-04-17_Quantum_Research_Report.md`
