---
keywords: Experience Platform 지원;플랫폼 지원;인텔리전트 서비스 지원;고객 ai 지원;attribution ai 지원;rtcdp 지원;지원 티켓 제출;고객 지원
title: Adobe Experience Cloud Customer One for Enterprise
description: Adobe 고객 지원 경험
seo-description: Adobe Customer Support Experience
exl-id: 276e0862-6f7e-491e-b63e-10a50b7238c2
source-git-commit: 361a370c64197b77ef5437efecfc41f5bd72a16e
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 0%

---

# Adobe 고객 지원 경험

## Experience League 지원 티켓

이제 [Experience League](https://experienceleague.adobe.com/home?lang=ko#support)을 통해 지원 티켓이 제출되었습니다. 지원 티켓을 제출하는 방법에 대한 지침은 [지원 티켓 제출](#create-a-support-ticket-with-experience-league) 섹션을 검토하십시오.

Adobe 고객 지원 팀과 상호 작용하는 방법을 개선하기 위해 노력하고 있습니다. 당사의 비전은 Experience League을 사용하여 단일 진입점으로 이동하여 지원 경험을 간소화하는 것입니다. 라이브 상태가 되면 조직은 Adobe 고객 지원 센터에 쉽게 액세스하고, 제품 간 공통 시스템을 통해 서비스 내역을 보다 잘 파악할 수 있으며, 단일 포털을 통해 전화, 웹 및 채팅을 통해 도움을 요청할 수 있습니다.

Adobe Commerce 사용자인 경우 Adobe Commerce에 대한 Experience League 지원 사용 안내서의 [지원 사례 제출](https://experienceleague.adobe.com/ko/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)을 참조하세요.

## 사례 제출에 필요한 권한 있는 역할 지원 {#submit-ticket}

[Experience League](https://experienceleague.adobe.com/home?lang=ko#support)에서 지원 티켓을 제출하려면 시스템 관리자가 지원 관리자 역할을 할당해야 합니다. 조직의 시스템 관리자만 이 역할을 할당할 수 있습니다. 제품, 제품 프로필 및 기타 관리 역할은 지원 관리자 역할을 할당할 수 없으며 지원 티켓을 제출하는 데 사용되는 **[!UICONTROL 사례 만들기]** 옵션을 볼 수 없습니다. 다양한 유형의 관리자 역할과 해당 권한에 대한 자세한 내용은 [관리자 역할](admin-roles.md)을 참조하세요.

Commerce을 사용하는 경우 지원 사례와 작업에 대한 액세스 권한을 공유하는 프로세스가 다릅니다. 자세한 내용은 Adobe Commerce용 Experience League 지원 사용 안내서의 [공유 액세스: 다른 사용자가 계정에 액세스할 수 있는 권한 부여](https://experienceleague.adobe.com/ko/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#shared-access)를 참조하십시오.

### 조직에 지원 권한 추가

지원 관리자 역할은 지원 관련 정보에 대한 액세스 권한이 있는 비관리 역할입니다. 지원 관리자는 문제 보고서를 보고 만들고 관리할 수 있습니다.

관리자를 추가하거나 초대하려면:

1. Admin Console에서 **[!UICONTROL 사용자]** > **[!UICONTROL 관리자]**&#x200B;를 선택합니다.
1. **[!UICONTROL 관리자 추가]**&#x200B;를 클릭합니다.
1. 이름 또는 이메일 주소를 입력합니다.

   유효한 이메일 주소를 지정하고 화면의 정보를 채워 기존 사용자를 검색하거나 새 사용자를 추가할 수 있습니다.

   ![관리자 추가](assets/admin-console-add-admin.png)

1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다. 관리자 역할 목록이 나타납니다.

사용자에게 지원 관리자 역할을 할당하려면(사용자가 지원에 문의할 수 있도록 활성화):

1. **[!UICONTROL 관리자 지원]** 옵션을 선택하십시오.

   ![관리자 권한 편집](assets/edit-admin-rights.png)

1. 다음 두 옵션 중 하나를 선택합니다.

   * 옵션 1: **[!UICONTROL 기본 지원 관리자]**. 사용자에게 모든 솔루션(Marketo Engage 제외)에 대한 액세스 권한을 부여하려면 이 옵션을 선택합니다.
   * 옵션 2: **[!UICONTROL 제품 지원 관리자]**: Marketo Engage 지원을 위해 이 옵션을 선택하십시오. 사용자에게 액세스 권한을 부여할 Marketo Engage 인스턴스를 선택합니다.

   ![관리자 권한 편집 Marketo](assets/edit-admin-rights-advanced.png)

1. 선택한 후에는 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

사용자가 `message@adobe.com`에서 새 관리 권한과 관련된 전자 메일 초대를 받습니다.

조직에 가입하려면 전자 메일에서 **시작하기**&#x200B;를 클릭해야 합니다. 새 관리자가 전자 메일 초대의 **시작** 링크를 사용하지 않으면 Admin Console에 로그인할 수 없습니다.

로그인 프로세스의 일부로 아직 Adobe 프로필이 없는 경우 사용자에게 프로필을 설정하라는 메시지가 표시될 수 있습니다. 전자 메일 주소와 연결된 프로필이 여러 개인 경우 **팀에 참여**&#x200B;를 선택한 다음(메시지가 표시되면) 새 조직과 연결된 프로필을 선택해야 합니다.

![관리자 권한 확인](assets/admin-rights-confirmation.png)

자세한 내용은 관리 역할 설명서의 [Enterprise 관리자 역할 편집](admin-roles.md#add-enterprise-role) 지침을 따르십시오. 조직의 시스템 관리자만 이 역할을 할당할 수 있습니다. 관리 계층에 대한 자세한 내용은 [관리 역할](admin-roles.md) 설명서를 참조하십시오.

### Experience League으로 지원 티켓 만들기

>[!NOTE]
>
> 지원 티켓을 제출하기 전에 [Adobe 상태](https://status.adobe.com) 사이트에서 Adobe 시스템 성능, 가용성 및 알려진 문제를 확인하십시오.

Experience League은 자격이 있는 고객에게 개인화된 지원과 사용하기 쉬운 경험을 제공하기 위해 설계된 셀프서비스 지원 포털입니다.

1. [Experience League](https://experienceleague.adobe.com/home?lang=ko#support)에서 티켓을 만들려면 위쪽 탐색에서 **[!UICONTROL 지원]** 탭을 선택하십시오.

   ![Experience league 지원 탭](./assets/experience-league-support-tab.png)

1. **[!UICONTROL 홈]** 메뉴에서 **[!UICONTROL 지원 티켓 열기]**, **[!UICONTROL 사례 보기 및 관리]**, **[!UICONTROL 콜백 요청]**&#x200B;하거나 추가 학습 리소스에 액세스할 수 있습니다.

   ![Experience league 홈 메뉴](./assets/home-menu.png)

1. 사례를 제출하려면 **[!UICONTROL 지원 티켓 열기]**&#x200B;를 선택하세요. 사이드바 메뉴에서 **[!UICONTROL 티켓 열기]**&#x200B;를 선택할 수도 있습니다.

   ![Experience league 티켓 열기](./assets/open-support-ticket.png)

### 지원 티켓 작성

**[!UICONTROL 지원 티켓 열기]** 또는 **[!UICONTROL 티켓 열기]**&#x200B;를 선택하면 서비스 케이스 만들기 페이지가 나타납니다.

양식에서는 안내식 여러 단계 워크플로우를 사용합니다.

* 영향을 받는 Adobe 제품 선택
* 문제 설명
* 시스템 및 환경에 대한 세부 정보 제공
* 영향 및 긴급성 표시
* 연락처 정보 확인
* 세부 사항 검토 및 제출

다음 단계에 따라 지원 티켓을 만드십시오.

1. 제품 이름을 클릭하여 영향을 받는 제품을 선택한 후 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   ![Experience league 제품 선택](./assets/select-product.png)

1. **[!UICONTROL 문제 세부 정보]** 섹션에서 사례 제목을 입력하고 문제를 설명하고 재현 단계를 제공합니다.

   ![Experience league 문제 세부 정보](./assets/issue-details.png)

   다음과 같은 세부 정보를 포함합니다.

   * 수행하려는 작업
   * 무엇이 예상대로 작동하지 않음
   * 최근 환경 변경 사항
   * 이미 수행한 단계

   문제 세부 정보를 입력하면 Experience League은 양식 옆에 있는 패널에 AI 기반 권장 사항을 표시합니다. 이러한 권장 사항은 다음과 같습니다.

   * 관련 설명서 또는 알려진 솔루션 제안
   * 문제가 이미 해결되었는지 확인하는 데 도움이 됩니다.
   * 일반적인 문제에 대한 사례 제출의 필요성 감소

   서비스 케이스 작성 프로세스를 중단하지 않고 패널이 나타납니다. 언제든지 권장 사항을 검토하고 필요한 경우 사례를 계속 제출할 수 있습니다.

   ![Experience league 문제 세부 정보](./assets/ai-recommendations.png)

1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 시스템 정보]** 섹션에서 환경을 선택하고 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   > 선택한 제품에 따라 추가 필드가 표시될 수 있습니다. 이러한 필드에는 문제가 발생하는 환경에 대한 세부 정보가 포함됩니다.

   ![Experience league 시스템 정보](./assets/system-information.png)

1. **[!UICONTROL 영향]** 섹션에서 아래를 선택합니다.
   * 사례 우선 순위(P4 - 사내, P3 - 중요, P2 - 긴급, P1 - 중요)
   * 비즈니스 영향 (소규모, Medium, 대규모)

   ![Experience league 영향 세부 정보](./assets/impact.png)

   사례 우선 순위 및 비즈니스 영향이 지원 응답 시간에 미치는 영향에 대한 자세한 내용은 성공 계획 리소스 설명서에서 [지원에 대한 목표 초기 응답 시간](https://experienceleague.adobe.com/ko/docs/support-resources/data-sheets/overview#targeted-initial-response-times-for-support)을(를) 참조하십시오.

1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 연락처 정보]** 섹션에서 시간대를 선택하고 전화 번호를 입력한 다음 감시자를 추가하고 필요한 경우 파일을 첨부한 다음 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   ![Experience league 연락처 정보](./assets/contact-information.png)

1. **[!UICONTROL 검토 및 제출]** 섹션에서 사례 세부 정보를 검토하고 **[!UICONTROL 제출]**&#x200B;을 클릭하세요.

   ![Experience league 검토 및 제출](./assets/review-and-submit.png)

   **[!UICONTROL 검토 및 제출]** 단계에서는 입력된 모든 정보를 요약하고 다음 작업을 수행할 수 있습니다.

   * 한 곳에서 모든 사례 세부 정보 검토
   * 편집하려면 이전 단계로 돌아가십시오.
   * 진행률을 잃지 않고 검토 요약으로 돌아가기

제출 후:

* 서비스 케이스가 Experience League에 로그인되어 있습니다.
* 포털을 통해 업데이트를 추적하고 지원 팀과 통신할 수 있습니다.
* Adobe 지원은 제공된 우선 순위 및 영향에 따라 응답합니다

>[!TIP]
>
> **[!UICONTROL 티켓 열기]** 옵션 또는 **[!UICONTROL 지원]** 탭이 표시되지 않으면 시스템 관리자에게 문의하여 지원 관리자 역할을 할당하십시오.

>[!NOTE]
>
> 이 문제로 인해 프로덕션 시스템이 중단되거나 심각하게 중단되는 경우 즉각적인 지원을 위해 전화 번호가 제공됩니다.
