---
title: Adobe 고객 지원 권한 구성
description: Adobe 고객이 Admin Console에서 지원 권한을 설정 및 관리하여 사용자가 지원 리소스에 액세스하고, 문제를 제출하고, 사례 활동을 관리할 수 있는 방법입니다.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 7f7a394874014fb5333ed9fb39f84b7137562726
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---


# Adobe 고객 지원 권한 구성

조직에 대한 지원 권한을 구성하려면 먼저 Admin Console을 통해 사용자를 추가하거나 초대합니다.

## 조직에 지원 권한 역할 추가

**[!UICONTROL 지원 관리자]** 역할은 지원 관련 정보에 대한 액세스 권한이 있는 비관리 역할입니다. **[!UICONTROL 지원 관리자]**&#x200B;가 문제 보고서를 보고 만들고 관리할 수 있습니다.

관리자를 추가하거나 초대하려면:

1. Admin Console에서 **[!UICONTROL 사용자]** > **[!UICONTROL 관리자]**&#x200B;를 선택합니다.
1. **[!UICONTROL 관리자 추가]**&#x200B;를 클릭합니다.
1. 이름 또는 이메일 주소를 입력합니다.

   유효한 이메일 주소를 지정하고 화면의 정보를 채워 기존 사용자를 검색하거나 새 사용자를 추가할 수 있습니다.

   ![관리자 추가](assets/admin-console-add-admin.png)

1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다. 관리자 역할 목록이 나타납니다.

사용자에게 **[!UICONTROL 지원 관리자]** 역할을 할당하려면(사용자가 지원 팀에 문의할 수 있도록 설정):

1. **[!UICONTROL 관리자 지원]** 옵션을 선택하십시오.

   ![관리자 권한 편집](assets/edit-admin-rights.png)

1. 다음 두 옵션 중 하나를 선택합니다.

   * 옵션 1: **[!UICONTROL 기본 지원 관리자]**. 사용자에게 모든 솔루션(Marketo Engage 제외)에 대한 액세스 권한을 부여하려면 이 옵션을 선택합니다.
   * 옵션 2: **[!UICONTROL 제품 지원 관리자]**: Marketo Engage 지원을 위해 이 옵션을 선택하십시오. 사용자에게 액세스 권한을 부여할 Marketo Engage 인스턴스를 선택합니다.

   ![관리자 권한 편집 Marketo](assets/edit-admin-rights-advanced.png)

1. 선택한 후에는 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

사용자가 `message@adobe.com`에서 새 관리 권한과 관련된 전자 메일 초대를 받습니다.

조직에 가입하려면 전자 메일에서 **[!UICONTROL 시작하기]**&#x200B;를 클릭해야 합니다. 새 관리자가 전자 메일 초대의 **[!UICONTROL 시작]** 링크를 사용하지 않으면 Admin Console에 로그인할 수 없습니다.

로그인 프로세스의 일부로 아직 Adobe 프로필이 없는 경우 사용자에게 프로필을 설정하라는 메시지가 표시될 수 있습니다. 전자 메일 주소와 연결된 프로필이 여러 개인 경우 **[!UICONTROL 팀에 참여]**&#x200B;를 선택한 다음(메시지가 표시되면) 새 조직과 연결된 프로필을 선택해야 합니다.

![관리자 권한 확인](assets/admin-rights-confirmation.png)

자세한 내용은 관리 역할 설명서의 [Enterprise 관리자 역할 편집](admin-roles.md#edit-enterprise-admin-role) 지침을 참조하십시오. 조직의 시스템 관리자만 이 역할을 할당할 수 있습니다. 관리 계층에 대한 자세한 내용은 [관리 역할](admin-roles.md) 설명서를 참조하십시오.
