---
title: 확장성 및 용량 계획
description: Adobe Commerce 판매자가 휴가철과 같이 트래픽이 많은 이벤트에 대비할 수 있는 환경을 준비하는 데 도움이 되는 확장성 및 용량 계획 권장 사항입니다.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
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
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%
---

# 확장성 및 용량 계획

이 섹션에서는 휴가철과 같이 트래픽이 많은 이벤트에 대비할 수 있도록 Adobe Commerce 환경을 조정하는 데 필요한 기술 권장 사항을 제공합니다.

>[!NOTE]
>
>**(클라우드 전용)**(으)로 표시된 단계는 클라우드 인프라의 Commerce에 적용됩니다. 대부분의 다른 권장 사항은 온-프레미스 배포에도 적용됩니다.

## 클러스터 조기 업그레이드 계획(클라우드만 해당) {#plan-cluster-upsize-early}

클라우드 인프라 고객의 Commerce을 위해 임시 클러스터 업사이드는 피크 시즌 트래픽 급증을 처리하기 위해 더 많은 컴퓨팅 리소스를 할당합니다. 날짜 범위 및 필요한 클러스터 크기로 지원 티켓을 미리 구입하고, 현재 리소스 사용량 및 요구 사항에 대해 전담 계정 관리자와 조율합니다. 블랙 프라이데이 및 사이버 먼데이 기간 동안 용량이 제한되므로 휴일 시즌에 맞는 경우, 최소 48시간 전에 요청서를 제출하십시오. [임시 업사이징을 요청하는 방법](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/how-to-request-temporary-adobe-commerce-on-cloud-infrastructure-upsize)을 참조하세요.

예를 들어, 일일 24코어(24개의 vCPU, 96GB RAM) 업사이징을 7일 동안 96개 코어로 수행하는 Pro 아키텍처 고객은 약 4배의 리소스(96개의 vCPU, 384GB RAM)를 사용하며, 이는 약 504vCPU-일(96×7 − 24×7)의 증분 소비량입니다.

## Fastly 원점 차폐 {#fastly-origin-shielding}

Adobe Commerce [!DNL Fastly]의 원본 차폐의 목적은 Adobe Commerce 원본으로 직접 트래픽을 줄이는 것입니다. 요청이 수신되면 [!DNL Fastly] 에지 위치(Point of Presence)가 캐시된 콘텐츠를 확인하고 전달합니다. 캐시되지 않은 경우 Shield POP로 계속 이동하여 해당 콘텐츠가 캐시되는지 확인합니다. 이전에 다른 글로벌 POP에서도 콘텐츠를 요청한 경우 캐시됩니다. 마지막으로 Shield POP에 캐시되지 않은 경우 원본 서버로만 진행됩니다.

[!DNL Fastly] 구성 백엔드 설정의 Adobe Commerce 관리에서 [!DNL Fastly] 원본 차폐를 사용하도록 설정할 수 있습니다. 최상의 성능을 위해 Adobe Commerce 원본 데이터 센터와 가장 가까운 실드 위치를 선택하십시오. 자세한 내용은 [백 엔드 및 원본 보호 구성](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration#configure-back-ends-and-origin-shielding)을 참조하세요.

기본적으로 [!DNL Fastly] 원본 차폐를 사용할 수 없습니다.

## 로드 및 페일오버 테스트 수행 {#conduct-load-and-failover-tests}

주요 캠페인에 앞서 로드 및 복구 테스트를 수행하여 확장 구성 및 롤백 계획을 확인합니다.