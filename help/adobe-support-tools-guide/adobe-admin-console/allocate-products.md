---
title: Global Admin Console을 사용하여 하위 조직에 제품 할당
description: 글로벌 관리자가 리소스를 하위 조직에 분배하여 각 조직 내에서 효과적인 리소스 관리와 사용자 할당을 가능하게 하는 방법을 알아봅니다.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: de6e785d-8965-40d5-ac78-7fbb2cd7afc7
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Global Admin Console을 사용하여 하위 조직에 제품 할당

Enterprise에 적용됩니다.

글로벌 관리자가 리소스를 하위 조직에 분배하여 각 조직 내에서 효과적인 리소스 관리와 사용자 할당을 가능하게 하는 방법을 알아봅니다.

[Global Admin Console](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)에서 **[!UICONTROL 제품 할당]** 탭으로 이동한 다음 하위 조직에 할당할 제품을 선택하십시오.

[Global Admin Console](https://global-admin-console.adobe.com)에 로그인합니다.

>[!NOTE]
>
>**[!UICONTROL 제품 할당]**&#x200B;은(는) Enterprise Term License Agreement(ETLA) 계약에만 사용할 수 있습니다.

조직 간에 Adobe 제품을 배포 및 관리하는 과정의 일부로, 구매한 리소스를 관리할 조직 전체의 리소스 할당으로 분할하는 것입니다. 자원의 전체 또는 일부를 제공하여 제품 자원의 관리를 다른 조직에 분배할 수 있습니다. 모든 제품의 모든 리소스를 할당할 수 있는 것은 아닙니다. 일부 제품은 다른 조직에 분배할 수 없습니다. 이러한 제품은 **[!UICONTROL 제품 할당]** 탭에 표시되지만 다른 조직에 추가할 수 있는 컨트롤이 없습니다.

>[!WARNING]
>
>**만료됨**&#x200B;이거나 조직이 **비활성** 상태인 계약에서 하위 조직에 제품을 할당할 수 없습니다. [계약 만료](https://helpx.adobe.com/kr/enterprise/using/contract-expiry.html)에 대해 자세히 알아보거나, 회사 관리자에게 문의하여 하위 조직의 사용자가 Adobe 앱 및 서비스에 액세스할 수 없도록 방지하십시오.

## 풀링된 스토리지

이는 Admin Console에 스토리지 탭이 있는 고객에게 적용됩니다. 스토리지 탭이 표시되지 않으면 Admin Console이 엔터프라이즈 스토리지 모델로 아직 업데이트되지 않은 것입니다. 조직이 마이그레이션되면 다음과 같은 변경 사항이 표시됩니다.

- 전역 관리자는 계층 전체에서 저장소 할당량 및 사용에 액세스할 수 있으며 **[!UICONTROL Global Admin Console]**&#x200B;의 [제품 할당](https://adminconsole.adobe.com/) 탭을 사용하여 조직에 저장소를 할당할 수 있습니다.
- 시스템 관리자와 스토리지 관리자는 조직 전체에 걸쳐 스토리지를 완벽하게 제어하고 파악할 수 있습니다. **[!UICONTROL Adobe Admin Console]**&#x200B;의 [저장소](https://adminconsole.adobe.com/) 탭을 사용하여 저장소를 추적하고 관리할 수 있습니다.

Adobe Creative Cloud 스토리지에 대한 업데이트를 통해 최종 사용자는 조직에서 구매한 스토리지 용량까지 스토리지 할당량을 유연하게 선택할 수 있습니다. [자세히 알아보기](https://helpx.adobe.com/kr/enterprise/using/manage-adobe-storage.html).

## 제품 할당

Global Admin Console의 **[!UICONTROL 제품 할당]** 탭에는 조직 계층 전체에서 구입한 제품에 대한 할당 단위가 표시됩니다. [전역 관리자](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins)로서 이러한 제품 리소스를 조직 트리의 다른 조직에 할당하고 할당 수량을 지정할 수 있습니다. [전역 뷰어](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins)로서 데이터를 보고 내보낼 수 있지만 업데이트할 수는 없습니다.

조직에 제품을 할당하려면 다음 단계를 수행합니다.

1. [Global Admin Console](https://global-admin-console.adobe.com)에 로그인하고 **[!UICONTROL 제품 할당]**(으)로 이동합니다.
1. 드롭다운 목록에서 제품을 선택하여 제품이 다른 조직에 어떻게 할당되는지 확인합니다.\
   조직에 현재 제품이 없는 경우 **[!UICONTROL 추가 +]** 아이콘이 나타납니다.

   >[ !N참고]
   >
   >하위 조직이 이미 구매 계약을 가지고 있는 경우 상위 조직에서 해당 하위 조직으로의 제품 할당이 제한될 수 있습니다. [자세히 알아보기](https://helpx.adobe.com/kr/enterprise/global-admin-console/allocate-products.html#limited-product-allocation).

1. 제품을 할당하려면 관련 조직의 **[!UICONTROL 추가 +]** 아이콘을 선택하십시오.\
   일부 제품에는 할당 가능한 리소스가 두 개 이상 포함되어 있습니다. 이 경우 대화 상자에 여러 리소스가 나열되며 각 리소스에 대한 값을 제공해야 합니다. 예를 들어 Adobe Stock에는 Adobe Stock 이미지 크레딧과 프리미엄 크레딧이 포함될 수 있습니다.
   ![Adobe Stock 이미지](/help/adobe-support-tools-guide/assets/adobe-stock-images.png)
1. 표시되는 대화 상자에서 제품 수량을 지정합니다.
1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.
1. 리소스의 초과 할당을 허용하거나 허용하지 않으려면 관련 토글을 선택합니다.
   ![초과 할당](/help/adobe-support-tools-guide/assets/overallocation.png)
1. 리소스 할당을 완료한 후 **[!UICONTROL 보류 중인 변경 내용 검토]**&#x200B;를 선택합니다. 검토 후 **[!UICONTROL 변경 내용 제출]**&#x200B;을(를) 선택하여 [실행](https://helpx.adobe.com/kr/enterprise/global-admin-console/execute-jobs.html)합니다.

## Adobe Acrobat Sign 사용자 라이선스 또는 트랜잭션 할당 및 배포

Global Admin Console을 사용하면 조직 계층 전체에 Acrobat Sign 사용자 라이선스 또는 트랜잭션을 할당하고 배포할 수 있습니다. Acrobat Sign 라이선스 또는 트랜잭션이 할당된 계층의 각 조직은 고유한 개별 Acrobat Sign 계정을 만듭니다.

- 생성된 각 Acrobat Sign 계정은 관리 및 콘텐츠 측면에서 독립적이며 개별적으로 사용됩니다.
- 각 Acrobat Sign 계정은 다른 Acrobat Sign 계정(예: 상위 또는 자매 조직)을 인식하지 못합니다.

[Admin Console에서 Adobe Acrobat Sign 관리](https://helpx.adobe.com/kr/enterprise/using/adobe-sign-for-enterprise.html)에 대해 자세히 알아보세요.

KBA(기술 자료 인증) 및 PA(전화 인증)와 같은 인증 추가 기능을 관리하려면 Adobe 담당자 또는 고객 성공 관리자에게 문의하십시오.


## 제품 할당 제한 사항

이러한 경우 상위 조직에서 하위 조직으로의 할당은 제한됩니다.

- 두 조직에 서로 다른 계약이 있고 할당하려는 제품이 두 조직에 모두 있는 경우 계약 간에 동일한 오퍼를 혼합할 수 없습니다.
- 두 조직에 동일한 계약이 있는 경우 Adobe 담당자에게 연락하거나 Global Admin Console의 [제품 할당](https://helpx.adobe.com/kr/enterprise/using/support-for-enterprise.html)이 차단되도록 지정하는 **[!UICONTROL 지원 제출]** 사례를 통해 제품 할당 권한을 요청할 수 있습니다.

## 초과 할당

[전역 관리자](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins)로서 리소스의 초과 할당을 허용할 수 있습니다.

제품 및 조직과 연결된 할당 [정책](https://helpx.adobe.com/kr/enterprise/global-admin-console/update-policies.html#update-policies)은(는) 초과 할당이 허용되는지 여부를 나타냅니다.

초과 할당을 사용하면 상위 조직에서 사용할 수 있는 것보다 더 많은 제품 리소스를 하위 조직에 부여할 수 있습니다. 이 방법은 할당이 대략적인 경우 유용하며 관리자가 리소스 할당을 계속 합산하는 데 부담을 느끼지 않으려는 경우에 유용합니다.
조직의 제품 자원에 대해 초과 할당이 비활성화된 경우 하위 부여의 합계는 상위 부여를 초과할 수 없습니다. 초과 할당이 비활성화된 것으로 표시된 리소스에 대한 초과 할당 요청이 실행되지 않습니다.
자원의 부여 수량에 초과 할당 상황이 존재하는 경우 초과 할당 토글이 사용가능에서 사용불능으로 전환되면 부여 갱신을 실행하기 전에 초과 할당을 제거하기 위해 부여 값을 조정해야 합니다.

![초과 할당](/help/adobe-support-tools-guide/assets/overallocation.png)

## 계층에서 만료된 계약

만료된 ETLA 계약에서는 하위 조직에 제품을 할당할 수 없습니다. **[!UICONTROL 개요]** 및 **[!UICONTROL 제품 할당]** 페이지에서 다음과 같은 인앱 배너 및 알림은 하나 이상의 하위 조직에 대한 계약이 만료되거나, 만료되었거나, 비활성 상태인 시기를 명확하게 나타냅니다.

![제품 할당](/help/adobe-support-tools-guide/assets/product-allocation.png)

>[ !I중요]
>
>계층 구조의 일부인 ETLA 계약이 비활성화되면 **[!UICONTROL 개요]** 및 **[!UICONTROL 제품 할당]** 페이지에서 제품이 제거됩니다.

[계약 만료에 대해 자세히 알아보거나](https://helpx.adobe.com/kr/enterprise/using/contract-expiry.html) 회사 관리자에게 문의하여 하위 조직의 사용자가 Adobe 앱 및 서비스에 액세스할 수 없도록 방지하십시오.
