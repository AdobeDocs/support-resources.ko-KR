---
title: Adobe Commerce 휴일 준비 개요
description: 휴가철과 같이 트래픽이 많은 이벤트에 대한 클라우드 인프라 환경에서 Adobe Commerce을 준비하기 위한 경영진 수준 지침입니다.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/63svzoaJbKTgiO3iJR3iCyr4-slOLmt4QaVT2Y--NYI'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 7ffe3c23f94b67342f02ed655d0a1700dd8f5a02
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%
---

# Adobe Commerce 휴일 준비 개요

이 플레이북은 휴가철과 같이 트래픽이 많은 이벤트에 대한 Adobe Commerce 환경을 준비하는 데 필요한 지침을 제공합니다. 기술 권장 사항을 다음과 같은 5가지 전략적 중점 영역으로 통합합니다.

- 성능 최적화
- 모범 사례 및 안정성
- 모니터링 및 가시성
- 확장성 및 용량 계획
- 운영 준비

이러한 집중 영역은 최대 로드 시에도 안정적이고 안전하며 성능을 유지하는 데 도움이 됩니다.

## 성능 최적화

다음은 최적화된 성능을 보장하기 위한 권장 단계에 대한 개요입니다. 자세한 내용은 [Adobe Commerce 휴일 준비 > 성능 최적화](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/performance-optimization.md)를 참조하십시오.

* Fastly 요청 캐싱 최적화: 프로모션 추적 매개 변수를 표준화하고 랜딩 페이지를 캐시할 수 있는지 확인하고 GraphQL GET for PWA 또는 Headless 상점 전면을 사용하여 Fastly 캐시 적중률을 높입니다.
* Fastly IO 활성화: Fastly 이미지 최적화 및 Deep IO를 켜서 원본 대신 CDN 에지에서 이미지 변환이 실행되므로 이미지가 많은 상점에서 페이지 렌더링 시간이 단축됩니다.
* L2 캐시 활성화: 각 웹 노드에 캐시 데이터를 로컬로 저장하여 Adobe Commerce 버전에 따라 지연을 줄이고 Redis/Valkey에 대한 네트워크 호출을 줄입니다. Redis 캐시는 Adobe Commerce 2.4.9 또는 2.4.5-p16, 2.4.6-p14, 2.4.7-p9 및 2.4.8-p4 이상의 패치 릴리스에는 지원되지 않습니다.
* 슬레이브 연결 사용: 읽기 중심의 쿼리를 `MYSQL_USE_SLAVE_CONNECTION` 및 `REDIS_USE_SLAVE_CONNECTION` 또는 `VALKEY_USE_SLAVE_CONNECTION`이(가) 있는 복제본 노드로 라우팅하여 마스터 데이터베이스가 로드 중 병목 현상이 발생하지 않도록 합니다.
* 비동기 주문 및 이메일 처리 활성화: 대기열 주문 배치, 주문 데이터 그리드 업데이트 및 체크아웃 이메일이 세 가지 별도 설정에서 백그라운드에서 실행되므로 높은 주문 볼륨에서 체크아웃이 빠르게 유지됩니다.
* 인덱서를 일정 업데이트 모드로 전환: customer_grid 인덱서를 제외하고, 자주 카탈로그를 업데이트하는 동안 잠기지 않도록 인덱서를 저장 시 업데이트에서 일정 업데이트 모드로 전환하여 cron 기반 업데이트 모드로 이동합니다.
* 크기 조정(분할) 아키텍처 고려: 조정 및 코드 수준 수정 사항으로 인해 CPU이 로드되지 않은 채 최대값이 유지되면 웹과 데이터베이스 노드의 크기를 독립적으로 조정하는 6노드 분할 계층 설정으로 이동합니다.

## 모범 사례 및 안정성

다음은 인스턴스 안정성을 보장하는 모범 사례에 대한 개요입니다. 각 단계에 대한 자세한 단계는 [Adobe Commerce 휴일 준비 > 모범 사례 및 안정성](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/best-practices-stability.md)을 참조하세요.

