---
title: 감사 로그 다운로드 및 보고서 내보내기
description: 글로벌 관리자가 Global Admin Console에서 감사 로그 및 보고서를 보고, 필터링하고, 내보내는 방법을 알아봅니다.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 4b562a4d-14e5-4687-a1ae-6a435f087627
source-git-commit: 7211d382c6cfba6070c8c3203956a1193f64ffbe
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 2%

---

# 감사 로그 다운로드 및 보고서 내보내기

Enterprise에 적용됩니다.

글로벌 관리자가 Global Admin Console을 사용하여 감사 로그 및 보고서를 보고, 필터링하고, 내보내는 방법을 알아봅니다.

시작하려면 [Global Admin Console](https://global-admin-console.adobe.com/)에 로그인하세요. 그런 다음 **[!UICONTROL 인사이트]** 탭으로 이동하여 **[!UICONTROL 감사 로그]**&#x200B;를 선택하여 조직 전체에 걸쳐 수행된 모든 변경 사항을 추적합니다.

## 감사 로그 보기 및 다운로드

글로벌 관리자는 Global Admin Console에서 수행한 변경 사항에 대한 모든 가시성을 갖습니다. 발생한 시간 및 수행한 사용자를 포함하여 지난 90일 동안 수행한 작업에 대한 감사 로그를 모든 조직에서 검색할 수 있습니다.
- 감사 로그는 부적절한 시스템 액세스를 방지하고 조직 내에서 의심스러운 행동을 감사하여 지속적인 규정 준수를 보장하는 데 도움이 됩니다.
- Global Admin Console에서 사용할 수 있는 로그에는 전역 관리자가 액세스할 수 있는 이벤트만 포함됩니다. 사용자 할당 또는 사용자 이벤트는 포함되지 않습니다. 각 콘솔에서 제공하는 다양한 기능에 대해 [자세히 알아보세요](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview).
- 로그는 계층의 모든 조직에 대한 이벤트를 다루므로 모든 조직의 감사 로그를 한 번에 검색할 수 있습니다.

>[!NOTE]
>
> [Adobe Admin Console](https://adminconsole.adobe.com) 조직의 시스템 관리자는 [감사 로그](https://helpx.adobe.com/kr/enterprise/using/audit-logs.html)를 사용하여 사용자 할당 및 사용자 이벤트를 검토할 수 있습니다. 선택한 조직의 하위 조직에서 시스템 관리자가 수행한 작업도 감사 로그에 포함됩니다. 시스템 관리자가 Admin Console에서 변경한 내용을 [추적](https://helpx.adobe.com/kr/enterprise/using/audit-logs.html)하는 방법에 대해 자세히 알아보세요.

조직의 감사 로그를 보거나 다운로드하려면 다음을 수행하십시오.

1. 전역 관리자로서 [Global Admin Console](https://global-admin-console.adobe.com/insights)에 로그인하십시오.
1. **[!UICONTROL 인사이트]** > **[!UICONTROL 감사 로그]**&#x200B;를 선택합니다.

감사 로그에는 필터링된 이벤트에 대한 다음 정보가 표시됩니다.

| 필드 | 설명 |
|------ |-------------|
| 일자 | 로컬 시간대에 표시되는 이벤트의 날짜 및 시간입니다. |
| 이벤트 이름 | 수행된 작업에 대한 설명입니다. |
| 이벤트 세부 정보 | 가능한 경우 추가 이벤트 세부 정보. |
| 개체 이름 | 이벤트에 포함된 제품, 제품 프로필 또는 사용자 그룹의 이름입니다(해당하는 경우). |
| 영향을 받는 사용자 | 해당하는 경우 영향을 받는 사용자의 이메일 주소. |
| 관리 | 작업을 수행한 관리자의 이메일 주소. Adobe 백 엔드 시스템에서 작업을 수행한 경우 *System*&#x200B;이 표시됩니다. |
| IP 주소 | 작업을 수행한 컴퓨터의 IP 주소입니다. 이는 일반적으로 물리적 위치를 반영하지만 프록시 서버 또는 VPN 주소일 수 있습니다. |
| 조직 | 이벤트의 영향을 받는 조직의 이름. |

1. 다음 옵션을 사용하여 감사 로그를 필터링할 수 있습니다.

   - 영향을 받는 사용자 또는 관리자로 검색합니다.
   - 조직을 하나 이상 선택합니다.
   - 날짜 범위를 정의합니다.
   - 이벤트 이름별로 필터링합니다.
   - 필터를 결합하여 결과 범위를 좁힙니다(예: 특정 조직의 지난 7일 이벤트 보기).

   ![감사 로그](assets/audit-logs.png)

   *이벤트 이름, 영향을 받는 조직 또는 날짜 범위를 기준으로 감사 로그를 필터링합니다.*

   ![조직 선택](assets/select-organizations.png)

   *감사 로그를 필터링할 조직을 선택하십시오.*

1. 감사 로그를 내보내려면 **[!UICONTROL CSV 내보내기]**&#x200B;를 선택하여 필터링된 결과를 내보냅니다. 결과는 CSV 형식으로 다운로드됩니다.

내보내기에 포함된 필드에 대한 자세한 내용은 [로그 스키마](#log-schema)를 참조하십시오.

>[!NOTE]
>
>내보낸 감사 로그 보고서는 생성된 후 90일 동안 유지됩니다.


## 감사 로그 보고서 이해 {#log-schema}

내보낸 감사 로그 보고서에는 각 조직에 대한 다음 필드가 포함됩니다.

| 필드 | 설명 |
|------|------------|
| ID | 이벤트 ID |
| eventTime | 이벤트 날짜 및 시간(현지 시간대) |
| eventType | 이벤트 이름 |
| eventSubType | 가능한 경우 추가 이벤트 세부 정보 |
| actorEmail | 이벤트를 수행한 관리자의 이메일 주소. Adobe 백 엔드 시스템에서 이벤트를 수행한 경우 *System*&#x200B;이 표시됩니다. |
| 타겟 사용자 이메일 | 해당하는 경우 영향을 받는 사용자의 이메일 |
| 대상 그룹 이름 | 해당하는 경우 영향을 받는 사용자 그룹 |
| targetProductName | 해당되는 경우 영향을 받는 제품 |
| targetProfileName | 해당되는 경우 영향을 받는 제품 프로필 |
| ip 주소 | 작업을 수행한 컴퓨터의 IP 주소입니다. 일반적으로 물리적 위치를 반영하지만 프록시 서버 또는 VPN 주소일 수 있습니다. |
| organizationName | 영향을 받는 조직의 이름 |

## 내보내기 보고서 다운로드

전역 관리자가 [Global Admin Console](https://global-admin-console.adobe.com/insights)에서 조직 데이터를 내보내면 보고서가 처리되고 **[!UICONTROL 보고서 내보내기]**&#x200B;의 **[!UICONTROL 인사이트]** 탭에서 사용할 수 있습니다.

글로벌 관리자가 생성한 모든 보고서를 한 곳에서 사용할 수 있습니다. 보고서 내보내기 기능은 다음 시나리오에서 유용합니다.

- 조직이 많은 대규모 계층이 있는 경우 내보내기 파일이 처리될 때까지 더 이상 기다릴 필요가 없습니다. 동료 관리자가 생성한 보고서를 사용할 수 있습니다.
- 나중에 비교하기 위해 이러한 보고서를 더 이상 유지하거나 저장할 필요가 없습니다. 보고서는 90일 동안 유지되며 언제든지 다운로드하여 보고서를 비교할 수 있습니다.


내보내기 보고서를 다운로드하려면 다음 작업을 수행하십시오.

1. [Global Admin Console](https://global-admin-console.adobe.com/insights)에 로그인하고 **[!UICONTROL 인사이트]** > **[!UICONTROL 보고서 내보내기]**&#x200B;로 이동합니다.

   지난 90일 이내에 생성된 보고서가 표시됩니다. 90일 후 보고서를 다시 생성할 수 있습니다. [조직 구조](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/export-or-import-organization-structure-and-product-allocations#export-the-organization-structure)에 대한 보고서를 생성하는 방법을 알아봅니다.


   | 필드 | 설명 |
   |------|------------|
   | 보고서 | 보고서 생성 날짜 및 시간(현지 시간대) |
   | 형식 | 파일 형식(CSV, JSON, XLSX) |
   | 크기 | 파일 크기 |
   | 제작자 | 보고서를 생성한 관리자의 이메일 주소 |
   | 작업 | 보고서 다운로드 링크 |

1. 보고서를 다운로드하려면 **[!UICONTROL 다운로드]**&#x200B;를 선택하십시오.

   방금 생성한 보고서가 목록에 표시되지 않으면 **[!UICONTROL 새로 고침]**&#x200B;을 선택하세요.

   ![내보내기-보고서](assets/export-reports.png)

*지난 90일 동안 생성된 보고서를 다운로드합니다.*
