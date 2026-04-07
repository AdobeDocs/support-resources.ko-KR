---
title: 기존 사용자를 Adobe Admin Console으로 마이그레이션
description: Adobe 구독 라이선스를 사용하고 Admin Console의 기존 사용자를 다른 구매 프로그램 또는 라이선스 유형으로 마이그레이션해야 하는 조직에 대한 지침입니다.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: aace5ed8-65a6-4cff-8542-bc50e9c765b7
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# 기존 사용자를 Adobe Admin Console으로 마이그레이션

엔터프라이즈 및 팀에 적용됩니다.

이 문서는 다른 구매 프로그램 또는 라이선스 유형으로 마이그레이션하는 ETLA(Enterprise Term License Agreement) 또는 VIP(Value Incentive Plan) 구독을 통해 기존 Creative Cloud, Document Cloud 및 Acrobat 라이선스를 보유하고 있는 조직을 위한 것입니다.

>[!NOTE]
>
>북미 지역에 있고 계정 관리자의 연간 Adobe VIP 계약 갱신에 도움이 필요한 경우 **renewalhelp@adobe.com**&#x200B;에 전자 메일을 보내십시오. 곧 연락드리겠습니다.

최종 사용자 제품 액세스가 중단되지 않도록 하려면 기존 VIP 구독 기간이 종료되기 전에 Adobe Admin Console에서 라이선스를 할당하십시오.

