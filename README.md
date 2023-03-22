# Instacart 고객 세분화 및 재구매 강화석분석

## 프로젝트 개요

---

온라인 배달 시장의 성장이 지속되면서 단순히 음식 배달을 넘어 온라인으로 장을 보고 배달을 받는 온라인 장보기 서비스가 일반화 되고 있다. 그리고 단순한 배달을 넘어 장을 본지 1~2시간 내 배송을 지원하는 `퀵커머스` 가 대두되고 있다. 

국내의 경우 대형마트를 필두로 유통계의 대기업부터 편의점까지 빠른 배송 서비스를 진행한다. 최근 GS리테일은 새벽 배송 서비스를 중단하고 즉시 배송 서비스를 런칭하였듯 많은 기업이 퀵커머스 시장을 선점하기 노력중이다. 

하지만 아직 배송이나 물류 창고 등에 막대한 투자 비용이 든다. 단기적으로 큰 수익성을 기대할 수 없는 것도 문제다. 퀵커머스는 생필품 등이 주요 상품이다. 상대적으로 마진이 높지 않다. 경쟁자가 많아질수록 '더 싸게 더 빠르게' 팔아야 하는 딜레마에 빠질 수 있다.

따라서 퀵커머스를 지향하는 기업은 낮은 비용과 고객을 유치하고 유지하는 전략을 세우는 것이 필수이다. 본 프로젝트는 미국, 캐나다의 대표적인 식료품 배송 서비스 기업인 Instacart의 데이터를 분석하여 고객의 구매행태를 분석하고 고객을 세분화 하여서 재구매 고객 유지를 위한 서비스를 제안하고자 한다.

Instacart와 국내 기업들의 수익 구조적 차이는 존재하지만 Instacart의 데이터 분석을 국내 배송 서비스에 접목시켜 대형마트가 아닌 일반 소매점의 배달서비스를 담당하는 회사에도 적용을 할 수 있도록 프로젝트를 진행할 것이다.

## Instacart

---

- 개요
    - 온라인 기반 농작물 및 식료품 배송 서비스이다.
    - 안드로이드, iOS, 그리고 별도로 마련된 웹사이트를 통해 서비스가 제공된다.
    - 사업에 진행됨에 따라 기존에 점포를 소유하고 있는 식품 회사들과 관계를 맺어가고 있으며 이에 따라 인스타카트 사용자들이 점포 가격에 따라 구입할 수 있다.
- 고객층
    - 맞벌이 부부, 1인 가구, 거동불편 등등
    - 코로나 이후 고객층이 늘어남 → 고객의 성향에 따른 분류가 필요
- 수익원
    - 배달 수수료 : 가장 기본적인 수익원
    - 소매업체 partnership : partner fees, placement fees
    - non partner markup
- 특징 및 강점
    - 3 무 → `물류창고x, 재고x, 트럭x` → 비용감소
    - 다양한 소매업체와 제휴 및 협력 → 경쟁이 아닌 `win-win`관계
    - 대형 마트의 독과점적 구조와 대비
    
## 문제 설정

---

1. 고객 세그맨테이션
    - (코로나 이전) 맞벌이 부부, 1인 가구, 거동불편한 고객 등 직접 장보기 불편한 그룹이 예측
    - (코로나 이후) 물리적으로 장보기 한계 → 많은 고객층 유입 →  고객의 성향에 따른 분류가 필요
    - 주문 상품 군에 따라 새로운 고객그룹이 설정될 것이다
2. 재구매 강화 문제
    - 새로운 그룹 별 유의미한 주문 행태의 차이가 있을 것이다.
    - 그룹 별 주문 성향을 바탕으로 특성을 파악하고 재구매를 유도할 상품군을 추천할 수 있다.
3. 구매 강화를 위한 방안
    - 요일과 시간대 별 주문량의 차이가 있을 것이다.
    - 재구매 상품의 경우 구매주기가 존재할 것이다
4. 한국 시장 적용방안
    - 대형 마트들이 각자의 퀵커머스 서비스를 진행하기에 진입장벽이 높다.
    - 인근 다른 소매점과 연계 → 하나의 소매점이 아닌 다수의 소매점 쇼핑 가능
    - 슈핑, 로마켓 등 동네 거점 소매점과 연계한 회사에 적용
    
    
## 과정

---

- 데이터 정제 및 시각화를 통한 고객 구매 패턴 분석
    - 상위 판매 상품 / 요일, 시간별 주문량 / 재주문 주기
- PCA 및 KMeans Clustering을 통한 고객 세분화
    - 4개의 그룹 생성
- 고객 그룹별 특성 파악
    - 육아를 하는 특수 그룹 특정 → 유아용품 추천

## 결과

---

- **고객 구매패턴과 특성에 따른 판매젼략 제시 / 국내 소형 마트와의 연계방향 제시**
