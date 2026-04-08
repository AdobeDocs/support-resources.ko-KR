---
title: Global Admin Console에서 사용자 그룹 관리
description: Global Admin Console에서 사용자 그룹을 생성, 공유, 편집 및 삭제하여 조직 전체의 사용자 관리를 간소화하는 방법에 대해 알아봅니다.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 1e20362a-0974-4b83-a083-9edaab04c255
source-git-commit: ad324036dbeb2a54855349321b2ba33405d2c075
workflow-type: tm+mt
source-wordcount: '1333'
ht-degree: 0%

---

# Global Admin Console에서 사용자 그룹 관리

Global Admin Console에서 사용자 그룹을 만들고, 관리하고, 공유하여 동일한 권한을 가진 사용자를 그룹화하고, 시간을 절약하고, 일관성을 보장함으로써 사용자 관리를 간소화합니다.

[Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)에서 조직을 선택하고 **[!UICONTROL 사용자 그룹]**(으)로 이동합니다. 단일 사용자 관리 소스를 사용하여 여러 조직에서 그룹을 공유하여 사용자와 그룹을 동기화합니다. [Global Admin Console에 로그인](https://global-admin-console.adobe.com)하려면 여기로 이동하세요.



## 사용자 그룹 만들기

[사용자 그룹을 개별적으로, 또는 대량으로 ](https://helpx.adobe.com/kr/enterprise/using/user-groups.html)만들거나 [기존 Azure AD에서 ](https://helpx.adobe.com/enterprise/using/add-azure-sync.html)의 사용자 그룹을 Adobe Admin Console의 페더레이션 디렉터리에 직접 동기화할 수 있습니다. Global Admin Console에서는 관련 제품 프로필이 할당된 사용자 그룹을 정의할 수 있습니다. 이 경우 사용자 그룹 관리자는 나중에 Admin Console을 사용하여 사용자를 추가할 수 있습니다.

1. [Global Admin Console](https://global-admin-console.adobe.com/)에 로그인하고 편집할 조직을 선택한 다음 **[!UICONTROL 사용자 그룹]** 탭으로 이동합니다.

2. **[!UICONTROL 사용자 그룹 추가]**&#x200B;를 선택합니다.

   사용자 그룹 탭이 선택된 Global Admin Console의 ![조직 탭](assets/add-user-group.png "사용자 그룹 추가")

   _조직에 사용자 그룹을 추가하여 사용자 관리를 간소화합니다._

3. 표시되는 **[!UICONTROL 사용자 그룹 추가]** 대화 상자에 다음을 입력하십시오.
   - **[!UICONTROL 이름]**: 사용자 그룹의 이름을 지정하십시오.
   - **[!UICONTROL 제품 프로필]**: 사용자 그룹의 현재 또는 향후 구성원에게 제품 액세스 권한을 부여하려면 드롭다운 화살표를 클릭하여 목록에서 제품 프로필을 선택하거나 제품 프로필 이름을 입력하고 표시되는 드롭다운 목록에서 선택합니다. 아직 만들지 않은 제품 프로필을 추가하려면 먼저 [제품 프로필](https://helpx.adobe.com/enterprise/using/global-admin-edit-organizations.html#profiles) 탭을 사용하여 추가해야 합니다.
   - **[!UICONTROL 관리자]**: 드롭다운 화살표를 클릭하여 목록에서 관리자를 선택하거나, 관리자의 전자 메일 주소를 입력하고 표시되는 드롭다운 목록에서 선택합니다. 아직 만들지 않은 새 관리자를 추가하려면 먼저 [관리자](#share-user-groups) 탭을 사용하여 해당 관리자를 만들어야 합니다.

   지정한 제품 프로필은 사용자 그룹에 할당되며, 지정한 관리자는 해당 그룹의 사용자 그룹 관리자가 됩니다. 사용자 그룹 관리자는 관련 조직의 Adobe Admin Console을 사용하여 그룹을 관리할 수 있습니다.

4. **[!UICONTROL 저장]**&#x200B;을 선택합니다.

5. 업데이트를 검토하려면 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택하십시오. **[!UICONTROL 변경 내용 제출]**&#x200B;을 선택하여 [실행](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/execute-jobs)합니다.

   >[!NOTE]
   >
   >전역 관리자는 Global Admin Console을 사용하여 [제품 프로필 및 사용자 그룹 관리자를 사용자 그룹에 할당](#review-user-groups)할 수 있습니다. Adobe Admin Console을 사용하여 시스템 관리자 및 사용자 그룹 관리자는 [사용자를 추가하고 관리자 및 제품 프로필을 할당](https://helpx.adobe.com/kr/enterprise/using/user-groups.html)할 수 있습니다.



## 사용자 그룹 공유

그룹 프로젝션을 사용하면 사용자 그룹 및 연결된 사용자를 단일 관리 소스의 여러 Admin Console에 동기화할 수 있습니다. 글로벌 관리자는 사용자 그룹을 위쪽이나 옆이 아니라 아래쪽으로 작업하면서 소스 조직의 계층적 하위 멤버와 공유할 수 있습니다.

1. [Global Admin Console](https://global-admin-console.adobe.com/)에 로그인하고 조직을 선택한 다음 **[!UICONTROL 사용자 그룹]** 탭으로 이동합니다.

2. 공유할 사용자 그룹의 확인란을 선택합니다.

   다음의 경우 그룹이 공유에 비활성화될 수 있습니다.
   - 사용자 그룹은 다른 조직에서 공유됩니다. 그룹을 공유하거나 편집하려면 조직 계층에서 그룹을 소유한 조직을 선택합니다.
   - 조직에서 전 세계적으로 단계적으로 출시되고 있는 [비즈니스용 Adobe 저장소](https://helpx.adobe.com/in/enterprise/using/storage-for-business.html)를 사용하지 않습니다.
   - 조직 정책을 사용할 수 없습니다. **[!UICONTROL 정책]** 탭으로 이동하여 **[!UICONTROL 공유 사용자 그룹 관리]** 정책을 켭니다.
   - 조직에 사용자 그룹을 공유할 하위 조직이 없습니다.

3. **[!UICONTROL 사용자 그룹 공유]**&#x200B;를 선택합니다.

4. <a id="review-user-groups"></a>다른 조직과 공유할 사용자 그룹을 검토합니다. 선택한 조직의 시스템 관리자인 경우에도 **[!UICONTROL Admin Console에서 열기]**&#x200B;를 선택하십시오. <img src="assets/icon-open-in-admin-console.png" alt="Admin Console에서 열기 아이콘" width="14" height="14"> 아이콘을 클릭하여 Adobe Admin Console에서 사용자 그룹 구성원 목록을 검토합니다.

   >[!NOTE]
   >
   >충돌을 방지하려면 사용자 그룹을 공유하려는 조직에 이름이 같은 그룹이 없는지 확인합니다.

5. **[!UICONTROL 다음]**&#x200B;을 선택합니다.

6. 사용자 그룹을 공유할 조직을 선택하고 **[!UICONTROL 다음]**&#x200B;을(를) 선택합니다.

7. 충돌이 없으면 **[!UICONTROL 사용자 그룹 공유]**&#x200B;를 선택하십시오.

   충돌이 있는 경우(대상 조직에 같은 이름의 사용자 그룹이 있는 경우) 다음 옵션 중 하나를 선택한 다음 **[!UICONTROL 사용자 그룹 공유]**&#x200B;를 선택하십시오.
   - **[!UICONTROL 무시(기본값)]**: 이름이 같은 대상 조직의 그룹을 건너뜁니다.
   - **[!UICONTROL 항목만 추가]**: 사용자를 제거하지 않고 기존 사용자 그룹에 새 사용자를 추가하여 사용자 그룹을 병합합니다.
   - **[!UICONTROL 미러 그룹]**: 사용자를 추가하거나 제거하여 공유 그룹과 일치하도록 대상 조직의 그룹을 조정하십시오.

8. 업데이트를 검토하려면 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택하십시오. **[!UICONTROL 변경 내용 제출]**&#x200B;을 선택하여 [실행](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/execute-jobs)합니다.

   그룹 프로젝션 이벤트는 참조를 위해 기록됩니다. [감사 로그를 보고 다운로드](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/download-audit-logs-and-export-reports)하는 방법을 배웁니다.


사용자 그룹을 공유하면 그룹과 해당 사용자가 대상 조직에 추가됩니다. 그러나 *소스 사용자 그룹 컨트롤*&#x200B;은 공유 사용자 그룹과 해당 사용자를 제어합니다. 관리자 및 제품 프로필 할당이 조직 간에 동기화되지 *않음*&#x200B;되었습니다.

소스 사용자 그룹의 예상 사용자 그룹 이름 또는 연관된 사용자 변경 사항은 대상 조직에서 자동으로 업데이트됩니다. 공유 사용자 그룹을 직접 관리할 수는 없지만 대상 조직 내의 관리자는 제품 프로필을 공유 그룹에 할당하여 그룹 사용자에게 라이선스 액세스 권한을 부여할 수 있습니다.



## 공유 그룹에 대한 액세스 취소

1. [Global Admin Console](https://global-admin-console.adobe.com/)에 로그인하고 조직을 선택한 다음 **[!UICONTROL 사용자 그룹]** 탭으로 이동합니다.

2. 관련 사용자 그룹에 대해 **[!UICONTROL 공유 액세스 관리]**&#x200B;를 선택합니다.

3. 액세스 권한을 취소할 조직을 선택합니다.

4. **[!UICONTROL 액세스 취소]**&#x200B;를 선택합니다.

5. 액세스를 취소하는 동안 사용자 그룹 및 사용자를 삭제하거나 대상 조직에 복사본을 남길 수 있습니다.
   - 삭제하면 대상 조직에서 사용자 그룹이 제거됩니다. 다른 공유 그룹의 구성원이 아닌 사용자는 대상 조직에서 제거되며 모든 제품, 서비스 및 자산에 대한 액세스 권한을 잃게 됩니다.
   - 복사본을 떠나면 사용자 그룹과 사용자는 모든 할당이 그대로 유지되는 대상 조직에 유지됩니다. 하지만 사용자 그룹은 더 이상 동기화되지 않으며 대상 조직의 관리자가 관리할 수 있습니다.

6. **[!UICONTROL 액세스 취소]**&#x200B;를 선택합니다.

7. 업데이트를 검토하려면 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택하십시오. **[!UICONTROL 변경 내용 제출]**&#x200B;을 선택하여 [실행](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/execute-jobs)합니다.



## 사용자 그룹 편집

1. [Global Admin Console](https://global-admin-console.adobe.com/)에 로그인하고 조직을 선택한 다음 **[!UICONTROL 사용자 그룹]** 탭으로 이동합니다.

2. **[!UICONTROL 추가 옵션 선택]** 관련 사용자 그룹에 대해 <img src="assets/icon-more-options.png" alt="기타 옵션 아이콘" width="14" height="14" style="vertical-align:middle"> 아이콘을 클릭하고 **[!UICONTROL 사용자 그룹 편집]**&#x200B;을 선택합니다.

   >[!NOTE]
   >
   >선택한 조직이 소유하지 않은 사용자 그룹은 편집할 수 없습니다.

   ![사용자 그룹 탭에서 [사용자 그룹 편집] 옵션이 강조 표시된 조직이 선택되었습니다.](assets/edit-user-group.png "사용자 그룹 편집")

   _사용자 그룹을 편집하여 사용자 그룹 이름, 제품 프로필 또는 관리자를 업데이트합니다._

3. 사용자 그룹 이름, 제품 프로필 또는 관리자를 업데이트합니다. 그런 다음 **[!UICONTROL 저장]**&#x200B;을 선택합니다.

   >[!NOTE]
   >
   >**[!UICONTROL 사용자 그룹 편집]** 마법사에서 이미 이 조직에 할당된 관리자 역할이 있는 사용자에게만 관리자 역할을 할당할 수 있습니다. [새 관리자를 추가](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)하는 방법을 알아봅니다.

4. 업데이트를 검토하려면 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택하십시오. **[!UICONTROL 변경 내용 제출]**&#x200B;을 선택하여 [실행](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/execute-jobs)합니다.

   >[!NOTE]
   >
   >공유 사용자 그룹의 이름을 변경하면 변경 사항이 대상 조직에서 자동으로 업데이트됩니다.



## 사용자 그룹 삭제

1. [Global Admin Console](https://global-admin-console.adobe.com/)에 로그인하고 조직을 선택한 다음 **[!UICONTROL 사용자 그룹]** 탭으로 이동합니다.

2. **[!UICONTROL 추가 옵션 선택]** 관련 사용자 그룹에 대해 <img src="assets/icon-more-options.png" alt="기타 옵션 아이콘" width="14" height="14" style="vertical-align:middle"> 아이콘을 클릭하고 **[!UICONTROL 사용자 그룹 삭제]**&#x200B;를 선택합니다.

   >[!NOTE]
   >
   >선택한 조직이 소유하지 않은 사용자 그룹은 삭제할 수 없습니다.

3. 표시되는 대화 상자에서 **[!UICONTROL 확인]**&#x200B;을 선택합니다.

   >[!CAUTION]
   >
   >사용자 그룹을 삭제하면 사용자에게 영향을 줄 수 있습니다. 사용자 그룹이 삭제될 때 손실될 액세스 권한 또는 정보가 없는지 확인합니다.

4. 조직을 편집한 후 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택하여 검토하십시오. **[!UICONTROL 변경 내용 제출]**&#x200B;을 선택하여 [실행](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/execute-jobs)합니다.
