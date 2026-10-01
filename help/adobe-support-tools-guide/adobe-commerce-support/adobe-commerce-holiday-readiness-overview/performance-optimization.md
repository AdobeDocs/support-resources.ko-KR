---
title: 성능 최적화
description: Adobe Commerce 판매자가 휴가철과 같이 트래픽이 많은 이벤트에 대비할 수 있는 환경을 준비하는 데 도움이 되는 성능 최적화 권장 사항입니다.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
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
source-git-commit: b2220ea4cb5a301cbee6cea5fb90d6dc8a05eeff
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 0%
---

# 성능 최적화

이 섹션에서는 휴가철과 같은 트래픽이 많은 이벤트에 대해 Adobe Commerce 환경(Commerce on cloud infrastructure 및 온프레미스)을 준비하기 위한 기술 권장 사항을 제공합니다.

>[!NOTE]
>
>**(클라우드 전용)**(으)로 표시된 단계는 클라우드 인프라의 Commerce에 적용됩니다. 대부분의 다른 권장 사항은 온-프레미스 배포에도 적용됩니다.

## Fastly 요청 캐싱 최적화(클라우드 전용) {#optimize-fastly-request-caching}

[!DNL Fastly]은(는) 에지에서 응답을 캐시하여 원본 서버의 로드를 줄입니다. 성수기 동안 몇 가지 구성 검사를 통해 해당 캐시를 최대한 활용할 수 있습니다. 특히 추적 매개 변수 또는 Headless 상점이 있는 프로모션을 실행할 때 유용합니다. 전체 구성 참조에 대해서는 [캐시 구성 사용자 지정](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration)을 참조하십시오.

* 추적 매개 변수 정규화: 휴가철에는 모든 URL에 고유한 추적 문자열을 추가하는 소셜 및 유료 캠페인(예: Google 광고, Facebook 및 X)을 실행할 수 있습니다. 각각의 고유한 문자열은 다른 경우에는 동일한 페이지에 대해 별도의 캐시 항목을 만들어 캐시 적중률을 낮춥니다. [!DNL Fastly]이(가) 이러한 매개 변수를 동등하게 취급하도록 Adobe Commerce 관리자의 [!DNL Fastly] 구성에 있는 **[!UICONTROL 무시된 URL 매개 변수]** 목록에 추가하십시오.
* 랜딩 페이지를 캐시할 수 있는지 확인합니다. 각 프로모션 랜딩 페이지에서 `x-cache` 응답 헤더를 확인합니다. 캐시 가능한 페이지는 후속 로드 시 `HIT` 또는 `HIT`/`MISS` 쌍을 반환합니다. 헤더가 `MISS, MISS`을(를) 반환하는 경우 페이지가 캐싱되지 않으므로 조사가 필요합니다.
* GraphQL 쿼리에 대한 GET 요청 사용: PWA 또는 Headless Storefront를 실행하는 경우 GraphQL 쿼리를 `POST` 요청이 아닌 URL에 포함된 쿼리와 함께 `GET` 요청으로 보냅니다. [!DNL Fastly]은(는) 쿼리가 URL의 일부인 `GET`개의 요청만 캐시합니다. 본문에서 보낸 쿼리가 있는 `GET` 요청이 캐시되지 않습니다.

>[!NOTE]
>
>[!DNL Fastly] 원본 차폐는 캐시 성능에도 영향을 줍니다. 구성 세부 정보는 [가장 빠른 원본 차폐](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding)를 참조하십시오.

## Fastly IO 활성화(클라우드만 해당) {#enable-fastly-io}

[!DNL Fastly] IO는 이미지 크기 조정 및 형식 전환을 Adobe Commerce 원본 대신 [!DNL Fastly] 에지 네트워크로 오프로드합니다. 이렇게 하면 트래픽이 많은 영업 기간 동안 흔히 발생하는 병목 현상인 이미지가 많은 상점의 서버 로드를 줄이고 페이지 렌더링 속도를 향상시킬 수 있습니다. 구성 옵션에 대해서는 [빠른 이미지 최적화](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/cdn/fastly-image-optimization)를 참조하십시오.

