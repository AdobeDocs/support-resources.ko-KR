---
title: Adobe DX 솔루션 통합 휴일 준비 안내서
description: 이 문서에서는 DX 솔루션에 대한 휴일 준비 가이드를 제공합니다.
solution: Experience Platform, Journey Optimizer, Customer Journey Analytics, Commerce, Experience Manager, Workfront, Campaign, Analytics, Target, Marketo Engage
role: Developer, Admin, Leader, User
source-git-commit: 3ae8c97072cd6f8ae09aa8dc1e3ce0249fe6fcb7
workflow-type: tm+mt
source-wordcount: '3726'
ht-degree: 1%

---

# Adobe DX 솔루션 통합 휴일 준비 안내서


Adobe DX 솔루션 통합 휴일 준비 안내서는 사후 문제 해결이 아닌 사전 계획에 중점을 두어 휴일 시즌을 준비할 수 있도록 도와줍니다. 인스턴스가 준비되었는지 확인할 수 있는 실용적인 단계를 제공하여 잠재적인 문제가 발생하기 전에 최소화합니다. Adobe 팀은 기술 전문 지식, 다양한 기능, 검증된 방법을 통해 기술 및 전략적으로 적절한 수준의 지원 및 지침을 제공하므로 비즈니스에 대한 준비가 잘 되어 있습니다.

다음 모범 사례를 따라 Adobe Digital Experience 솔루션의 복원력이 뛰어나고 안전하며 피크 홀리데이 트래픽에 대비할 수 있도록 하십시오.

