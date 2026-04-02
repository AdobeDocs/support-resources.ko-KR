---
title: Global Admin Console에서 제품 프로필 관리
description: 글로벌 관리자가 Global Admin Console에서 제품 프로필을 추가, 편집 및 삭제하는 방법을 알아봅니다.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: 6a0b2d9f-9e02-428c-a2be-bc457230f7e0
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: 579
ht-degree: 1%

---

# Global Admin Console에서 제품 프로필 관리

**적용 대상:** Enterprise

글로벌 관리자는 [Global Admin Console](https://global-admin-console.adobe.com/)에서 제품 프로필을 추가, 편집 및 삭제할 수 있습니다.

>[!NOTE]
>
>[Global Admin Console](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console)에서 조직을 선택하고 **[!UICONTROL 제품]**(으)로 이동합니다. 제품 프로필을 사용하여 제품에 대해 모든 또는 선택한 서비스를 활성화할 수 있습니다.

표준 Admin Console에서와 같이 제품 프로필을 사용하면 조직 내에서 제품 사용을 세밀하게 조정할 수 있습니다. **[!UICONTROL 제품 프로필 관리자]**&#x200B;라고 하는 관리자를 제품 프로필에 할당할 수도 있습니다. 이러한 관리자는 관리하는 제품 프로필에 최종 사용자를 추가할 수 있습니다.

제품 프로필을 관리하려면 제품을 선택합니다. 제품 프로필을 추가, 편집 및 삭제하는 컨트롤이 표시됩니다.

>[!NOTE]
>
>일부 제품의 경우 Global Admin Console에서 제품 프로필을 만들거나 편집할 수 없습니다. 이러한 경우 대신 [Admin Console](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)을(를) 사용하십시오.

## 제품 프로필 추가

1. [Global Admin Console](https://global-admin-console.adobe.com/)에서 편집할 조직을 선택한 다음 **[!UICONTROL 제품]** 탭으로 이동합니다.
1. 제품 프로필을 추가할 제품을 선택합니다.
1. **[!UICONTROL 프로필 추가]**&#x200B;를 선택합니다.
1. **[!UICONTROL 프로필 추가]** 대화 상자에 다음 세부 정보를 입력하십시오.

   | 필드 | 설명 |
   |---|---|
   | **[!UICONTROL 이름]** | 다른 제품 프로필 및 사용자 그룹과 구별되는 조직 내 제품 프로필의 고유 이름. |
   | **[!UICONTROL 할당량]** | 이 프로필에 할당된 타겟 라이선스 수입니다. |
   | **[!UICONTROL 사용자 그룹]** | 드롭다운에서 선택하거나 사용자 그룹 이름을 입력합니다. 사용자 그룹이 아직 없는 경우 [**[!UICONTROL 사용자 그룹&#x200B;]**](https://helpx.adobe.com/kr/enterprise/global-admin-console/manage-user-groups.html) 탭을 통해 먼저 만드십시오. |
   | **[!UICONTROL 관리자]** | 드롭다운에서 을 선택하거나 관리자의 이메일 주소를 입력합니다. 관리자가 아직 없는 경우 [**[!UICONTROL 관리자&#x200B;]**](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators) 탭을 통해 먼저 관리자를 만드십시오. |

   지정한 [!UICONTROL 사용자 그룹]에 제품 프로필이 할당되었습니다. 지정한 관리자는 관련 조직의 Adobe Admin Console을 통해 프로필을 관리할 수 있는 **[!UICONTROL 제품 프로필 관리자]**&#x200B;가 됩니다.

   ![프로필 추가](./assets/manage-product-profiles_add-profile.png)

1. **[!UICONTROL 알림]** 토글을 사용하여 전자 메일 알림을 활성화하거나 비활성화하십시오. 활성화되면 사용자가 프로필에 추가되거나 프로필에서 제거될 때 이메일로 알림을 받습니다.
1. 개별 **[!UICONTROL 서비스]**&#x200B;를 사용하여 제품 프로필에 특정 서비스를 사용하거나 사용하지 않도록 설정합니다. 자세한 내용은 [제품 프로필에 대한 서비스 사용/사용 안 함](https://helpx.adobe.com/kr/enterprise/using/enable-disable-services.html)을 참조하세요.
1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.
1. 조직 편집을 마치면 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택합니다. 검토 후 **[!UICONTROL 변경 내용 제출]**&#x200B;을(를) 선택하여 [실행](https://helpx.adobe.com/kr/enterprise/global-admin-console/execute-jobs.html)합니다.

## 제품 프로필 편집

1. 편집할 조직을 선택하고 **[!UICONTROL 제품]** 탭으로 이동한 다음 제품을 선택하십시오.
1. 관련 제품 프로필에 대해 **[!UICONTROL 추가 옵션]** ![추가 옵션](./assets/manage-product-profiles_more-options.png) 아이콘을 선택한 다음 **[!UICONTROL 프로필 편집]**&#x200B;을 선택합니다.
1. 필요에 따라 제품 프로필 세부 정보를 업데이트하고 **[!UICONTROL 저장]**&#x200B;을 선택합니다.
1. 조직 편집을 마치면 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택합니다. 검토 후 **[!UICONTROL 변경 내용 제출]**&#x200B;을(를) 선택하여 [실행](https://helpx.adobe.com/kr/enterprise/global-admin-console/execute-jobs.html)합니다.

## 제품 프로필 삭제

>[!WARNING]
>
> 제품 프로필을 삭제하면 해당 프로필의 멤버이거나 해당 프로필에 첨부된 사용자 그룹에 속한 모든 사용자에 대한 제품 액세스 권한이 제거됩니다.

1. 편집할 조직을 선택하고 **[!UICONTROL 제품]** 탭으로 이동한 다음 제품을 선택하십시오.
1. 관련 제품 프로필에 대해 **[!UICONTROL 추가 옵션]** ![추가 옵션](./assets/manage-product-profiles_more-options.png) 아이콘을 선택한 다음 **[!UICONTROL 프로필 삭제]**&#x200B;를 선택합니다.
1. 확인 대화 상자에서 **[!UICONTROL 확인]**&#x200B;을 선택합니다.
1. 조직 편집을 마치면 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택합니다. 검토 후 **[!UICONTROL 변경 내용 제출]**&#x200B;을(를) 선택하여 [실행](https://helpx.adobe.com/kr/enterprise/global-admin-console/execute-jobs.html)합니다.


## 관련 읽기

- [전역 관리 채택](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)
- [관리자 관리](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)
- [사용자 그룹 관리](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-user-groups)
- [하위 조직에 제품 할당](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/allocate-products)
- [보류 중인 작업 실행](https://helpx.adobe.com/kr/enterprise/global-admin-console/execute-jobs.html)
- [서비스 사용/사용 안 함](https://helpx.adobe.com/kr/enterprise/using/enable-disable-services.html)
- [Admin Console 개요](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)