시작하기 전에 원점 차폐가 구성되어 있는지 확인합니다. [!DNL Fastly] IO는 필수 조건으로 원점 차폐가 필요합니다. 구성 세부 정보는 [가장 빠른 원본 차폐](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding)를 참조하십시오.

[!DNL Fastly] IO를 사용하려면:

1. 관리자의 **[!UICONTROL Fastly 구성]** 페이지로 이동하여 **[!UICONTROL 기본 IO 구성 옵션]** 옆에 있는 **[!UICONTROL 구성]**&#x200B;을 선택합니다.
1. [!DNL Fastly] IO 코드 조각이 활성화되어 있는지 확인하십시오.
1. **[!UICONTROL 이미지 최적화]** 구성에서 **[!UICONTROL 딥 이미지 최적화 사용]**&#x200B;을 *[!UICONTROL 예]*(으)로 설정하십시오. 이 설정은 Adobe Commerce의 기본 제공 이미지 크기 조정을 비활성화하고 작업을 [!DNL Fastly]&#x200B;(으)로 전송합니다.
1. 실드 위치가 올바르게 설정되어 있는지 확인합니다. 구성 세부 정보는 [가장 빠른 원본 차폐](#fastly-origin-shielding)를 참조하십시오.

>[!NOTE]
>
>딥 이미지 최적화는 제품 이미지만 조정합니다. 배너 및 컨텐츠 블록과 같은 CMS 이미지는 영향을 받지 않으며 Adobe Commerce의 기본 제공 크기 조정을 계속 사용합니다.

[!DNL Fastly] IO가 작동하는지 확인하려면 제품 이미지 요청에 대한 응답 헤더를 확인하십시오.

* `x-cache` 헤더가 `HIT`을(를) 반환합니다.
* `fastly-io-info` 및 `fastly-stats` 헤더가 채워집니다.
* 이미지 URL이 경로에 `/cache/` 디렉터리를 포함하지 않습니다.

## Redis L2 캐시 구현 {#implement-redis-l2-cache}

효율적인 캐싱 방법을 구현하여 트래픽이 많이 발생하는 시즌 동안 스토어가 안정적으로 수행됩니다. [!DNL Redis] L2 캐시는 각 웹 노드에 로컬로 캐시 데이터를 저장하여 네트워크 대역폭을 [!DNL Redis]&#x200B;(으)로 줄입니다. L2 캐시의 작동 방식에 대한 배경은 [수준 2 캐시](https://experienceleague.adobe.com/ko/docs/commerce-operations/configuration-guide/cache/level-two-cache)를 참조하십시오.

클라우드 인프라의 Commerce에서 `REDIS_BACKEND` 배포 변수를 설정하여 이 기능을 사용하도록 설정합니다. 구성 단계는 Commerce on Cloud Infrastructure Guide의 [REDIS_BACKEND](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_backend)을(를) 참조하십시오. 온-프레미스에서 `app/etc/env.php`에서 직접 구성하십시오.

>[!NOTE]
>
>[!DNL Redis]은(는) Adobe Commerce 2.4.9 이상 또는 2.4.5-p16, 2.4.6-p14, 2.4.7-p9 또는 2.4.8-p4 이상의 패치 릴리스에서 L2 캐시 백엔드로 지원되지 않습니다. 이 버전에서는 대신 `VALKEY_BACKEND`을(를) 사용합니다.

## MySQL 및 Redis 슬레이브 연결 활성화(Cloud만 해당) {#enable-mysql-and-redis-slave-connections}

[!DNL Redis] 및 [!DNL MySQL] 슬레이브 연결은 읽기 트래픽을 복제본 노드로 오프로드하므로 트래픽이 많은 기간 동안 마스터 연결에 대한 로드를 줄입니다. 구성 단계는 Adobe Commerce 버전에 따라 [MYSQL_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#mysql_use_slave_connection) 및 [REDIS_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_use_slave_connection) 또는 [VALKEY_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#valkey_use_slave_connection)을 참조하십시오.

### Redis 슬레이브 연결

[!DNL Redis] 슬레이브 연결은 [!DNL Redis] 인스턴스에 대한 읽기 전용 연결이므로 비마스터 노드에서 읽기 트래픽을 제공할 수 있습니다. [!DNL MySQL]을(를) 사용하도록 설정하지 않으면 부하가 높은 병목 현상이 발생할 수 있습니다. [!DNL New Relic]의 APM 개요 차트에서 응답 시간이 빨라졌는지 초기 기호로 확인한 다음, 가장 시간이 많이 걸리는 트랜잭션을 기준으로 정렬하여 **[!UICONTROL 데이터베이스]** 탭에서 느린 [!DNL MySQL]개의 `SELECT`개 쿼리를 확인합니다. 배포 변수 `REDIS_USE_SLAVE_CONNECTION`을(를) `true`(으)로 설정하여 이 기능을 활성화하십시오.

>[!NOTE]
>
>`REDIS_USE_SLAVE_CONNECTION`은(는) 스테이징 및 Production Pro 클러스터 환경에서만 지원됩니다. 시작 또는 크기 조정(분할) 아키텍처 프로젝트에서는 지원되지 않습니다. 크기가 조정된 아키텍처에서 이 기능을 사용하면 [!DNL Redis]개의 연결 오류가 발생합니다. 해당 아키텍처에서 [!DNL Redis]개의 L2 캐시를 대신 사용하십시오. 위의 [Redis L2 캐시 구현](#implement-redis-l2-cache-implement-redis-l2-cache)을 참조하십시오.

### MySQL 슬레이브 연결

특정 읽기 전용 데이터베이스 쿼리를 슬레이브 연결로 보내도록 Pro 클러스터 환경에서 `MYSQL_USE_SLAVE_CONNECTION` 플래그를 사용하도록 설정하여 마스터 연결에서 쿼리 실행을 오프로드합니다.

>[!CAUTION]
>
>프로덕션에서 두 설정 중 하나를 활성화하기 전에 테스트를 로드합니다. 정상 부하가 있는 환경에서 슬레이브 연결은 성능을 10~15% 느리게 할 수 있습니다. 지속적인 부하가 많은 환경에서는 비슷한 수준의 성능으로 성능을 향상시킬 수 있습니다. 활성화하기 전에 예상되는 성수기 트래픽에서 평가합니다.

## 비동기 주문 및 이메일 처리 활성화 {#enable-asynchronous-order-and-email-processing}

비동기 처리를 사용하여 백그라운드에서 대량 주문 관련 작업을 큐에 추가하고 실행하여 최대 트래픽 동안 프론트엔드 지연을 줄입니다. 여기에는 서로 관련되지만 서로 다른 세 가지 설정이 포함됩니다. 개요는 [구성 모범 사례](https://experienceleague.adobe.com/ko/docs/commerce-operations/performance-best-practices/configuration)를 참조하세요.

* 비동기 주문 배치: 비동기 주문 모듈은 주문을 받은 것으로 표시하고 큐에 배치하며 선입선출 방식으로 주문을 처리합니다. 기본적으로 비활성화되어 있습니다. 명령줄에서 활성화합니다.

  ```
  bin/magento setup:config:set --checkout-async 1
  ```

  사용하도록 설정하면 주문 세부 정보를 즉시 사용할 수 없습니다. `placeOrderProcess` 소비자가 인벤토리에 대해 확인하고(기본적으로 사용하도록 설정됨) 업데이트할 때까지 해당 주문은 대기 상태로 유지됩니다. 이 모듈을 비활성화하기 전에 진행 중인 모든 비동기 주문 처리가 완료되었는지 확인하십시오. 자세한 내용은 [체크아웃 성능 모범 사례](https://experienceleague.adobe.com/ko/docs/commerce-operations/performance-best-practices/high-throughput-order-processing)를 참조하세요.

* 비동기 주문 데이터 처리: 데이터베이스 수준에서 집중적인 상점 영업 및 집중적인 주문 처리가 충돌할 수 있습니다. 이 설정을 활성화하면 두 트래픽 패턴이 구별되므로 주문이 임시 저장소에 배치되고 충돌 없이 Order Management 그리드로 대량으로 이동됩니다. 이렇게 하면 기본적으로 주문, 송장, 선적 및 대변 메모 그리드로 업데이트되므로 잠금이 발생하지 않고 처리 시간이 줄어듭니다. 최상의 결과를 얻으려면 1분에 한 번 실행되도록 cron 을 구성하십시오.

  >[!NOTE]
  > 
  >이 기능을 활성화하는 방법은 배포 모드에 따라 다릅니다. 클라우드 인프라 스테이징 및 프로덕션 환경의 Adobe Commerce은 기본적으로 프로덕션 모드에서 실행되며, 여기서 이 설정은 관리자를 통해 사용할 수 없습니다. 프로덕션 모드에서 `bin/magento config:set dev/grid/async_indexing 1`을(를) 대신 실행합니다. 기본 모드에서 **[!UICONTROL 스토어]** > **[!UICONTROL 구성]** > **[!UICONTROL 고급]** > **[!UICONTROL 개발자]** > **[!UICONTROL 그리드 설정]**(으)로 이동하여 **[!UICONTROL 비동기 인덱싱]**&#x200B;을 *[!UICONTROL 사용]*(으)로 설정합니다.

  자세한 내용은 [예약된 주문 작업](https://experienceleague.adobe.com/ko/docs/commerce-admin/stores-sales/order-management/orders/order-scheduled-operations)을 참조하십시오.

* 비동기 이메일 알림: 이 설정은 체크아웃 및 주문 처리 이메일 알림을 백그라운드로 이동합니다. **[!UICONTROL 스토어]** > **[!UICONTROL 구성]** > **[!UICONTROL 판매]** > **[!UICONTROL 판매 이메일]** > **[!UICONTROL 일반 설정]** > **[!UICONTROL 비동기 전송]**&#x200B;에서 사용하도록 설정합니다.

## 일정에 따른 업데이트를 위한 인덱서 구성 {#configure-indexers-for-update-on-schedule}

데이터베이스 잠금을 방지하고 자주 카탈로그를 업데이트하는 동안 응답성을 향상시키려면 인덱서를 예약 모드에서 실행하도록 설정하십시오. 자세한 내용은 [인덱서 구성 모범 사례](https://experienceleague.adobe.com/ko/docs/commerce-operations/implementation-playbook/best-practices/maintenance/indexer-configuration)를 참조하세요.

인덱서는 **[!UICONTROL 저장 시 업데이트]** 또는 **[!UICONTROL 일정에 따라 업데이트]** 모드에서 실행할 수 있습니다.

* 카탈로그나 다른 데이터가 변경될 때마다 **[!UICONTROL 저장 시 업데이트]**&#x200B;합니다. 낮은 업데이트 및 탐색 강도를 가정하며, 높은 로드 상태에서 상당한 지연과 데이터 비가용성을 초래할 수 있습니다.
* **[!UICONTROL 일정에 따라 업데이트]**&#x200B;하는 것이 프로덕션에 권장됩니다. 전용 cron 작업을 통해 데이터 업데이트에 대한 정보를 저장하고 백그라운드에서 다시 인덱싱합니다.

**[!UICONTROL 시스템]** > **[!UICONTROL 도구]** > **[!UICONTROL 인덱스 관리]**&#x200B;에서 각 인덱서의 업데이트 모드를 독립적으로 설정합니다.

>[!IMPORTANT]
>
>`customer_grid` 인덱서의 지원되는 모드는 Adobe Commerce 버전에 따라 다릅니다. 2.4.8 이전 버전에서는 고객 그리드가 **[!UICONTROL 저장 시 업데이트]**&#x200B;만 지원합니다. **[!UICONTROL 일정에 따라 업데이트]**&#x200B;로 설정하지 마십시오. Adobe Commerce 2.4.8 이상에서는 고객 그리드가 두 모드를 모두 지원하며 기본값은 **[!UICONTROL 일정에 따라 업데이트]**&#x200B;입니다.

## 카탈로그 플랫 테이블 비활성화 및 평가 {#disable-and-evaluate-catalog-flat-table}

제품 및 범주에 플랫 테이블을 사용하지 않는 것이 좋습니다. 더 이상 사용되지 않는 기능으로 인해 성능 저하 및 색인화 문제가 발생할 수 있습니다. 자세한 내용은 [기본 카탈로그](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/catalog/catalog-flat)를 참조하세요.

플랫 카탈로그를 사용하지 않으려면 **[!UICONTROL 스토어]** > **[!UICONTROL 구성]** > **[!UICONTROL 카탈로그]** > **[!UICONTROL 카탈로그]** > **[!UICONTROL 상점]**&#x200B;로 이동하고, **[!UICONTROL 플랫 카탈로그 범주 사용]**&#x200B;을 *[!UICONTROL 아니요]*(으)로 설정하고, **[!UICONTROL 플랫 카탈로그 제품 사용]**&#x200B;을 *[!UICONTROL 아니요]*(으)로 설정한 다음 **[!UICONTROL 구성 저장]**&#x200B;을 클릭하십시오.

일부 타사 모듈 및 사용자 지정에서는 제대로 작동하기 위해 플랫 테이블이 필요합니다. 플랫 테이블을 비활성화하기 전에 해당 확장을 계속 사용할 때의 영향과 위험을 평가합니다.

## 크기 조정(분할) 아키텍처(클라우드만 해당) 고려 {#consider-scaled-split-architecture}

이전 구성과 코드 수준 최적화를 적용한 후에도 로드 테스트 또는 라이브 인프라 성능이 CPU 및 기타 리소스를 최대 한도로 표시한 경우 크기 조정(분할) 아키텍처로 이동하는 것이 좋습니다. 자세한 내용은 [조정된 아키텍처](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/architecture/scaled-architecture)를 참조하십시오.

>[!NOTE]
>
>배율 조정 아키텍처는 Pro 48 클러스터 이상의 계정에서만 사용할 수 있습니다.

분할 계층 아키텍처에서는 최소 6개의 노드를 사용합니다. [!DNL OpenSearch] 또는 [!DNL Elasticsearch], [!DNL MariaDB] 및 [!DNL Redis] 또는 [!DNL Valkey]을(를) 실행하는 서비스 노드 3개와 `php-fpm` 및 `NGINX`을(를) 실행하는 웹 노드 3개.

* 서비스 노드는 서버 크기(CPU 및 메모리)를 늘려 수직으로만 확장할 수 있습니다. 데이터베이스 클러스터는 고가용성을 위해 구축되므로 서비스 노드를 안정적으로 수평으로 확장할 수 없습니다.
* 웹 노드는 수직 및 수평 모두 확장할 수 있으며, 증가하는 요청 볼륨을 처리하기 위해 웹 서버를 추가할 수 있습니다.

이를 통해 부하가 높은 기간에 대해 필요에 따라 인프라를 확장하여 각 계층을 독립적으로 확장할 수 있습니다. 예상되는 과부하 기간 전에 분할 계층 아키텍처로 전환하려면 Adobe 계정 팀에 문의하십시오.