* 트래픽 증가에 대한 계획을 수립합니다.
* 최대 기간 중에는 주요 변경 사항을 피하고, 휴가철 전 또는 후에 업데이트를 예약하십시오.
* 대시보드와 경고를 사용하여 성능을 모니터링하고 병목 현상을 조기에 감지할 수 있습니다.
* 승인된 지원 담당자가 최신 상태인지 확인하십시오.
* 가능한 경우 미리 [Adobe 지원에 문의](https://experienceleague.adobe.com/ko/docs/learning-manager/using/faq/how-to-submit-support-ticket)합니다.

Adobe의 솔루션별 휴일 준비 권장 사항은 다음 섹션을 참조하십시오.

* [Adobe Experience Platform](#aep)
* [Adobe Journey Optimizer](#ajo)
* [Adobe Customer Journey Analytics](#cja)
* [Adobe Commerce](#commerce)
* [Adobe Experience Manager](#aem)
* [Adobe Marketo](#marketo)
* [Adobe Workfront](#workfront)
* [Adobe Campaign](#campaign)
* [Adobe Analytics](#analytics)
* [Adobe Target](#target)

>[!NOTE]
>
>각 섹션을 클릭하여 확장합니다.

<details>
<summary><h2 id="aep" style="display: inline-block;">Adobe Experience Platform (AEP) 휴일 준비 안내서</h2></summary>

Adobe Experience Platform(AEP)는 실시간 고객 경험을 강화하는 데 중요한 역할을 합니다. 휴가철이 다가오면서 AEP 구현이 트래픽 증가, 안전한 데이터 처리 및 확장 가능한 수집에 최적화되도록 하는 것이 중요합니다.

## 계절별 수요 예측

계절별 트래픽 급증에 대비하기 위해 Adobe에서는 용량을 계획하고 스트리밍 프로필 수집을 모니터링하는 것이 좋습니다. 여기에는 데이터 볼륨을 예측하고 시스템에서 처리량을 늘릴 수 있도록 하는 작업이 포함됩니다. 자세한 내용은 [용량 및 시즌 트래픽 계획](https://experienceleague.adobe.com/ko/docs/experience-platform/dataflows/ui/monitor-streaming-profile)을 참조하십시오.

## 크기 조정 준비

Adobe은 사용자 환경이 휴일 트래픽에 대비할 수 있도록 다음과 같은 몇 가지 전략을 제공합니다.

* 샌드박스에 대한 할당 용량을 늘립니다.
* [모니터링 대시보드](https://experienceleague.adobe.com/ko/docs/experience-platform/dataflows/ui/monitor-streaming-profile)에서 처리량이 많은 데이터 흐름을 식별하고 필요한 경우 조절 또는 필터링을 적용합니다.
* [라이선스 사용 및 용량: 스트리밍 처리량 모범 사례](https://experienceleague.adobe.com/ko/docs/experience-platform/landing/license/capacity#suggestions)에 설명된 대로 처리 수집을 사용하여 대기 시간이 짧은 사용 사례를 통해 성능을 최적화하십시오.

이러한 사례는 수집 안정성을 유지하고 최대 기간 동안 지연을 줄이는 데 도움이 됩니다.

## 우수 사례 및 보호 기능

Adobe은 작동 제한 내에서 유지하고 서비스 중단을 방지하려면 다음 수집 및 프로필 보호 기능을 권장합니다.

* [스트리밍 처리량 모범 사례](https://experienceleague.adobe.com/ko/docs/experience-platform/landing/license/capacity#suggestions)
* [데이터 수집을 위한 보호 기능](https://experienceleague.adobe.com/ko/docs/experience-platform/ingestion/guardrails)
* [실시간 고객 프로필 데이터 및 세분화를 위한 기본 보호 기능](https://experienceleague.adobe.com/ko/docs/experience-platform/profile/guardrails)
* [AEP 블루프린트: 가드레일](https://experienceleague.adobe.com/ko/docs/blueprints-learn/architecture/architecture-overview/guardrails)

## 보안 및 관리

Adobe은 특히 데이터 민감도가 높아지는 트래픽이 많은 시즌에 강력한 보안 및 거버넌스 관행을 강조합니다.

AEP 구현 전반에 걸쳐 고객 데이터를 보호하고, 개인 정보 컨트롤을 적용하고, 규정 준수를 유지 관리하는 방법에 대한 권장 사항은 [Adobe Experience Platform의 거버넌스, 개인 정보 보호 및 보안: 보안](https://experienceleague.adobe.com/ko/docs/experience-platform/landing/governance-privacy-security/overview#security)을 참조하십시오.

조직은 이러한 지침을 따르고 Adobe의 공개 설명서를 활용하여 Adobe Experience Platform이 탄력적이고 안전하며 휴가철 내내 탁월한 고객 경험을 제공할 준비가 되었는지 확인할 수 있습니다.

</details>

<details>
<summary><h2 id="ajo" style="display: inline-block;">Adobe Journey Optimizer (AJO) 휴일 준비 안내서</h2></summary>

휴가 시즌을 대비하여 Adobe Journey Optimizer을 준비하려면 조직은 이벤트 급증과 크로스 채널 복잡성을 예측하고 여정 및 빈도 규칙을 구성하고 데이터 위생 및 의사 결정 논리를 보장해야 합니다. 또한 규모에 맞게 성능을 검증하고, 보안 및 API 가드레일을 적용하며, 피크 이후 통찰력을 적용하여 향후 캠페인을 구체화해야 합니다.

## 수요 예측

* 휴가철 압축률과 더 무거운 캠페인 양에 따라 다음을 예상하십시오.
   * 실시간 이벤트 및 트리거된 여정(장바구니 포기, 마지막 순간 오퍼)의 스파이크
   * 메시지 포화 위험(옵트아웃 증가, 피로)
   * 크로스 채널 복잡성 증가(이메일 + 푸시 + SMS + 인앱)
* 지난 해의 지표 (열기/클릭/옵트아웃 비율, 여정 시작 볼륨)를 사용하여 예상되는 로드를 모델링하고 메시징 시스템에 대한 임계값을 설정합니다.
* &quot;조용한 창&quot; 또는 성능이 낮은 기간(예: 주말, 공휴일)을 식별하고 그에 따라 볼륨을 전송하기로 계획합니다.

## 크기 조정 준비

* AJO의 모든 채널 구성(이메일, 푸시, SMS, 웹, 인앱)이 올바르게 설정되었는지 확인합니다. [채널 구성 설정](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/configuration/channel-surfaces)을 참조하세요.
* 빈도 제한 및 제한 규칙을 구성하여 메시지 볼륨을 제어합니다. [빈도 제한](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/configuration/business-rules/configure-frequency-capping-rules) 문서를 참조하십시오.
* 채널/여정 규칙 집합 구성: [규칙 집합 작업](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets)을 참조하세요.
* 데이터 위생/실시간 이벤트 스트림 및 세그멘테이션 프레임워크를 준비합니다.
* 다음과 같이 휴일 캠페인에 대한 타겟 대상을 정의했는지 확인합니다.
   * 가치가 높은 고객
   * 단골 세그먼트
   * 장바구니 포기 사용자
   * 최초 구매자
* 휴일 여정을 위한 템플릿을 미리 로드하거나 준비하고, 의사 결정 논리(오퍼/제한)를 활용하여 인벤토리, 시간에 민감한 오퍼 및 채널 환경 설정에 따라 동적으로 조정할 수 있습니다. [오퍼에 제약 조건 추가](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/decisioning/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints) 문서에서 예제를 참조하십시오.
* 기술 준비: API/끝점 로드 용량, 사용자 지정 작업 및 외부 통합에 대한 스로틀/캡핑 규칙을 확인합니다. [보호 기능 및 제한 사항](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/get-started/guardrails)을 참조하세요.

## 테스트 및 유효성 검사

* 실험 프레임워크를 사용하여 주요 변수 변경 사항을 테스트합니다.
   * 전송 시간
   * 오퍼 유형
   * 채널 혼합
[AJO Experimentation Accelerator 모범 사례](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-best-practices)를 참조하세요.
* 엔드 투 엔드 여정 유효성 검사 수행:
   * 이벤트 트리거
   * 세분화 항목
   * 여정 경로 흐름
   * 개인화 논리
   * 오퍼 제한
   * 종료 기준
* 최대 가용량 및 충돌 규칙을 확인합니다. [여정 제한 및 중재](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/conflict-prioritization/journey-capping) 문서를 참조하세요.
* 최대 전송 또는 스파이크에 대한 스트레스 테스트 크기 조정된 볼륨: 높은 트리거 볼륨을 시뮬레이션하여 로드 중 시스템 동작의 유효성을 검사합니다.
* 전달성의 유효성 확인: 이메일 도메인/보낸 사람을 미리 정리하고, 모바일 푸시 구성을 확인하고, SMS/인앱에 대한 대체 채널을 확인합니다.

## 모범 사례

* 옴니채널 오케스트레이션을 사용합니다. AJO의 휴가철 예제를 보여주는 블로그 [참여 및 성장에 대한 필수 옴니채널 고객 여정](https://business.adobe.com/blog/essential-customer-journeys-for-omnichannel-engagement) 문서를 참조하세요.
* 적절한 경우 실시간 트리거를 우선 지정합니다. 예를 들어 장바구니 포기, 찾아보기 포기 및 재고 알림(휴일 쇼핑객이 더 반응형).
* 세그먼테이션 및 개인화 활용: 고의적인 세그먼트를 타겟팅하고 과거의 구매 행동 및 환경 설정을 기반으로 오퍼를 맞춤화합니다.
* 최소 메시징 피로: 과도한 요청을 방지하기 위해 제한 및 조용한 시간을 적용합니다. AJO의 [일일 빈도 제한으로 고객 경험 개선](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510?profile.language=ko) 블로그 게시물을 참조하십시오.
* 시간 문제: 플랜은 휴일 기간(압축된 시즌)에 더 일찍 전송하고 채널을 시간대 및 로컬 대상자 행동에 맞게 조정합니다.
* 긴급성을 만들려면 동적/제한 시간 오퍼를 제공하고, 중복과 충돌을 방지하기 위해 채널 간에 조정합니다.
* 제외 논리 사용: 방금 구매한 대상을 표시하지 않거나 사후 구매 여정을 적용하여 중복 메시지를 방지합니다.

## 보안 및 관리

* 필요한 사용자만 여정을 배포하거나 비즈니스 규칙을 수정할 수 있도록 액세스 제어 및 권한이 구성되어 있는지 확인합니다.
* API 호출/연결 한도 모니터링 및 적용: 예를 들어 [한도 API를 참조하십시오. | Adobe Journey Optimizer](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/connect-systems/external-systems/capping) 문서입니다.
* 깔끔한 자사 데이터를 사용하고 메시징이 중복/잘못 정렬되지 않도록 적절한 ID 결합을 보장합니다.
* 게재 기능 도메인이 따뜻하고 스팸 방지 조치가 적절히 배치되었는지 확인합니다. 특히 대량 휴일 전송인 경우 더욱 그렇습니다.
* 피크 시즌 동안 감사 로그 및 여정 변경 사항을 자주 검토하여 잘못된 실행 또는 잘못된 여정을 조기에 감지합니다.

## 피크 이후 학습

* 최대 로드 후 여정 항목 수, 제외 수, 옵트아웃 비율, 전달성 지표 및 채널 성능을 검토합니다.
* 억제된 세그먼트를 정리하고 휴일 기간용으로 빌드된 여정을 일시 중지 또는 폐기하여 이월 피로를 방지합니다.
* 실시간 성과에서 얻은 통찰력을 사용하여 내년 계획을 구체화합니다(예: 시간 조정 전송, 채널 혼합 및 메시지 볼륨).

조직에서는 시즌 수요를 사전 예방적으로 예측하고, 채널과 규칙을 구성하고, 여정 성능을 검증하고, 보안 및 거버넌스를 강화함으로써 Adobe Journey Optimizer이 이번 연휴 기간 및 그 이후에도 매끄럽고 개인화되고, 탄력적인 고객 경험을 제공하도록 할 수 있습니다.

</details>

<details>
<summary><h2 id="cja" style="display: inline-block;">Adobe Customer Journey Analytics (CJA) 휴일 준비 안내서</h2></summary>

Customer Journey Analytics은 5개의 P를 사용하여 휴가철/성수기 준비를 달성합니다.

## Customer Journey Analytics - 휴일/성수기 준비: 5 Ps

### 크기 조정 준비

* CJA 연결 및 데이터 보기를 검토하고 향상된 모니터링 및 프로비저닝이 필요한 연결 및 데이터 보기를 설정합니다.
* 프로비저닝이 휴일 확장에 충분한지 확인하고, 필요에 따라 중요한 연결 및 데이터 보기를 확장하십시오. 자세한 내용은 [연결 관리](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-connections/manage-connections)를 참조하십시오.

### 성능 모니터링

* RAM([[!UICONTROL Reporting Activity Manager] 개요](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview))을 활용하여 활성 및 대기 중인 보고 요청을 실시간으로 모니터링하고, 용량별 연결을 식별하고, 병목 현상을 파악할 수 있습니다.
* [오류 및 문제 해결 안내서](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages) 및 [알려진 제한 사항](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-workspace/workspace-faq/aw-limitations) 문서를 사용하여 최대 로드 중 지연 시간이 늘어나는지 확인하십시오.
* 관리자가 RAM을 통해 장기 실행/차단된 요청을 미리 일시 중단하거나 취소할 수 있는 권한을 부여합니다. [CJA의 보고 요청 취소](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests) 문서를 참조하십시오.

### 모범 사례

* 트래픽이 적은 기간 동안 내보내기/보고서를 예약하여 로드를 원활하게 하고 지연을 최소화합니다. [예약된 보고서](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-components/scheduled-projects-manager) 문서를 참조하십시오.
* 요청 분산: 하루 종일 서로 다른 간격으로 보고서를 예약합니다.
* 패널을 줄이고, 세그먼트를 단순화하고, 날짜 범위를 단축하고, 과도한 동시 작업을 방지할 수 있습니다. 자세한 내용은 [CJA Workspace 성능 최적화](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-workspace/workspace-faq/optimizing-performance) 문서를 참조하십시오.

### 문제 해결

* 작업 영역 오류를 해결할 때 원인 및 권장 작업에 대한 오류 메시지를 참조하십시오. 병목 현상을 제거하고 동시성을 효과적으로 관리하려면 RAM([!UICONTROL 보고 활동 관리자])을 사용하십시오. 자세한 내용은 [CJA Workspace 오류 처리](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages)를 참조하십시오.
* RAM([[!UICONTROL CJA의 Reporting Activity Manager]](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview))을 사용하여 문제가 있는 사용자, 쿼리 또는 프로젝트를 정확하게 찾아내고 필요에 따라 우선 순위를 지정하고 종료/취소합니다.

### 피크 이후 학습

* 휴일/피크 기간이 끝나면 성능 및 문제 로그를 검토하여 제공된 모범 사례의 영향을 평가합니다.
* 느린 쿼리 및 사용자 작업을 검토하여 다음 시즌에 최적화할 수 있는 패턴/트렌드를 확인하십시오.
* 사용자 및 관련자로부터 피드백을 수집하고 새로 얻은 통찰력을 사용하여 자체 Runbook 및 준비 계획을 업데이트합니다.
* 계정 팀을 통해 Adobe 팀에 피드백을 제공합니다.

</details>

<details>
<summary><h2 id="commerce" style="display: inline-block;">Adobe Commerce 휴일 준비 안내서</h2></summary>

조직의 성공적인 성수기를 보장하려면 높은 트래픽을 위한 Adobe Commerce 디지털 스토어를 준비하는 것이 중요합니다.

## 수요 예측

* 최대 휴일 판매 기간(11월 중순부터 1월 중순까지) 동안 Adobe은 클라우드 인프라에서 호스팅되는 모든 Adobe Commerce 가맹점이 휴일 급증 용량 요청을 제출하여 방문자 증가에 대해 적극적으로 계획할 것을 권장합니다. 자세한 내용은 [클라우드 인프라의 Adobe Commerce에 대한 휴일 서지 용량 요청](https://experienceleague.adobe.com/ko/docs/commerce-knowledge-base/kb/announcements/commerce-announcements/holiday-surge-capacity-requests-for-magento-commerce-cloud)을 참조하십시오.

## 크기 조정 준비

[계획 및 피벗: Adobe Commerce(및 선택 사항인 Adobe Experience Cloud 도구)를 사용하여 실행 가능한 전략을 제공하는 2025년 성수기에 대한 전략적 접근](https://experienceleague.adobe.com/ko/perspectives/planning-and-pivoting-a-strategic-approach-to-peak-season-2025) 안내서의 권장 사항을 따라 가장 바쁜 시기에 뛰어난 고객 경험을 계획, 피벗 및 제공할 수 있습니다.

## 모범 사례

* Adobe의 가이드 [높은 트래픽을 위한 인프라를 준비하는 방법 - 성수기 5Ps 성능](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic)을 따르십시오.
* 트래픽이 많도록 인프라를 준비하고, 가동 중단을 방지하고, 휴일 기간에 성능을 최적화하는 방법에 대한 팁은 [Commerce 휴일 준비를 위한 기술 팁](https://experienceleague.adobe.com/ko/docs/commerce-knowledge-base/kb/how-to/tech-tips-for-commerce-holiday-readiness)을 확인하십시오.

</details>

<details>
<summary><h2 id="aem" style="display: inline-block;">Adobe Experience Manager (AEM) 휴일 준비 안내서</h2></summary>

휴가철이 빠르게 다가오고 있으며, 많은 Adobe 고객들에게 이것은 최대 판매 기간의 시작을 의미한다. 귀사의 성공을 위해 다가오는 트래픽 급증에 대해 만반의 준비를 갖추도록 하고 싶습니다.

## Adobe Experience Manager(AEM) 클라우드 서비스

조직에서 휴가철 동안 가장 바쁜 순간을 경험하는 경우 최대 트래픽을 수용하도록 Adobe Experience Manager 사이트를 최적화하는 방법에 대해 고민할 수 있습니다. 다행히도 Adobe Experience Manager Cloud Services를 사용하면 사이트에 자동 확장 기능이 이미 갖춰져 있으므로 트래픽에 급격한 변화가 있더라도 방문자가 원활한 경험을 할 수 있습니다.

## 크기 조정 준비

* Adobe Experience Manager Cloud Services를 사용하여 높은 트래픽을 준비하는 방법에 대한 자세한 인사이트 및 지침은 다음 링크를 참조하십시오.

   * AEM as a Cloud Service의 [CDN](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/content-delivery/cdn)
   * [AEM as a Cloud Service 캐싱](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/cloud-service/caching/overview)

* Ultimate Success 고객이고 최근에 Adobe 계정 팀과 거래량 예측 정보를 공유한 경우 이미 보기가 있으므로 다시 당사에 전송하는 것에 대해 걱정하지 마십시오.

우리는 귀하의 여정의 모든 단계에서 당신을 지원하기 위해 여기에 있습니다. 질문이 있거나 문제가 있는 경우 언제든지 [지원 티켓을 제출](https://experienceleague.adobe.com/ko/docs/learning-manager/using/faq/how-to-submit-support-ticket)하세요.

휴가철 마케팅 캠페인을 준비하려면 [AEMaaCS 사용 안내서: 소개 - 마케팅 캠페인 매개 변수](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/content-delivery/caching#marketing-parameters) 설명서를 확인하십시오.

## 보안 및 관리

AEM 웹 사이트 트래픽 보안/보호에 대한 자세한 내용은 AEM as a Cloud Service 자습서의 [개요 - AEM 웹 사이트 보호](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/cloud-service/security/traffic-filter-and-waf-rules/overview) 문서를 참조하십시오.

## 휴일 유지 관리 계획

Adobe은 중요한 휴일 기간 동안 중단 없는 서비스를 보장하기 위해 유지 관리 제외 기간을 예약했습니다.

* **자동 업데이트가 없음**:
   * 2025년 11월 24일 - 2025년 12월 2일
   * 2025년 12월 15일 - 2026년 1월 2일

이렇게 하면 트래픽이 많은 기간 동안 안정성이 보장됩니다. 전체 릴리스 일정 및 유지 관리 기간은 [AEM 릴리스 로드맵](https://experienceleague.adobe.com/ko/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap)을 참조하세요.

## Adobe Experience Manager(AEM) 및 Adobe Managed Services(AMS)

Adobe Managed Services을 활용하는 AEM 고객은 CSE와 사전 예방적으로 협력하여 공휴일의 보장 요구 사항을 계획할 수 있습니다.

</details>

<details>
<summary><h2 id="marketo" style="display: inline-block;">Adobe Marketo 휴일 준비 안내서</h2></summary>

Adobe Marketo을 사용하여 성공적인 휴일 캠페인을 위해서는 팀이 이메일 인증 설정을 확인하고, 데이터베이스를 정리하고, 보안을 유지하고, 캠페인 로직과 일정을 최적화하고, 이메일 렌더링 및 전달성을 철저히 테스트하고, 최대 성능과 참여에 대한 지원 준비를 간소화해야 합니다.

## 크기 조정 준비

* SPF/DKIM 설정을 확인하고 모든 것이 계속 설정되고 올바르게 작동하는지 확인하십시오. 자세한 내용은 [전자 메일 배달 가능성을 위한 SPF 및 DKIM 설정](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-spf-and-dkim-for-your-email-deliverability) 문서를 참조하십시오.
* 비활성/유효하지 않은 레코드를 제거하여 Marketo 데이터베이스를 감사 및 정리합니다. 이렇게 하면 대부분의 판매 준비 잠재 고객의 받은 편지함에 땅을 보낼 가능성이 높아집니다. 자세한 내용은 [Marketo 데이터베이스 상태 검사 및 정리 방법](https://nation.marketo.com/t5/champion-program-blogs/marketo-database-health-check-up-amp-how-to-keep-it-clean/ba-p/323563) 문서를 참조하십시오.
* 팀 구성원이 작업을 수행하고 이메일에 대한 의도하지 않은 액세스 또는 변경을 방지할 수 있는 올바른 권한을 가지고 있는지 확인하십시오. **[!UICONTROL 관리자]**&#x200B;를 통해 변경하거나 **[!UICONTROL Admin Console]**&#x200B;을 통해 변경하든 관계없이 모든 작업을 수행할 수 있습니다. [사용자 역할 및 권한 관리](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions) 문서를 참조하십시오.
* Launchpad 통합을 검토하여 올바른 인증을 확인하고 잠재적 오류를 해결한 후 사용합니다. [Marketo 개발자 안내서: 인증](https://experienceleague.adobe.com/ko/docs/marketo-developer/marketo/rest/authentication) 문서를 참조하십시오.

## 모범 사례

효율성은 Marketo이 캠페인의 우선 순위를 지정하고 처리하는 방법을 정확히 이해하는 것에서부터 시작됩니다. 이러한 최적화 팁을 통해 캠페인에 속도의 이점을 제공하십시오.

* Marketo이 캠페인 흐름 단계 처리에 우선 순위를 두는 방법을 이해하는 것은 긴급하거나 우선 순위가 높은 이메일이 의도치 않게 지연되는 것을 방지하기 위해 중요합니다. [캠페인 처리 작동 방식](https://nation.marketo.com/t5/knowledgebase/how-campaign-processing-works/ta-p/248264) 문서를 참조하십시오.
* 스마트 목록 논리를 염두에 두면 캠페인이 신속하게 최대 성능으로 실행되도록 하는 데 도움이 됩니다. [스마트 목록 모범 사례](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/best-practices-for-smart-lists) 문서를 참조하십시오.
* **[!UICONTROL 앞쪽 시작]** 또는 **[!UICONTROL 수신자 시간대]**&#x200B;를 사용하면 전송 전에 전자 메일을 빌드하여 지연을 줄이고 리소스 논리가 높은 잠재 고객에 대한 추가 준비 시간을 제공할 수 있습니다. 자세한 내용은 [전자 메일 프로그램 시작 시점](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/head-start-for-email-programs) 및 [받는 사람 표준 시간대로 전자 메일 프로그램 예약](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/scheduling-with-recipient-time-zone/schedule-email-programs-with-recipient-time-zone) 문서를 참조하십시오.
* 캠페인이 활성 상태이고 잠재 고객이 이동하고 있는 경우 흐름 단계에 오류가 표시됩니다. 빠른 조정으로 해결하고 싶지만 라이브 대기 단계를 변경하거나 흐름을 재정렬할 때 어떤 일이 발생하는지 알아두면 많은 두통을 피하고 나중에 정리하는 데 도움이 될 수 있습니다. [대기 단계의 구성원과 함께 캠페인 흐름 편집](https://nation.marketo.com/t5/knowledgebase/editing-campaign-flow-with-members-in-wait-steps/ta-p/254294) 문서를 참조하십시오.

## 테스트 및 유효성 검사

**[!UICONTROL 보내기]**&#x200B;를 누르기 전에 전자 메일이 의도한 대로 정확하게 표시되고 수행되는지 확인하십시오.

* Marketo은 이메일 모양을 테스트하여 이메일 모양이 사용자가 의도한 대로 표시되는지 확인하는 여러 가지 방법을 제공합니다.
   * **[!UICONTROL 미리 보기]** 함수를 사용하여 세그먼테이션 또는 개별 리드를 미리 보고 다이내믹 콘텐츠와 토큰이 올바르게 렌더링되도록 하십시오. [다이내믹 콘텐츠로 이메일 미리 보기](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/email-marketing/general/functions-in-the-editor/preview-an-email-with-dynamic-content) 문서를 참조하십시오.
   * 테스트 레코드에 다이렉트 이메일을 빠르고 쉽게 보내 다양한 클라이언트/디바이스에서 이메일이 어떻게 표시되는지 확인합니다. [스마트 목록에서 단일 흐름 단계 실행](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/using-smart-lists/run-a-single-flow-step-from-a-smart-list) 문서를 참조하십시오.
   * [!DNL Litmus] 사용자의 경우 계정을 통합하고 전자 메일 편집기에서 바로 렌더링 테스트를 시작하는 것이 이전보다 더 쉬워졌습니다. [테스트 전자 메일 렌더링 사용 [!DNL Litmus]](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/email-marketing/email-designer/test-email-rendering) 문서를 참조하십시오.
* [!DNL SpamAssassin]과(와) 통합되어 이메일의 콘텐츠를 검토하고 받은 편지함에 도달하거나 *스팸*(으)로 표시될 가능성에 대한 점수를 할당하는 이메일 스팸 보고서 기능을 확인하십시오. [이메일 스팸 보고서](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/email-marketing/email-designer/spam-report) 문서를 참조하십시오.
* [!UICONTROL 캠페인 큐]를 주시하여 캠페인이 처리 중인지 확인하고 긴급도가 높은 항목의 우선 순위를 올바르게 지정하세요. [이(가) 실행 중인지 확인하십시오.](https://nation.marketo.com/t5/knowledgebase/is-my-campaign-running/ta-p/248662) 문서.

## 지원 환경 간소화

문제가 발생하면 속도가 문제가 되므로 Marketo 지원 센터에서 도움을 받으십시오! 앞뒤로 오가는 것을 방지하고 팀이 더 빠른 해결을 위해 노력할 수 있도록 이러한 세부 사항을 지원 사례에 포함하십시오. [Marketo 지원 작업에 대한 모범 사례](https://nation.marketo.com/t5/knowledgebase/best-practices-for-working-with-marketo-support/ta-p/253491) 문서를 참조하십시오.

이 안내서를 사용하면 이 중요한 기간 동안 참여와 전환을 유도하는 강력한 위치에서 시작한다는 것을 알고 있으므로 약간 더 쉬울 수 있습니다. 걱정은 많지만 스트레스는 그럴 필요가 없어 오늘 준비를 시작하고 이번 휴가 시즌을 아직 가장 성공적으로 만드십시오.

</details>

<details>
<summary><h2 id="workfront" style="display: inline-block;">Adobe Workfront 휴일 준비 안내서</h2></summary>

휴가 시즌을 대비하여 Adobe Workfront을 준비하려면 팀은 지원 담당자를 업데이트하고, 내부 일정을 Adobe과 맞추고, 최대 기간 동안 큰 변화를 피하고, 원활한 운영을 위해 자동화 및 통합을 사전 예방적으로 모니터링해야 합니다.

## 크기 조정 준비

휴일 동안 원활한 지원 경험을 보장하기 위해:

* 승인된 지원 담당자를 미리 검토하고 업데이트합니다.
* 중요한 문제가 발생하는 경우 주요 관련자가 지원 팀과 공동 작업을 수행할 수 있는지 확인합니다.
* 휴일 기간 동안 제품 또는 워크플로우가 변경되는 경우 최상의 처리 시간을 위해 11월 중순 이전 또는 1월 초 이후로 일정을 예약하는 것이 좋습니다.
* 내부 휴무 일정을 Adobe 담당자에게 전달하여 정렬을 확인합니다.

## 테스트 및 유효성 검사

Workfront 릴리스에 대한 최신 정보를 확인하고 샌드박스 환경에서 새로운 기능을 테스트하십시오.

* [Adobe Workfront 릴리스 준비](https://experienceleague.adobe.com/ko/docs/workfront/using/product-announcements/product-releases/release-readiness)
* [Workfront 릴리스 노트 보관](https://experienceleague.adobe.com/ko/docs/workfront/using/product-announcements/product-releases/product-releases)
* [2025년 1분기 릴리스 개요](https://experienceleague.adobe.com/ko/docs/workfront/using/product-announcements/product-releases/release-25-q1/25-q1-release-overview)
* [Workfront 릴리스 웨비나 녹화](https://experienceleague.adobe.com/ko/docs/events/workfront-recordings/releases/25-1-release-webinar)

## 모범 사례

* 사전 계획: 내부 휴가 일정의 영향을 받을 수 있는 시스템 종속성 또는 예약된 자동화를 식별합니다.
* 지속적인 커뮤니케이션: 내부 팀 및 Adobe 지원 팀에 계획된 유지 관리 또는 주요 이벤트에 대한 정보를 제공합니다.
* 대시보드 사용: 주요 통합 및 자동화를 모니터링하여 성능 문제의 조기 징후를 포착합니다.
* 조기 에스컬레이션: 서비스 저하가 예상되거나 관찰되는 경우 즉시 지원 티켓을 여십시오. 서비스가 심각해질 때까지 기다리지 마십시오.

미리 계획하고, 명확한 커뮤니케이션을 유지하고, 문제를 조기에 악화시킴으로써 조직은 중단을 최소화하고 Workfront이 연휴 기간 동안 중요한 워크플로우를 계속 지원할 수 있습니다.

</details>

<details>
<summary><h2 id="campaign" style="display: inline-block;">Adobe Campaign 휴일 준비 안내서</h2></summary>

휴가 준비를 위해 Adobe Campaign을 준비하려면 팀은 전달성 설정을 사전에 확인하고, 대상자 세분화 및 메시지 빈도를 최적화하며, 인프라 확장성을 보장하고, 크로스 채널 캠페인 오케스트레이션을 테스트하여 시즌 볼륨 및 참여 스파이크를 효과적으로 처리해야 합니다.

## 연말연시 캠페인을 돋보이게 할 수 있는 전문가의 팁

연말연시 선물 준비를 미리 시작할수록 좋은 것처럼, 대성공을 거둬야 하는 연말연시 마케팅 캠페인을 위한 계획도 미리 시작할수록 좋습니다. Adobe Campaign을 사용하면 조직의 모든 휴일 소망을 실현하는 캠페인을 디자인, 계획 및 실행할 수 있습니다. 하지만 한 해를 멋지게 마무리할 수 있는 캠페인을 실행하기 위한 팁을 모두 알고 계시나요? 이 비디오에서 [연말연시 캠페인을 돋보이게 할 수 있는 전문가 팁](https://experienceleague.adobe.com/ko/docs/events/experience-league-live-recordings/episodes/exl-live-episode-03)을 확인하세요. 이 팁은 게재 가능성 및 실행 모범 사례를 논의하며 Adobe Campaign에서 이 모든 작업을 수행하는 방법을 보여 줍니다.

## 휴가 기간에 대한 고려 사항 및 준비

이 비디오 [Adobe Campaign: 휴일 준비 - 휴일 기간 고려 사항 및 준비](https://helpx.adobe.com/kr/customer-care-office-hours/campaign/campaign-holiday-readiness.html)에서는 다음을 다룹니다.

* Campaign 커뮤니티 참여
* 전달성 - 휴일 및 그 이후에 대한 고려 사항!
* ACC(Adobe Campaign Classic) 및 ACS(Adobe Campaign Standard)에 대한 기술 권장 사항

Adobe Campaign이 휴일 성수기를 맞이할 수 있도록 조직은 전달성 확인을 완료하고 캠페인 구성을 검증하며 확장 가능한 인프라 및 크로스 채널 오케스트레이션이 마련되어 휴일 기간 동안 대량의 시간에 민감한 캠페인을 자신 있게 실행할 수 있도록 해야 합니다.

</details>

<details>
<summary><h2 id="analytics" style="display: inline-block;">Adobe Analytics 휴일 준비 안내서</h2></summary>

휴가철이 다가옴에 따라 Adobe Analytics을 사용하는 조직은 트래픽 피크 기간 동안 데이터 정확도, 플랫폼 성능 및 보고 안정성을 보장하기 위해 사전 조치를 취해야 합니다. Adobe은 팀이 효율적으로 준비할 수 있도록 여러 리소스 및 모범 사례를 제공합니다.

## 트래픽 예측

적절한 하드웨어 할당 및 시스템 응답성을 보장하기 위해 Adobe에서는 **시간당 최대 및 일별 서버 히트/호출 볼륨**&#x200B;을 미리 제출할 것을 권장합니다.

* 대량 기간 동안 실시간 의사 결정에 있어 데이터를 사용할 수 있는 속도를 파악하는 것이 중요하므로 [트래픽 스파이크 예약 및 하드웨어 할당 리드 타임](https://experienceleague.adobe.com/ko/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/t-traffic-schedule-spike#hardware-allocation-lead-times)을 확인하십시오.

* 예기치 않은 트래픽 스파이크 및 하드웨어 문제를 포함하여 [Adobe Analytics 데이터 지연 개요](https://experienceleague.adobe.com/ko/docs/analytics/technotes/latency)에서 Adobe Analytics의 데이터 가용성과 지연에 영향을 주는 사항을 알아보고 데이터 지연을 줄이기 위한 권장 전략을 살펴보십시오.

## 모범 사례

데이터 피드를 사용하여 원시 분석 데이터를 내보내는 팀의 경우, Adobe에서 피드 구성을 최적화하고 일반적인 위험을 방지하는 지침을 제공합니다.

* [Adobe Analytics 데이터 피드에 대한 우수 사례](https://experienceleague.adobe.com/ko/docs/analytics/export/analytics-data-feed/data-feeds-best-practices)

휴일 동안 빠르고 안정적인 보고를 유지하기 위해 Adobe은 다음을 권장합니다.

* [Analysis Workspace 성능 최적화](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance)
* [Report Builder 문제 해결 및 모범 사례: 요청 최적화를 위한 권장 사항](https://experienceleague.adobe.com/ko/docs/analytics/analyze/legacy-report-builder/troubleshoot#section_33EF919255BF46CD97105D8ACB43573F)
* [Analytics 구성 요소 안내서: 예약된 보고서 큐](https://experienceleague.adobe.com/ko/docs/analytics/components/scheduled-reports-admin)

## 휴일 유지 관리 계획

Adobe은 일반적으로 서비스를 중단하지 않도록 최대 휴일 기간 동안 **유지 관리 제외 기간**&#x200B;을 적용합니다. 고객은 Experience League을 통해 Adobe의 릴리스 및 유지 관리 일정을 모니터링하고 지원 계획을 위해 Adobe 계정 팀과 협력해야 합니다.

조직은 이러한 지침을 따르고 Adobe의 공개 설명서를 활용하여 Adobe Analytics 구현이 강력하고, 반응적이며, 휴가철 수요에 대비할 수 있도록 할 수 있습니다.

</details>

<details>
<summary><h2 id="target" style="display: inline-block;">Adobe Target 휴일 준비 안내서</h2></summary>

휴가철은 참여를 위한 흥미로운 기회를 제공하지만 트래픽 급증 및 개인화 시스템에 대한 수요 증가와 같은 과제도 함께 제공됩니다. 이 중요한 기간 동안 원활한 경험을 제공할 수 있도록 Adobe Target 구현이 준비되도록 주요 권장 사항을 컴파일했습니다.

## 수요 예측

먼저 20~50% 이상의 트래픽 스파이크를 예측하고 인프라가 로드를 처리할 수 있는지 확인합니다. Adobe Target, Analytics 및 AEP에서 활동 및 데이터 볼륨을 예측하여 예상치 못한 상황을 방지합니다.

또한 체크아웃, 제품 추천, 프로모션 오퍼와 같은 미션 크리티컬한 여정을 식별하는 것이 중요하므로, 개인화 노력은 가장 중요한 부분에 중점을 둡니다.

[Adobe Target을 사용한 최적화 모범 사례](https://experienceleague.adobe.com/ko/docs/target-learn/tutorials/administration/strategy/target-best-practices-for-optimization)를 참조하세요.

## 크기 조정 준비

* 웹 사이트 및 모바일 장치의 트래픽 증가를 계획하고 Target 지원 팀에 알려 차단된 호출을 방지하도록 서버 용량을 늘리십시오.
* 로드/펜 테스트의 경우 Target 지원 팀에 미리 알려야 합니다.
* 최신 `at.js`/배달 API 버전으로 업그레이드하십시오.
* 중요하지 않은 변경 내용을 고정하고, 대체 경험을 준비합니다.
* 지원 및 에스컬레이션 프로세스를 조정하고 사전 경고를 활성화합니다.

## 테스트 및 유효성 검사

[QA 링크](https://experienceleague.adobe.com/ko/docs/target/using/activities/activity-qa/activity-qa)를 사용하여 콘텐츠 게재의 유효성을 검사하여 모든 것이 예상대로 작동하는지 확인하십시오. **[!UICONTROL 대상 규칙을 일치시켜 경험을 봅니다]** 전환을 사용하여 테스트 중인 활동에 적합한 대상을 확인합니다. **[!UICONTROL 목표 지표]** 구성이 활동의 **[!UICONTROL 목표]**&#x200B;에 정렬되었는지 다시 확인하십시오. 그리고 만일의 경우를 대비하여 항상 백업 계획을 준비하십시오.

## 모범 사례

시작하기 전에 구현을 [Adobe Target 제한](https://experienceleague.adobe.com/ko/docs/target/using/troubleshoot/target-limits) 이내에 두고 [GDPR 및 CCPA 준수](https://experienceleague.adobe.com/ko/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation)를 미리 확인하십시오. 100개 미만의 활성 활동을 유지하고 오래된 활동을 아카이빙하여 작업 능률화 유지 AI 기반 최적화를 위해 **[!UICONTROL 자동 할당]**/**[!UICONTROL 자동 타겟]**&#x200B;을 활용하십시오. 롤백 계획 및 실시간 모니터링 대시보드를 설정합니다.

## 보안 및 관리

경험을 개인화하기 전에 GDPR 및 CCPA에서 동의 준수를 확인합니다. 프로필 매개변수에 PII(개인 식별 정보)를 저장하지 않고 API 보안을 확인하여 고객 데이터를 보호합니다.

</details>