* ETLA 고객의 경우 최소 30일 동안 제품이 겹치게 됩니다. 사용자가 Adobe 앱 및 서비스에 계속 액세스할 수 있도록 기념일 이전에 마이그레이션을 완료하십시오. ETLA 계약 만료 세부 정보는 [ETLA 계약에 대한 자동화된 만료 단계](https://helpx.adobe.com/enterprise/using/contract-expiry.html)를 참조하십시오.
* VIP 고객의 경우 멤버십 갱신일 이전에 라이선스를 구매하고 현재 VIP 계약 기간이 종료되기 전에 라이선스를 할당하십시오.
* CLP 또는 TLP 고객은 [라이선스](https://helpx.adobe.com/enterprise/using/licensing.html)의 마이그레이션 지침을 사용하여 serialize된 Acrobat 또는 Creative Suite에서 명명된 사용자 라이선스로 마이그레이션할 수 있습니다.

>[!NOTE]
>
>조직의 라이선스 유형이 변경되면 최종 사용자는 모든 Adobe 제품 또는 서비스에서 로그아웃한 후 동일한 자격 증명으로 다시 로그인해야 합니다.
>
>Photoshop, Acrobat 및 Illustrator과 같은 데스크탑 제품의 경우 도움말 메뉴에서 로그아웃 및 로그인 옵션을 사용합니다. Adobe.com에서 오른쪽 위 모서리에 있는 아이콘을 사용하여 로그아웃했다가 다시 로그인합니다.

## 빠른 라이선스 할당(VIP에서 VIP으로)

VIP을 통해 Creative Cloud for enterprise 또는 Acrobat(for enterprise)을 구입한 현재 VIP 구성원은 빠른 라이선스 할당을 사용하여 갱신 기간 동안 라이선스를 빠르게 할당할 수 있습니다. 적격 고객은 다음과 같은 기준을 충족합니다.

* 제품이 동일함

   1. 갱신 창이 열립니다(VIP 계약 기념일 전 또는 후 30일).
   2. 주문의 엔터프라이즈 제품은 현재 용어의 팀 버전에 해당하는 새로운 SKU입니다.
   3. 엔터프라이즈 라이선스 주문 수량이 기존 팀 라이선스 수량보다 크거나 같습니다.

* 더 높은 가치의 제품

   1. 갱신 창이 열렸습니다.
   2. 주문의 엔터프라이즈 제품은 현재 기간의 팀 제품보다 더 높은 가치를 제공하는 새로운 SKU입니다.
   3. 엔터프라이즈 라이선스 주문 수량이 기존 팀 라이선스 수량보다 크거나 같습니다.

* 빠른 라이선스 할당은 다음 경우에 사용할 수 없습니다.

   * 주문에 대한 기업 라이선스의 수가 기존 팀 라이선스의 수보다 적습니다.
   * 주문은 고부가 기업 제품을 위한 것이지만 주문된 기업 라이선스 수량은 기존 팀 라이선스 수량보다 적습니다.
   * 주문은 수량에 관계없이 팀 및 엔터프라이즈 제품을 혼합합니다.
   * 고객은 갱신 기간 전에 이미 팀 및 엔터프라이즈 제품을 구매했습니다.
   * 엔터프라이즈 갱신 SKU는 새 엔터프라이즈 주문에 사용됩니다.
   * 엔터프라이즈 제품 주문은 다른 VIP 계약 번호에 대한 것입니다.
   * 현재 팀 제품에는 엔터프라이즈 버전이 없는 항목이 포함되어 있습니다.

Adobe이 기업 구매 발주를 처리하면 액세스 권한을 상실하기 전에 사용자를 팀 라이선스에서 Admin Console의 기업 라이선스로 전송해야 하는 날을 포함하는 지침이 포함된 확인 이메일을 받게 됩니다.

Admin Console에서는 빠른 라이선스 할당을 사용하여 라이선스를 할당하라는 메시지가 표시됩니다.

1. 할당할 라이선스 수를 확인합니다.

   ![라이선스 전송](assets/migrate-transfer-licenses.png)

2. 할당 해제된 팀 제품 라이선스가 할당 중인 엔터프라이즈 라이선스와 일치하는지 확인합니다.

3. 프로세스가 완료되면 이메일을 받게 됩니다.

   ![라이선스 할당 확인](assets/migrate-license-assignment.png)

Admin Console에서 [결과 보고서](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header_1346350355)를 다운로드하여 모든 라이선스가 할당되었는지 확인하십시오. 확인 이메일의 날짜 이전에 완료하는 경우 최종 사용자는 서비스가 중단되지 않아야 합니다.

:1관리 역할[&#x200B; 및 &#x200B;](https://helpx.adobe.com/enterprise/using/admin-roles.html)ID[&#x200B; 등 Adobe 온보딩 전문가와 1](https://helpx.adobe.com/kr/enterprise/using/identity.html) 온보딩 통화를 예약하여 Admin Console에 대해 자세히 알아보십시오(아직 수행하지 않은 경우).

>[!NOTE]
>
>빠른 라이선스 할당은 팀 Admin Console에서 초대 보류 중인 사용자를 마이그레이션하지 않습니다.

## 벌크 라이선스 할당(VIP에서 VIP으로)

Admin Console의 CSV 템플릿을 사용하여 대량 작업으로 라이선스를 할당합니다. 다음과 같은 경우에 이 접근 방식을 사용하십시오.

* 빠른 라이선스 할당 요구 사항을 충족하지 않는 VIP 고객이거나
* 갱신 기간 외에 라이선스를 할당해야 합니다.

1. [Adobe Admin Console](https://adminconsole.adobe.com/enterprise)에 액세스할 수 있고 라이선스가 추가되면 **[!UICONTROL 사용자]** > **[!UICONTROL 사용자]**(으)로 이동합니다.
2. ![사용자](assets/migrate-more-options.png) 페이지의 오른쪽 상단 모서리에서 **[!UICONTROL 추가 옵션 메뉴]**&#x200B;를 클릭한 다음 **[!UICONTROL CSV로 사용자 세부 정보 편집]**&#x200B;을 선택합니다.
3. **[!UICONTROL CSV로 사용자 편집]** 대화 상자에서 **[!UICONTROL CSV 템플릿 다운로드]**&#x200B;를 클릭하고 **[!UICONTROL 현재 사용자 목록]**&#x200B;을 선택합니다.

   ![CSV로 사용자 편집](assets/migrate-edit-users-by-csv.png)

   다운로드한 파일의 필드 설명은 [CSV 파일 형식](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header)을 참조하십시오.
4. 라이선스 할당을 CSV에 추가한 다음 업데이트된 파일을 **[!UICONTROL CSV로 사용자 편집]** 대화 상자로 드래그하고 **[!UICONTROL 업로드]**&#x200B;를 클릭합니다. 작업이 완료되면 이메일이 전송됩니다.

   ![사용자 편집 완료](assets/migrate-user-edit-complete.png)

할당의 유효성을 검사하려면 [결과 보고서](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header_1346350355)를 다운로드하십시오. 그런 다음 Adobe 온보딩 전문가와 온보딩을 예약하여 [관리 역할](https://helpx.adobe.com/enterprise/using/admin-roles.html) 및 [ID](https://helpx.adobe.com/kr/enterprise/using/identity.html)에 대해 알아보세요.

## 벌크 라이선스 할당(VIP에서 ETLA으로)

VIP 구독이 있고 사용자를 ETLA으로 이동하는 경우 이 벌크 흐름을 사용하십시오.

1. [Adobe Admin Console](https://adminconsole.adobe.com/enterprise)에 로그인하고 VIP 사용자가 포함된 조직을 엽니다.
2. **[!UICONTROL 사용자]** > **[!UICONTROL 사용자]**(으)로 이동합니다.
3. 오른쪽 상단의 ![추가 옵션 메뉴](assets/migrate-more-options.png)를 클릭한 다음 **[!UICONTROL 사용자 목록을 CSV로 내보내기]**&#x200B;를 선택합니다.
4. 해당 사용자를 원하는 ETLA 조직을 엽니다.
5. **[!UICONTROL 사용자]** > **[!UICONTROL 사용자]**(으)로 이동합니다.
6. **[!UICONTROL CSV로 사용자 추가]**&#x200B;를 클릭합니다.
7. **[!UICONTROL CSV 템플릿 다운로드]**&#x200B;를 클릭한 다음 3단계에서 내보낸 CSV에서 VIP 사용자를 추가합니다.
8. 업데이트된 CSV를 업로드합니다.

사용자가 ETLA 조직에 추가되면 이메일을 받게 됩니다.

![VIP에서 ETLA으로 마이그레이션한 후 추가된 사용자](assets/migrate-users-added-vip-etla.png)

할당의 유효성을 검사하려면 [결과 보고서](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header_1346350355)를 다운로드하십시오. [관리 역할](https://helpx.adobe.com/enterprise/using/admin-roles.html) 및 [ID](https://helpx.adobe.com/kr/enterprise/using/identity.html)에 대해 Adobe 온보딩 전문가와 온보딩을 예약하십시오.

일괄 업로드 문제에 대해서는 [일괄 사용자 업로드 문제 해결](https://helpx.adobe.com/enterprise/kb/troubleshoot-bulk-user-csv-upload.html)을 참조하십시오.

## 벌크 라이선스 할당(ETLA에서 VIP으로)

ETLA 구독이 있고 사용자를 VIP으로 이동하는 경우:

1. [Adobe Admin Console](https://adminconsole.adobe.com/enterprise)에 로그인하고 ETLA 사용자가 포함된 조직을 엽니다.
2. **[!UICONTROL 사용자]** > **[!UICONTROL 사용자]**(으)로 이동합니다.
3. 오른쪽 상단의 ![추가 옵션 메뉴](assets/migrate-more-options.png)를 클릭한 다음 **[!UICONTROL 사용자 목록을 CSV로 내보내기]**&#x200B;를 선택합니다.

   ![사용자 목록 메뉴 내보내기](assets/migrate-export-user-list.png)

4. 해당 사용자를 원하는 VIP 조직을 엽니다.
5. **[!UICONTROL 사용자]** > **[!UICONTROL 사용자]**(으)로 이동합니다.
6. **[!UICONTROL CSV로 사용자 추가]**&#x200B;를 클릭합니다.
7. **[!UICONTROL CSV 템플릿 다운로드]**&#x200B;를 클릭한 다음 3단계에서 내보낸 CSV에서 ETLA 사용자를 추가합니다.
8. 업데이트된 CSV를 업로드합니다.

사용자가 VIP 조직에 추가되면 이메일을 받게 됩니다.

![ETLA에서 VIP으로 마이그레이션한 후 추가된 사용자](assets/migrate-users-added-etla-vip.png)

할당의 유효성을 검사하려면 [결과 보고서](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header_1346350355)를 다운로드하십시오. [관리 역할](https://helpx.adobe.com/enterprise/using/admin-roles.html) 및 [ID](https://helpx.adobe.com/kr/enterprise/using/identity.html)에 대해 Adobe 온보딩 전문가와 온보딩을 예약하십시오.

일괄 업로드 문제에 대해서는 [일괄 사용자 업로드 문제 해결](https://helpx.adobe.com/enterprise/kb/troubleshoot-bulk-user-csv-upload.html)을 참조하십시오.
