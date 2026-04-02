---
title: Global Admin Console에서 조직 선택
description: Global Admin Console 내에서 편집할 조직을 선택하는 방법에 대해 알아봅니다.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: 6a94922a-3343-433d-96e7-0af0f26581a1
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 1%

---

# Global Admin Console에서 조직 선택

Global Admin Console 내에서 편집할 조직을 선택하는 방법에 대해 알아봅니다.

>[!NOTE]
>
>[Global Admin Console](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console)에 대한 액세스 권한이 있으면 먼저 조직의 이름, 사용자 그룹, 제품 프로필, 관리자 및 조직 정책을 보고 관리할 조직을 선택할 수 있습니다. Global Admin Console에 로그인하려면 [여기를 클릭하세요](https://global-admin-console.adobe.com/).

Global Admin Console은 Adobe 리소스에 대한 조직의 중앙 관리 허브 역할을 합니다. 전역 관리자는 다음과 같은 작업을 수행할 수 있습니다.

- 조직 아래에 하위 조직 만들기
- 이들을 관리할 시스템 관리자 할당
- 하위 조직에 자원을 분배하여 해당 조직의 사용자에게 관리 및 지정합니다.

>[!NOTE]
>
> 조직의 사용자와 관리자는 조직 외부의 사용자, 스토리지 또는 기타 자원을 볼 수 없습니다.

## 조직 선택

**[!UICONTROL 조직 선택기]** 드롭다운 목록에 나열된 조직은 명시적으로 전역 관리자인 조직입니다. 즉, 전역 관리자 또는 전역 뷰어 역할을 가진 해당 조직의 관리자 목록에 추가되었습니다. 암시적으로 계층 구조의 해당 지점 아래에 있는 모든 조직의 전역 관리자(또는 전역 뷰어)이지만 해당 조직은 [!UICONTROL 조직 선택기]에 나열되지 않습니다.

![조직 선택기](/help/adobe-support-tools-guide/assets/org-picker.png)

이들을 나열하려면 나열할 조직에 자신을 글로벌 관리자로 추가합니다. [!UICONTROL 조직 선택기]에서 조직을 선택하면 관리 권한은 선택한 조직의 전역 관리자를 기준으로 합니다. 또한 트리에서 상위 조직의 전역 관리자로 나열되어 더 많은 권한을 제공할 수 있습니다. 추가 권한을 얻으려면 해당 상위 수준 조직을 선택해야 합니다.

Global Admin Console에서는 [!UICONTROL 계층 구조 트리]에서 조직을 선택한 후 특정 조직에 대한 정보 편집을 시작할 수 있습니다.

**편집 내용은 다음 항목에 영향을 줄 수 있습니다.**

- 조직 이름
- 사용자 그룹
- 제품 프로필
- 관리자
- 조직 정책

**편집 내용은 영향을 줄 수 없습니다.**

- 사용자(그룹 또는 제품 프로필 삭제 제외)
- 사용자 추가(관리자 제외)

계층 트리에서 조직을 선택하면 다음 정보가 표시됩니다.

- 조직 이름
- 지역
- 사용자 수
- 제품 목록
- 제품 프로필
- 사용자 그룹
- 관리자
- 요청된 도메인
- 조직의 정책 값

제품, 사용자 그룹, 관리자, 도메인, 정책 또는 정책 템플릿을 보거나 편집하려면 해당 탭을 선택합니다. 대부분의 경우 [!UICONTROL 검색] 필드를 사용하여 탭에서 특정 항목을 찾을 수 있습니다.

![조직 편집](/help/adobe-support-tools-guide/assets/edit-an-organization.png)

조직에 추가되거나 조직에서 제거된 모든 관리자는 이메일 알림을 받습니다. 조직에 대한 특정 정책을 변경하면 해당 조직의 [!DNL Admin Console]에 알림이 표시됩니다.

## 제한 및 필수 조건에 대해 알아보기

- 조직 중첩의 최대 깊이는 5입니다. 따라서 a/b/c/d/e는 허용되지만 a/b/c/d/e/f는 오류입니다. 예를 들어, Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London이 허용되지만, Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London/ Acme Mayfair 은 오류입니다.

- 최대 경로 이름 길이(모든 조직 포함)는 255자(&quot;/&quot; 포함)입니다. 단일 조직 이름의 최대 길이는 4~100자입니다.

- 조직 경로 이름은 고유하지만 단순 이름은 형제간에서만 고유합니다. 조직 계층 구조의 다른 곳에 동일한 단순 이름을 가진 조직이 있을 수 있습니다.

- 글로벌 Admin Console을 사용하여 선택한 조직에 연결된 도메인 목록만 볼 수 있습니다. 선택한 조직의 시스템 관리자인 경우 **[!UICONTROL Admin Console에서 열기]**&#x200B;를 선택하여 [도메인 관리](https://helpx.adobe.com/kr/enterprise/using/manage-domains-directories.html)를 수행합니다. 도메인 탭에 표시되는 정보를 이해하려면 [스키마 내보내기 및 가져오기](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/export-or-import-organization-structure-and-product-allocations#export-and-import-schemas)를 참조하십시오.

- IE 11은 전역 관리 액세스에 지원되지 않습니다. 다른 브라우저 또는 최신 버전의 IE 브라우저를 사용합니다.
