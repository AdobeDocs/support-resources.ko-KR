---
title: 관리자 관리
description: Adobe 고객이 Global Admin Console에서 관리자를 설정하고 관리하여 사용자 액세스, 제품 라이선스 및 조직 리소스를 제어하는 방법.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 41c00379-98ee-4922-8eba-cc373c23a019
source-git-commit: 8860538190e99e171abc6273adda321443e41fed
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 2%

---

# 관리자 관리

*Enterprise에 적용됩니다.*

글로벌 관리자 기능을 탐색하고 각 개별 조직의 관리자에게 사용자, 제품 라이선스 및 그룹 관리를 위임하고 배포하는 방법을 알아봅니다.

Global Admin Console에서 조직을 선택하고 **[!UICONTROL 관리자]** 탭으로 이동하여 관리자 권한을 추가, 편집 또는 제거할 수 있습니다. 자세한 내용은 [전역 관리 채택](https://helpx.adobe.com/kr/enterprise/global-admin-console/adopt-global-administration.html)을 참조하세요. 로그인하려면 [Global Admin Console](https://global-admin-console.adobe.com/)&#x200B;(으)로 이동하세요.


Global Admin Console에서는 전역 관리자라는 역할을 도입했습니다. 이 역할은 시스템 관리자와는 다르며 다음을 수행할 수 있습니다.

- Global Admin Console 계층에 추가된 모든 Admin Console에서 총 Adobe 투자의 전역 환경을 봅니다.
- 여러 Admin Console에서 Adobe 라이선스 및 리소스 할당 및 사용을 모니터링합니다.
- Admin Console 또는 조직을 만듭니다.
- 루트 또는 상위 Admin Console에서 계층 구조 내 아래에 있는 하위 Admin Console에 제품 라이선스를 할당합니다.
- 시스템 관리자가 고유한 Admin Console을 계속 관리하는 동안 일상적인 작업을 유지합니다. 예를 들어 글로벌 관리자는 하위 Admin Console에 제품을 할당할 수 있지만 사용자에게 할당할 수 없습니다. 시스템 관리자는 Admin Console 내의 시트를 받고 해당 사용자에게 제품을 할당합니다.
- 필요한 경우 계층의 모든 Admin Console에 조직 정책을 적용합니다.

## 기본 관리 작업

Global Admin Console은 여러 조직과 Admin Console에서 작동하도록 디자인되었습니다. 다음 표에서는 Admin Console 또는 Global Admin Console과 같은 다양한 기능과 이러한 기능을 완료할 수 있는 위치를 간략하게 설명합니다.

<table>
  <tr>
    <th colspan="2">작업</th>
    <th>Global Admin Console</th>
    <th>Admin Console</th>
  </tr>

<tr>
    <td colspan="2">하위 조직 생성, 재상위 및 삭제</td>
    <td align="center">예</td>
    <td align="center">아니요</td>
  </tr>

<tr>
    <td colspan="2">여러 조직과 작업</td>
    <td align="center">예</td>
    <td align="center">아니요</td>
  </tr>

<tr>
    <td rowspan="2" valign="middle">관리자 관리</td>
    <td>하나 이상의 조직용</td>
    <td align="center">예</td>
    <td align="center">아니요</td>
  </tr>

<tr>
    <td>하나의 조직용</td>
    <td align="center">예</td>
    <td align="center">예</td>
  </tr>

<tr>
    <td colspan="2">제품 프로필 및 사용자 그룹 관리</td>
    <td align="center">예</td>
    <td align="center">예</td>
  </tr>

<tr>
    <td colspan="2">정책 정의 및 관리</td>
    <td align="center">예</td>
    <td align="center">아니요</td>
  </tr>

<tr>
    <td colspan="2">조직 전체에 제품 할당</td>
    <td align="center">예</td>
    <td align="center">아니요</td>
  </tr>

<tr>
    <td colspan="2">사용자에게 제품 할당</td>
    <td align="center">아니요</td>
    <td align="center">예</td>
  </tr>

<tr>
    <td colspan="2">사용자 관리</td>
    <td align="center">아니요</td>
    <td align="center">예</td>
  </tr>

<tr>
    <td colspan="2">패키지 관리</td>
    <td align="center">아니요</td>
    <td align="center">예</td>
  </tr>

<tr>
    <td colspan="2">도메인 및 디렉터리 설정</td>
    <td align="center">아니요</td>
    <td align="center">예</td>
  </tr>

<tr>
    <td colspan="2">엔터프라이즈 스토리지 및 암호화 관리</td>
    <td align="center">아니요</td>
    <td align="center">예</td>
  </tr>
</table>

## 관리자 관리

Adobe 제품 액세스 및 사용을 세분화하고 관리할 수 있는 유연한 관리 계층을 만들 수 있습니다. Adobe Admin Console과 마찬가지로 Global Admin Console을 사용하면 시스템 관리자, 제품 관리자, 제품 프로필 관리자, 사용자 그룹 관리자, 배포 관리자, 지원 관리자 및 저장소 관리자를 추가할 수 있습니다. 이러한 관리자는 자신이 관리하는 조직에서 각자의 관리 작업을 수행할 수 있습니다. 이러한 역할 외에도 전역 관리에는 전역 관리자와 전역 뷰어라는 두 가지 새로운 역할이 있습니다.

전역 관리자는 전이적 역할입니다. 사용자를 조직의 전역 관리자로 지정하면 해당 사용자가 직접 또는 간접적으로 해당 조직의 모든 하위 항목에 대한 전역 관리자가 됩니다. 또한, 조직 계층에서 새 조직이 만들어지는 경우, 해당 조직의 상위 조직의 모든 전역 관리자는 즉시 새로 만들어진 조직의 전역 관리자가 됩니다.

다음은 글로벌 관리자 역할의 기능입니다.

- 하위 조직 생성 및 삭제
- 정책 설정 및 편집
- 관리자 역할 설정 및 수정
- 하위 조직의 제품 추가 및 제거
- 하위 조직에 대한 리소스 할당 설정 또는 변경
- 제품 프로필 및 사용자 그룹 관리

다음은 전역 뷰어 역할의 기능입니다.

- 조직 및 하위 조직의 사용자 그룹, 제품, 제품 프로필, 관리자, 정책 세트 및 리소스 목록을 봅니다.

## 분산 관리

글로벌 관리자는 관리자를 관리함으로써 사용자, 제품 라이선스 및 그룹 관리를 각 개별 조직의 관리자에게 위임하고 배포할 수 있습니다. 글로벌 관리자가 조직에 추가한 관리자에게는 다른 조직의 관리에 대한 가시성을 확보하지 않고도 조직을 관리할 수 있는 유연성이 제공됩니다. 따라서 전역 관리자는 리소스 및 사용자에 대한 데이터를 격리한 상태로 유지하는 리소스 및 사용자 관리를 위임할 수 있습니다.

글로벌 관리자는 조직을 만들고, 제품 및 저장소와 같은 리소스를 해당 조직에 배포하고, ID 설정을 관리하고, 조직 정책 템플릿을 만들고 적용할 수 있습니다. 글로벌 관리자가 조직에 추가한 시스템 관리자는 사용자에게 제품을 할당하고 사용자를 온보딩하며 제품 프로필을 만들고 관리하며 해당 조직 내에서 다른 관리 작업을 수행할 수 있습니다.

## 관리자 추가

1. [Global Admin Console](https://global-admin-console.adobe.com/)에서 편집할 조직을 선택한 다음 **[!UICONTROL 관리자]** 탭으로 이동합니다.

1. **[!UICONTROL 관리자 추가]**&#x200B;를 선택합니다.

   ![Global Admin Console 관리자 추가](../assets/global-admin-console-add-admin.png)

1. **[!UICONTROL 관리자 추가]** 대화 상자에서 **[!UICONTROL 사용자 세부 정보]**(전자 메일, 이름, 성, 계정 유형 및 국가 코드)를 입력합니다.

   기존 사용자를 관리자로 추가하려면 기존 사용자와 동일한 계정 유형을 선택하십시오. 그렇지 않으면 추가 작업이 실패합니다.

   >[!NOTE]
   >
   > 조직은 계정 유형을 추가할 수 있는 제한을 가질 수 있습니다. [정책](https://helpx.adobe.com/kr/enterprise/global-admin-console/update-policies.html) 또는 조직의 다른 구성 매개 변수를 기반으로 할 수 있습니다. 조직에서 AdobeID 사용자와 BusinessID 사용자를 동시에 추가하는 것을 허용하지 않습니다. 일반적으로 조직에 두 가지 유형의 사용자가 모두 없어야 하지만 규칙이 설정되는 순서에 따라 특정 계정 유형의 사용자가 정책이나 규칙의 적용을 미리 예약할 수 있습니다.

1. **[!UICONTROL 관리자 권한]** 섹션에서 관리자 역할을 하나 이상 선택하십시오.

   제품 관리자, 제품 프로필 관리자 및 사용자 그룹 관리자 등의 역할에 대해 각각 특정 제품, 프로필 및 그룹을 선택합니다.

   ![Global Admin Console 관리자 추가](../assets/global-admin-console-add-admin-detail.png)

1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.

1. 조직을 편집한 후 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택한 다음 **[!UICONTROL 변경 내용 제출]**&#x200B;을 선택하여 [변경 내용을 실행](https://helpx.adobe.com/kr/enterprise/global-admin-console/execute-jobs.html)합니다.

관리자 역할이 추가되면 사용자는 역할 변경을 알리는 이메일 알림을 받습니다.

관리자가 추가되면 자신의 역할을 수락하고 Admin Console에 대한 링크를 제공할 수 있도록 초대하는 이메일 메시지를 받게 됩니다. 전역 관리자와 일부 다른 역할로 추가된 경우 두 개의 초대를 받게 되며 그중 한 개는 Global Admin Console에, 한 개는 Admin Console에 초대됩니다.

## 관리자 편집

1. 편집할 조직을 선택하고 **[!UICONTROL 관리자]** 탭으로 이동합니다.

1. 관련 관리자에 대한 **[!UICONTROL 추가 옵션]**(⋮) 아이콘을 선택한 다음 **[!UICONTROL 관리자 편집]**&#x200B;을 선택합니다.

   ![Global Admin Console 관리 권한 편집](../assets/global-admin-console-edit-admin-right.png)

1. 관리자 세부 정보를 업데이트한 다음 **[!UICONTROL 저장]**&#x200B;을 선택합니다.

1. 조직을 편집한 후 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택합니다.

추가 또는 제거된 각 관리자 역할에 대해 보류 중인 변경 목록에 별도의 명령이 표시됩니다. 검토 후 **[!UICONTROL 변경 내용 제출]**&#x200B;을(를) 선택하여 [실행](https://helpx.adobe.com/kr/enterprise/global-admin-console/execute-jobs.html)합니다.

## 관리자 권한 제거

1. 편집할 조직을 선택하고 **[!UICONTROL 관리자]** 탭으로 이동합니다.

1. 관련 관리자에 대한 **[!UICONTROL 추가 옵션]**(⋮) 아이콘을 선택한 다음 **[!UICONTROL 관리자 권한 제거]**&#x200B;를 선택합니다.

   ![Global Admin Console 관리자 권한 제거](../assets/global-admin-console-remove-admin-right.png)

1. 확인 대화 상자에서 **[!UICONTROL 확인]**&#x200B;을 선택합니다.

1. 조직을 편집한 후 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택합니다. 검토 후 **[!UICONTROL 변경 내용 제출]**&#x200B;을(를) 선택하여 [실행](https://helpx.adobe.com/kr/enterprise/global-admin-console/execute-jobs.html)합니다.

관리자를 삭제하면 사용자는 해당 조직의 Admin Console에 대한 액세스 권한이 없음을 알리는 이메일 알림을 받게 됩니다.