* 최신 Adobe Commerce 버전으로 업그레이드: Adobe에서 각 버전에 제공하는 보안 수정 사항과 성능 개선 사항을 유지하려면 지원되는 릴리스를 유지하십시오.
* 최신 ECE-Tools 및 Quality Patch Tool(QPT) 설치: ece-Tools를 종속성으로 업데이트하고 클라우드 및 온프레미스 설치 모두에 대해 적용 가능한 Quality Patches Tool 수정 사항이 적용되는지 확인합니다.
* 로그 파일 검토 및 정리: 디버그 로그를 제거하고 반복 오류를 모니터링하여 디스크 과사용을 방지하고 로그 가시성을 개선합니다.
* 디스크 크기 증가 모니터링: 공유 파일 및 데이터베이스 볼륨의 사용량이 70% 미만이 되도록 유지하여 스토리지 증가가 중단을 유발하지 않도록 합니다.
* 느린 데이터베이스 쿼리 검토: APM 툴링 및 MySQL 느린 쿼리 로그를 사용하여 최대 트래픽에 도달하기 전에 비용이 많이 드는 쿼리를 찾아 수정합니다.
* cron 작업을 올바르게 구성: Commerce의 모든 비동기 작업이 cron 작업에 의존하므로 cron 이 올바른 사용자 아래에서 매분 실행되는지 확인하십시오.
* 클라이언트측 설정 최적화: CSS, JavaScript 및 HTML 축소 및 번들링을 사용하여 상점 로드 시간을 가속화합니다.

## 모니터링 및 가시성

성수기 동안 Adobe Commerce 인스턴스를 모니터링하는 권장 방법은 다음과 같습니다. 이러한 각 모니터링 및 관찰 가능성 권장 사항에 대한 자세한 단계는 [Adobe Commerce 휴일 준비 > 모니터링 및 관찰 가능성](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/monitoring-observability.md)을 참조하십시오.

* New Relic으로 트래픽 모니터링: New Relic으로의 Fastly 로그 스트리밍을 사용하여 트래픽 이상, 악의적인 IP, 결제 등 엔드포인트를 타겟팅하는 악의적인 요청, 장치/브라우저 트렌드를 파악할 수 있습니다.
* New Relic 경고 사용자 지정: Adobe의 관리 경고 외에도 비정상적인 트래픽, 느린 GraphQL 쿼리 또는 증가하는 오류율에 대한 고유한 NRQL 기반 경고를 설정합니다.
* Apdex 점수 추적: Apdex 점수(target ≥ 0.85)를 시청하여 사용자가 만족스러운 것으로 간주하는 범위에서 백엔드 및 프론트엔드 응답 시간을 유지합니다.
* 지원 인사이트 검토(SWAT 보고서): 최대 이벤트 전후에 SWAT 보고서를 실행하여 시스템 수준 위험 및 개선 영역을 식별합니다.

## 확장성 및 용량 계획

이러한 각 확장성 및 용량 계획 권장 사항에 대한 자세한 단계는 [Adobe Commerce 휴일 준비 > 확장성 및 용량 계획](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md)을 참조하십시오.

* 클러스터 업사이징을 일찍 계획하십시오. 주요 판촉 행사 최소 10일(영업일 기준) 전에 Adobe 지원부에 임시 컴퓨팅 업사이징을 요청하십시오.
* Fastly 원본 실딩 활성화: 원본 근처에 있는 Shield POP를 통해 캐시되지 않은 요청을 라우팅하여 원본 서버에 직접 도착하는 요청이 줄어듭니다.
* 로드 및 장애 조치 테스트 수행: 주요 캠페인을 앞두고 로드 및 복구 시나리오를 테스트하여 확장 및 롤백 계획이 실제로 유지되는지 확인합니다.

## 운영 준비

* 모든 보안 및 성능 패치 적용: 나중에 배포가 중단되지 않도록 코드 동결 전에 모든 패치를 완료합니다.
* 휴일 전 상태 검사 실행: 백업, cron 상태 및 캐시 warmup 스크립트를 테스트하여 로드 중 작업이 원활하게 실행되도록 합니다.
* 모니터링 플레이북을 설정합니다. 경고 임계값, 에스컬레이션 경로 및 24x7 연락처를 문서화하여 팀이 최대 가동 시간 동안 빠르게 응답할 수 있도록 합니다.
* 문서 롤백 계획: 버전이 지정된 롤백 전략을 준비하여 잘못된 배포에서 신속하게 복구할 수 있습니다.