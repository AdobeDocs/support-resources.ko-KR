---
title: Global Admin Console에서 정책 템플릿 관리
description: 글로벌 관리자가 Global Admin Console에 저장된 조직에서 직접 또는 간접적으로 모든 하위 조직에 정책 템플릿을 적용하는 방법에 대해 알아봅니다.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: cf30f2a656ccb28b678ea6fcd8e4d56d7c8a8fb4
workflow-type: tm+mt
source-wordcount: 705
ht-degree: 0%

---

# Global Admin Console에서 정책 템플릿 관리

**적용 대상:** Enterprise

글로벌 관리자가 Global Admin Console에 저장된 조직에서 직접 또는 간접적으로 모든 하위 조직에 정책 템플릿을 적용하는 방법에 대해 알아봅니다.

>[!NOTE]
>
>[Global Admin Console](https://helpx.adobe.com/kr/enterprise/global-admin-console/adopt-global-administration.html)에서 편집할 조직을 선택하고 **정책 템플릿** 탭으로 이동하여 설정을 간소화하고 조직 간 일관된 정책 관리를 용이하게 합니다.
>
> [Global Admin Console에 로그인](https://global-admin-console.adobe.com/)

## 정책 템플릿 작동 방식

정책 템플릿은 조직과 함께 저장되며 해당 조직의 모든 글로벌 관리자가 볼 수 있습니다. 정책이 적용되면 각 조직에서 정책 템플릿의 항목을 개별적으로 설정합니다. 정책 템플릿이 조직에 적용되면 정책 템플릿의 각 항목이 조직의 정책에 적용되어 기존 정책 값이 대체됩니다.

### 잠긴 정책 동작

잠긴 정책에 대한 업데이트는 업데이트를 적용하는 사용자가 업데이트할 정책의 **[!UICONTROL 잠근 사용자]** 아이콘으로 표시된 조직의 전역 관리자일 경우에만 수행됩니다.

템플릿을 적용하는 사용자에게 정책의 잠금을 해제할 권한이 있는 경우 정책 잠금은 적용된 템플릿(잠김 또는 잠금 해제)의 값을 가져옵니다. 템플릿에 잠금 상태를 그대로 유지해야 한다고 표시되면 정책의 잠금 값은 이전과 동일하게 유지됩니다.

### 저장에 대한 중요 참고 사항

>[!NOTE]
>
>Global Admin Console에서 수행한 다른 변경 사항과 달리, 정책 템플릿에 대한 편집 내용은 **[!UICONTROL 보류 중인 변경 내용 검토 - 제출]** 프로세스를 진행할 필요 없이 즉시 적용됩니다. 그러나 정책 템플릿이 적용되는 조직에서 보류 중인 변경 내용을 구현하려면 [제출](https://helpx.adobe.com/kr/enterprise/global-admin-console/execute-jobs.html)해야 합니다.

## 정책 템플릿 만들기

1. [Global Admin Console](https://global-admin-console.adobe.com/)에서 편집할 조직을 선택한 다음 **[!UICONTROL 정책 템플릿]** 탭으로 이동합니다.
1. **[!UICONTROL 템플릿 만들기]**.<br> 선택
   ![Pic1](./assets/DXSKB-3209-1-ga_14.png)
   <br>
1. **[!UICONTROL 정책 템플릿 만들기]** 대화 상자에서 정책 템플릿에 대한 **이름** 및 **설명**&#x200B;을 입력합니다.<br>정책 템플릿의 이름은 최대 100자까지 가능합니다.
1. 템플릿에 포함할 정책을 선택합니다.
1. 선택한 정책에 대한 값을 설정하십시오(아래 [정책 값 설정](#setting-policy-values) 참조).
1. **저장**&#x200B;을 선택합니다.

### 정책 값 설정 중 {#setting-policy-values}

템플릿에 포함된 각 정책에 대해 다음 두 가지 설정을 구성합니다.

* **허용/허용되지 않음:** 슬라이더를 원하는 값으로 설정합니다. [정책 세부 정보](https://helpx.adobe.com/kr/enterprise/global-admin-console/update-policies.html#policy-details)에 대해 알아보세요.
* **잠금 값:** 다음 옵션 중 하나를 사용하여 정책의 잠금 상태를 수정합니다.
   * **잠금** - 템플릿 적용 후 정책이 잠깁니다.
   * **잠금 해제** - 템플릿 적용 후 정책이 잠금 해제됩니다.
   * **그대로 유지** — 정책의 잠금 상태는 템플릿을 적용하기 전과 동일하게 유지됩니다.<br>
     ![Pic2](./assets/DXSKB-3209-2-policy-template.png)
<br>

## 조직에 템플릿 적용

1. [Global Admin Console](https://global-admin-console.adobe.com/)에서 편집할 조직을 선택한 다음 **[!UICONTROL 정책 템플릿]** 탭으로 이동합니다.
1. 관련 정책 템플릿에 대한 **[!UICONTROL 추가 옵션]** ![추가 옵션](./assets/manage-product-profiles_more-options.png) 아이콘을 선택하고 **[!UICONTROL 조직에 템플릿 적용]**&#x200B;을 선택합니다.<br>
   ![Pic3](./assets/DXSKB-3209-3-ga_15.png)
   <br>
1. 템플릿을 적용할 조직을 선택합니다. 여러 조직을 선택할 수 있습니다.<br>
   ![Pic4](./assets/DXSKB-3209-4-bulk-apply-template.png)
   <br>
1. **[!UICONTROL 템플릿 적용]**&#x200B;을 선택합니다.
1. 정책 템플릿이 적용되는 조직에서 보류 중인 변경 내용을 구현하려면 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택하십시오. 검토 후 **[!UICONTROL 변경 내용 제출]**&#x200B;을(를) 선택하여 [실행](https://helpx.adobe.com/kr/enterprise/global-admin-console/execute-jobs.html)합니다.

선택한 조직의 모든 정책 값이 템플릿의 값과 이미 일치하는 경우 변경 사항이 없음을 알리는 메시지가 나타납니다. 또한 보류 중인 다른 편집 내용이 없으면 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 사용할 수 없습니다.

## 템플릿 편집

1. [Global Admin Console](https://global-admin-console.adobe.com/)에서 편집할 조직을 선택한 다음 **[!UICONTROL 정책 템플릿]** 탭으로 이동합니다.
1. 관련 템플릿에 대해 **[!UICONTROL 추가 옵션]** 아이콘 ![추가 옵션](./assets/manage-product-profiles_more-options.png)을 선택하고 **[!UICONTROL 템플릿 편집]**&#x200B;을 선택합니다.<br>
   ![사진5](./assets/DXSKB-3209-5-ga_15-1.png)
   <br>
1. 정책 템플릿을 업데이트하고 **[!UICONTROL 지금 업데이트]**&#x200B;를 선택합니다.
1. 정책 템플릿이 적용되는 조직에서 보류 중인 변경 내용을 구현하려면 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택하십시오. 검토 후 **[!UICONTROL 변경 내용 제출]**&#x200B;을(를) 선택하여 [실행](https://helpx.adobe.com/kr/enterprise/global-admin-console/execute-jobs.html)합니다.

## 템플릿 삭제

1. [Global Admin Console](https://global-admin-console.adobe.com/)에서 편집할 조직을 선택한 다음 **[!UICONTROL 정책 템플릿]** 탭으로 이동합니다.
1. 관련 템플릿에 대한 **[!UICONTROL 추가 옵션]** ![추가 옵션](./assets/manage-product-profiles_more-options.png) 아이콘을 선택하고 **[!UICONTROL 템플릿 삭제]**&#x200B;를 선택합니다.<br>
   ![사진6](./assets/DXSKB-3209-6-ga_15-2.png)
   <br>
1. 표시되는 대화 상자에서 *예*&#x200B;를 선택합니다.
