---
title: 조직 계층 관리
description: 글로벌 관리자가 Global Admin Console에서 조직의 계층을 관리하는 방법을 알아봅니다.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 6fcf16e3-0408-4961-9981-14d526e1ea28
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '1547'
ht-degree: 0%

---

# 조직 계층 관리

Enterprise에 적용됩니다.

글로벌 관리자가 Global Admin Console에서 조직의 계층을 관리하는 방법을 알아봅니다.

[Global Admin Console에 액세스](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console)한 후 새 조직을 만들고, 기존 조직을 계층에 추가하고, 조직을 삭제하고, 상위 조직을 변경할 수 있습니다. [Global Admin Console에 로그인](https://global-admin-console.adobe.com/)하려면 여기로 이동하세요.

조직은 Adobe 제품 및 사용자를 관리하는 데 사용되는 구조입니다. [Adobe Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)을(를) 통해 관리자는 조직의 제품 및 사용자의 배포 및 구성을 관리할 수 있습니다. [Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)을(를) 사용하면 전역 관리자가 여러 조직을 만들고, 관리하고, 삭제할 수 있습니다.

## 하위 조직 만들기

[전역 관리자](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)로서 계층 구조에 있는 조직의 하위 조직을 만들고 이름, 국가, 사용자 그룹, 제품, 제품 프로필, 관리자 및 정책을 설정할 수 있습니다.

새 하위 조직이 생성되면 다음 항목이 바로 위 상위에서 자동으로 상속됩니다.

- 조직의 [정책](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) 설정(있는 경우 잠금 포함).
- 시스템 관리자 목록(**[!UICONTROL 만들 때 시스템 관리자 상속]** [정책](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)에 의해 제어됨).
다음과 같은 이유로 시스템 관리자가 상속되지 않을 수 있습니다.
   - [도메인 신뢰](https://helpx.adobe.com/enterprise/using/directory-trust.html)가 없습니다.
   - 사용자 유형 제한(Adobe ID/Enterprise ID/Federated ID 사용자 정책 추가). [정책 세부 정보](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)에 대해 알아보세요.
- 상위 조직이 액세스할 수 있는 도메인에서 Federated ID 또는 Enterprise ID 사용자에 대한 액세스. 이렇게 하면 상위 조직의 도메인 사용자를 하위 조직에서 사용할 수 있습니다. 사용자 액세스 상속은 **상위 조직에서 관리하는 디렉터리에서 사용자 상속** [정책](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)에 의해 제어됩니다.
- 공유 정책, 암호 정책 및 보안 연락처(**하위 조직이 만들어질 때 자산 공유 설정 상속** [정책](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)에 의해 제어됨).

1. [Global Admin Console](https://global-admin-console.adobe.com/)에 로그인합니다. **[!UICONTROL 조직]** 탭에서 하위 조직을 추가할 조직을 선택합니다.
2. **[!UICONTROL 추가+]** 아이콘을 선택합니다.
   ![조직 추가](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. 조직의 **이름** 및 **국가**&#x200B;을(를) 지정하십시오.\
   조직의 단순 이름은 4자에서 100자 사이여야 합니다. 경로 이름의 최대 길이는 255자입니다.
   ![하위 조직 추가](/help/adobe-support-tools-guide/assets/add-a-child-organization.png)
4. **[!UICONTROL 저장]**&#x200B;을 선택합니다.
5. 조직을 편집한 후 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택합니다. 검토 후 **[!UICONTROL 변경 내용 제출]**&#x200B;을(를) 선택하여 [실행](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)합니다.

## 하위 조직 삭제

[전역 관리자](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)로서 하위 조직을 삭제할 수 있습니다. 삭제 작업은 실행 취소할 수 없으며 루트 조직을 삭제할 수 없습니다. 삭제된 조직에 할당된 리소스는 상위 조직으로 반환됩니다. 조직이 삭제되기 전에 해당 상위 조직은 자동으로 하위 조직의 상위 조직이 됩니다.

다음 기준을 충족해야 조직을 삭제할 수 있습니다.

- 조직에 Sign 계정, Adobe Stock 구매 또는 저장소 저장소가 없습니다.
- 조직에 클레임된 도메인이 없습니다.
- 조직에 인스턴스화된 제품이 없습니다.
- 조직에 인스턴스화를 포함할 수 있는 Experience Cloud 제품이 없습니다.

>[!WARNING]
>
>조직을 삭제하면 사용자에게 영향을 줍니다. 조직을 삭제할 때 손실될 액세스 또는 정보가 없는지 확인합니다.

1. [Global Admin Console](https://global-admin-console.adobe.com/)에 로그인합니다. **[!UICONTROL 조직]** 탭으로 이동하여 삭제할 조직을 선택합니다.
1. **[!UICONTROL 삭제]** 아이콘을 선택하십시오.
   ![조직 삭제](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. **[!UICONTROL 조직 삭제]** 대화 상자에서 **[!UICONTROL 확인]**&#x200B;을 선택합니다.
1. 조직을 편집한 후 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택합니다. 검토 후 **[!UICONTROL 변경 내용 제출]**&#x200B;을(를) 선택하여 [실행](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)합니다.

## 조직 이름 바꾸기

조직 이름은 구매 중에 설정되는 회사 또는 기관의 공식 이름입니다. 로그인 중에 프로필을 선택할 때, 특히 여러 조직의 Adobe 제품에 액세스할 수 있거나 비즈니스 및 개인 프로필 중에서 선택해야 하는 경우 이 이름이 표시됩니다.

[전역 관리자](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)로서 사용자가 Creative Cloud 제품 및 서비스에 로그인할 때 올바른 프로필을 식별하는 데 도움이 되도록 상위 또는 하위 조직의 이름을 편집할 수 있습니다.

1. [Global Admin Console](https://global-admin-console.adobe.com/)에 로그인합니다. **[!UICONTROL 조직]** 탭에서 이름을 바꿀 조직을 선택합니다.
1. **[!UICONTROL 편집]** 아이콘을 선택합니다.
   ![조직 이름 바꾸기](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. 조직 이름을 업데이트하고 **[!UICONTROL 저장]**&#x200B;을 선택하세요.

>[!TIP]
>
>사용자가 올바른 프로필을 선택하는 데 도움이 되도록 명확하고 인식 가능한 조직 이름을 최대 255자까지 사용합니다. 특수 문자를 사용하지 말고 지역, 부서 또는 권한을 포함하는 것이 좋습니다. 또한 조직 계층 구조에서 흔하지 않은 약어와 모호하거나 유사한 이름을 사용하지 마십시오.

변경 사항이 감사 로그에 기록되고 모든 사용자에게 이메일로 알림이 전송되며 이름을 24시간 동안 다시 업데이트할 수 없습니다. [감사 로그를 보고 다운로드하는 방법을 알아보세요](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/download-audit-logs-and-export-reports).

## 조직의 상위 항목 변경

[전역 관리자](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)로서 **[!UICONTROL 계층 변경]** 단추를 사용하여 조직 계층에서 조직의 상위 항목을 다시 지정할 수 있습니다.

조직의 상위 항목을 변경하면 다음과 같은 영향을 받습니다.

- 조직을 다시 부모로 지정하면 다시 부모로 지정된 조직에 뿌리를 둔 전체 하위 트리가 이동합니다. 다시 가져온 조직 및 해당 하위 조직의 경로 이름이 새 위치를 반영하도록 업데이트됩니다.
- 이동된 조직의 [정책](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) 조직이 업데이트되어 정책에 대한 모든 잠금이 새 계층의 조직에서 유지됩니다.
- 계층에서 조직의 위치를 변경하면 해당 조직의 글로벌 관리자가 변경될 수 있습니다. 전역 관리 역할은 계층 아래로 상속되므로 새 상위 조직의 전역 관리자는 이동된 조직의 전역 관리자가 됩니다. 마찬가지로 글로벌 관리자는 이전 부모의 글로벌 관리자가 되어 해당 역할을 맡게 되면 이동된 조직에서 자신의 역할을 상실할 수 있습니다. 상속된 전역 관리 역할은 조직의 관리자 창에 나열되지 않습니다.
- 부모 재지정은 이동된 조직에서 사용 가능한 제품에도 영향을 줍니다. 가능하면 [제품 할당](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)이 새 상위 위치를 통해 오도록 업데이트됩니다.
- 새 상위 항목에서 오도록 제품 할당을 업데이트할 수 없는 경우 해당 제품의 제품 프로필과 함께 제품이 제거됩니다. 이 작업으로 인해 사용자는 액세스 권한을 잃을 수 있습니다. 새 위치에서 제품을 사용할 수 있으려면 이전 위치와 새 위치의 가장 가까운 공통 조상이 제품을 사용할 수 있어야 합니다.

>[!WARNING]
>
>육아 관리의 결과로 제품이 제거되면 사용자는 해당 제품에 액세스할 수 없게 됩니다.

1. [Global Admin Console](https://global-admin-console.adobe.com/)에 로그인합니다. **[!UICONTROL 조직]** 탭에서 **[!UICONTROL 계층 변경]**&#x200B;을 선택하여 조직의 부모 재지정을 활성화합니다.
2. 표시되는 팝업 화면에서 **[!UICONTROL 확인]**&#x200B;을 선택합니다.
3. 상위 항목을 다시 지정하려면 원하는 조직 위로 하위 조직을 끌어옵니다.
4. 조직을 다시 양육하려면 **[!UICONTROL 저장]**&#x200B;을 선택하세요.
5. 조직을 편집한 후 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택합니다. 검토 후 **[!UICONTROL 변경 내용 제출]**&#x200B;을(를) 선택하여 [실행](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)합니다.

작업이 완료되면 제품 할당으로 이동하여 제품 리소스 할당 변경을 반영하도록 [권한 부여 값을 변경](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)할 수 있습니다.

## 조직 매퍼를 사용하여 기존 조직 추가

[전역 관리자](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)로서 현재 Global Admin Console 계층에 속하지 않은 기존 조직을 조직 계층에 추가할 수 있습니다.

조직 계층에 팀 조직을 추가할 수도 있습니다. 팀 조직은 제품 할당 또는 제품 사용 롤업에 참여하지 않으며 Global Admin Console에서 팀 조직의 관리가 제한됩니다. 조직 계층에 이를 추가하여 이를 추적하고 구매하는 제품에 대한 가시성을 가질 수 있습니다. 팀 조직에는 하위 조직이 있을 수 없으며 엔터프라이즈 조직의 기능이 많지 않습니다.

[제품 할당에 대한 제한](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limitations)에 대해 자세히 알아보세요.

>[!WARNING]
>
> 동일한 스토리지 모델을 기반으로 하는 루트 조직에만 하위 조직을 추가할 수 있습니다. 따라서 사용자 스토리지 모델을 기반으로 하는 하위 조직만 사용자 스토리지 모델을 기반으로 하는 루트 조직에 추가할 수 있습니다. 또한 엔터프라이즈 스토리지 모델을 기반으로 하는 하위 조직은 엔터프라이즈 스토리지 모델을 기반으로 하는 루트 조직에만 추가할 수 있습니다.

**[!UICONTROL 조직 매퍼]** 탭에는 다음이 표시됩니다.

1. 하위 조직을 추가할 수 있는 가능한 상위 조직 목록이 포함된 드롭다운. 전역 관리자인 조직입니다.
1. 1단계에서 선택한 상위 조직 아래에 추가할 수 있는 하위 조직 목록입니다. 이러한 조직은 사용자가 시스템 관리자이고 이미 다른 조직의 하위 조직도 아닌 조직입니다.

조직이 전역 관리에 추가되면 조직 매퍼를 사용하여 추가된 조직의 제품은 구매로 유지됩니다. [제품 할당](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) 번호는 이러한 조직에서 롤업을 중지합니다.

1. [Global Admin Console](https://global-admin-console.adobe.com/)에 로그인하고 **[!UICONTROL 조직 매퍼]**(으)로 이동합니다.
2. 드롭다운 목록에서 상위 조직을 선택합니다.\
   전역 관리자로 직접 추가된 조직입니다. 드롭다운 목록에서 상위로 사용할 조직이 표시되지 않으면 계층에서 한 단계 높은 조직을 선택합니다. 조직 매퍼 작업이 완료되면 [계층 구조 변경](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/set-up-organizations#change-the-parent-of-an-organization)을 사용하여 새 조직을 트리의 아래로 이동하여 사용할 상위 조직을 가질 수 있습니다.
3. 이전 단계에서 선택한 조직의 하위 조직으로 추가할 조직을 선택합니다.
4. **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택합니다. 그런 다음 **[!UICONTROL 변경 내용 제출]**&#x200B;을 선택하여 [실행](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)합니다.
5. 변경 사항을 실행한 후 위의 단계를 반복하여 조직 계층에 하위 조직을 추가할 수 있습니다.

조직이 계층 구조에 있으면 **[!UICONTROL 조직]** 탭으로 이동하여 조직 정책, 관리자 또는 기타 설정을 조정할 수 있습니다.
