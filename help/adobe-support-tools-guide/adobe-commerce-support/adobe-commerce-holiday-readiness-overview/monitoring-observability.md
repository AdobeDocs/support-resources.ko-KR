---
title: 모니터링 및 가시성
description: Adobe Commerce 판매자가 휴가철과 같이 트래픽이 많은 이벤트에 대비할 수 있는 환경을 준비할 수 있도록 모니터링 및 관찰 가능성 권장 사항.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: 4239b8a6-e74f-567d-a7a5-b98b9ead0ea4
    internal-label: Observability
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 2%
---

# 모니터링 및 가시성

이 섹션에서는 휴가철과 같이 트래픽이 많은 이벤트에 대비하기 위해 Adobe Commerce 환경을 모니터링하기 위한 기술 권장 사항을 제공합니다.

>[!NOTE]
>
>**(클라우드 전용)**(으)로 표시된 단계는 클라우드 인프라의 Commerce에 적용됩니다. 대부분의 다른 권장 사항은 온-프레미스 배포에도 적용됩니다.

## New Relic으로 트래픽 모니터링(Cloud만 해당) {#monitor-traffic-with-new-relic}

클라우드 인프라의 Adobe Commerce에는 [!DNL Fastly] 로그 스트리밍을 [!DNL New Relic]에 거의 실시간으로 원활하게 통합하는 [!DNL New Relic] observability platform 구독이 포함되어 있습니다. 이 통합을 통해 트래픽 패턴 및 트렌드를 실시간으로 모니터링할 수 있으므로 수정 작업을 수행할 수 있습니다.

이 로그를 사용하여 다음을 수행합니다.

* 웹 요청이 시작된 국가를 식별합니다.
* 귀하의 사이트에 악용적인 IP 주소 또는 사용자 IP 에이전트를 찾습니다.
* 결제와 같은 특정 끝점을 타겟팅하는 악성 트래픽을 식별합니다.
* 고객이 사용하는 장치 및 브라우저 유형에 대한 보고서를 작성합니다.

예를 들어 트래픽의 소스 국가를 모니터링하여 이것이 판촉 행사 및 고객의 지리적 위치를 반영하는지 확인합니다.

```sql
SELECT count(*) FROM Log
WHERE cache_status IS NOT NULL
AND project_id = '<YOUR_PROJECT_ID>'
AND (content_type LIKE 'text/html;%' or url LIKE '%graphql%' or url like '%rest%')
FACET geo_country_code
SINCE 7 days ago until today
```

필요에 따라 이 쿼리를 수정하거나, 더 세분화하거나, 중앙 집중식 추적을 위해 대시보드로 전환합니다. 자세한 내용은 [New Relic 로그 관리](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management)를 참조하십시오.

## New Relic 경고 사용자 지정(Cloud만 해당) {#customize-new-relic-alerts}

클라우드 인프라의 Adobe Commerce에서 설정한 관리 경고 외에도 최대 판매 시즌 동안 플랫폼에 대한 광범위한 경고 및 알림을 설정할 수 있습니다(예: GraphQL 쿼리의 봇 트래픽 또는 증가된 응답 시간 알림). 기본 제공 경고의 전체 목록은 [Adobe Commerce에 대한 관리 경고](https://experienceleague.adobe.com/ko/docs/commerce-operations/tools/managed-alerts-for-adobe-commerce/managed-alerts-for-magento-commerce)를 참조하십시오.

[!DNL New Relic] 경고 및 AI가 NRQL 기반 쿼리 구조를 지원합니다. **[!UICONTROL 경고 및 AI]** 아래의 [!DNL New Relic] 대시보드에서 사용자 지정 경고를 설정합니다.

## Apdex 점수 검토(Cloud만 해당) {#review-apdex-score}

Apdex 점수는 웹 애플리케이션 및 서비스의 응답 시간에 대한 사용자 만족도를 측정합니다. [!DNL New Relic]을(를) 사용하여 클라우드 인프라에서 Adobe Commerce의 Apdex 점수를 검토할 수 있습니다.

Apdex 점수의 범위는 0에서 1까지입니다. 점수가 0인 것은 가능한 한 나쁜 점수입니다. 이것은 응답 시간의 100%가 **불합격**&#x200B;임을 의미합니다. 점수 1이 가장 좋은 점수입니다. 이것은 응답 시간의 100%가 **만족**&#x200B;되었음을 의미합니다. [!DNL New Relic]은(는) 백엔드 성능을 반영하는 App Server 점수와 클라이언트측 성능을 반영하는 최종 사용자 점수를 모두 보고합니다.

Apdex 점수 0.5 이하. 0.4 이하의 스코어는 중단으로 간주됩니다.

[!DNL New Relic]은(는) Apdex와 함께 클라우드 인프라의 Adobe Commerce에서 성능 문제를 분석할 수 있는 다양한 통계를 제공합니다. 단계는 [Adobe Commerce에서 New Relic을 사용하여 성능 문제 해결](https://experienceleague.adobe.com/ko/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/troubleshoot-performance-using-new-relic-on-magento-commerce)을 참조하십시오.

## 지원 인사이트 검토(SWAT 보고서) {#review-support-insights-swat-report}

환경에 대한 자세한 보고서를 보려면 사이트 전체 분석 도구(SWAT) 보고서를 생성하십시오. SWAT 도구에 대한 자세한 내용은 [사이트 전체 분석 도구](https://experienceleague.adobe.com/ko/docs/commerce-operations/tools/site-wide-analysis-tool/intro)를 참조하십시오.