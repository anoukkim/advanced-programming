# Traveling Salesman Problem (TSP) Solution Using Genetic Algorithm

## 프로젝트 개요
본 프로젝트는 유전 알고리즘(Genetic Algorithm, GA)을 활용하여 외판원 문제(Traveling Salesman Problem, TSP)를 해결합니다. TSP는 모든 도시를 단 한 번씩 방문하고 출발지로 돌아오는 최소 경로를 찾는 NP-Hard 문제로, 본 연구에서는 다양한 교차 연산자와 지역 탐색 기법을 조합한 하이브리드 유전 알고리즘(Hybrid GA)을 구현하였습니다.

- **지도교수**: 윤유림
- **소속**: 가천대학교 컴퓨터공학과, 심화프로그래밍

---

## 주요 내용
- **목적**: GA를 기반으로 TSP 최적 경로 탐색 및 성능 개선
- **사용 기법**:
  - Permutation Encoding
  - Ordinal, PMX, Ordered, Edge Recombination Crossover
  - 2-OPT, 3-OPT, 5-OPT Local Search
- **실험 데이터**:
  - 최적해 데이터: `att48`, `dantzig42`
  - 사용자 정의 데이터: `custom25`, `custom100`
- **결과 요약**: Ordered Crossover와 2-OPT/3-OPT 조합이 최상의 성능을 보임

---

## 결과
64개의 실험을 통해 각 데이터셋에서 최적의 조합과 최단 경로를 확인하였습니다.

### 최적 경로 요약
| 데이터셋       | Crossover + Local Search        | 최단 거리     |
|----------------|----------------------------------|---------------|
| att48          | Ordered Crossover + 2-OPT      | 40,263.04     |
| dantzig42      | Ordered Crossover + 3-OPT      | 726.02        |
| custom25       | Ordinal Crossover + 2-OPT      | 8,645.96      |
| custom100      | Ordered Crossover + 3-OPT      | 29,624.62     |

### 주요 성능 비교
- 기존 연구(37,076.68) 대비 att48 데이터에서는 최적해 거리가 다소 증가하였으나, dantzig42 데이터에서는 기존 연구(929.28) 및 DCGO 알고리즘(771.35) 대비 개선된 결과를 도출하였습니다.
- Local Search 유무에 따라 성능 차이가 크게 발생하였으며, **2-OPT**와 **3-OPT**가 효율적임을 확인하였습니다.

---

## 사용 기술
- 언어: Python
- 개발 환경: Jupyter Notebook
- 라이브러리: NumPy, Matplotlib
