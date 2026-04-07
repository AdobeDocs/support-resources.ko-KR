---
title: IP 주소로 제품 액세스 제한
description: IP 기반 액세스를 사용하여 Adobe 제품에 대한 사용자 액세스를 제어하고 승인된 공개 IP 범위로 사용을 제한합니다.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: e4595040-3930-48af-9888-cf1349596c77
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---

# IP 주소로 제품 액세스 제한

Enterprise에 적용됩니다.

IP 기반 액세스를 사용하여 Adobe 제품에 대한 사용자의 액세스를 제어하고 목록에 없는 공개 IP 주소의 무단 사용을 방지합니다.

Adobe 앱 및 서비스의 안전한 사용을 위해 [Admin Console](https://adminconsole.adobe.com/settings/identity)&#x200B;(으)로 이동하여 **IP 기반 액세스** 허용 목록에 신뢰할 수 있는 공용 IP 주소를 추가하십시오.

## IP 기반 액세스의 이점

IP 기반 액세스 제어는 IP 주소 허용 목록에 추가하다를 사용하여 임의의 공개 IP 주소에서 Adobe 제품의 사용을 제한합니다. IP 기반 액세스는 Adobe Admin Console의 모든 디렉터리 및 관련 제품에 적용됩니다.

**허용 IP 주소** 목록에 신뢰할 수 있는 공용 IP를 추가하여 사용자의 사용을 중지할 수 있습니다.

- 허용된 IP 범위를 벗어난 공용 IP의 제품에 액세스
- 허용된 IP 범위 외부의 공용 IP에서 Adobe [사용자 프로필](https://helpx.adobe.com/kr/enterprise/using/manage-adobe-profiles.html)에 로그인
- 웹 앱의 사용자 프로필을 허용된 IP 범위 외부로 전환

  ![조직 구조 내보내기](./assets/ip-based-access.avif)

## IP 기반 액세스 활성화

### 중요한 고려 사항

>[!IMPORTANT]
>
>- 관리자는 자신의 공개 IP 주소를 추가한 다음 다른 IP 범위만 추가해야 합니다. 그렇지 않으면 오류가 발생할 수 있습니다.
>- IP 기반 액세스는 개인 IP 주소에 적용되지 않습니다.

CIDR 형식에서만 최대 150개의 다양한 공개 IP 범위를 추가할 수 있습니다.

Adobe Admin Console에서 IP 기반 액세스를 활성화하려면 다음 단계를 따르십시오.

1. **[Adobe Admin Console 설정](https://adminconsole.adobe.com/settings/identity)** 섹션으로 이동합니다.
2. 선택 메뉴에서 **[!UICONTROL 개인 정보 및 보안]**&#x200B;을 선택하고 확장한 다음 **[!UICONTROL 인증 설정]**&#x200B;을 선택합니다.
3. **[!UICONTROL IP 기반 액세스]** 섹션에서 **[!UICONTROL IP 주소 추가]** 단추를 선택합니다.
4. **[!UICONTROL IP 주소 추가]** 창에서:
   - 공개 IP 주소 또는 CIDR 블록을 입력하여 허용 목록에 추가하다에 추가하십시오.
   - 여러 IP 주소를 구분하려면 쉼표를 사용하십시오.
   - **[!UICONTROL 저장]**&#x200B;을 선택합니다.

   현재는 IPv4 형식만 지원합니다. 다음은 몇 가지 예입니다.
   - IP v4 주소: 1.3.4.6
   - IP v4 서브넷 주소: 1.2.0.0/24

몇 분 내에 IP 주소가 추가됩니다. 연결된 사용자는 다음에 허용된 공개 IP 주소 외부에서 로그인하거나 프로필을 전환하려고 하면 제한 사항이 표시됩니다. 이 변경 사항을 사용자에게 미리 알리는 것이 좋습니다.

각 항목 옆에 있는 편집 또는 삭제 옵션을 선택하여 나열된 IP 주소를 편집하거나 제거할 수 있습니다.

>[!NOTE]
>
>- IP 기반 액세스가 활성화되면 **강제 로그아웃이 발생하지 않습니다**. 사용자는 웹에서 로그인하거나 프로필을 전환할 때 제한된 프로필을 선택하려고 할 때만 영향을 받습니다.
>- 보안 웹 게이트웨이를 사용하는 경우 모든 트래픽이 이 게이트웨이를 통해 라우팅되는지 확인하십시오. Adobe 앱 및 서비스가 올바르게 작동할 수 있도록 [허용할 도메인 목록](https://helpx.adobe.com/kr/enterprise/kb/network-endpoints.html)을 봅니다.
>- 잘못된 IP 주소를 입력했기 때문에 Admin Console에서 잠긴 경우 [Adobe 고객 지원 센터](https://helpx.adobe.com/kr/enterprise/using/support-for-enterprise.html)에 문의하십시오.

## 대화에 참여

공동 작업하고, 질문하고, 다른 관리자와 대화하려면 [Enterprise 및 Teams 커뮤니티](https://www.adobe.com/go/entcom_kr)를 방문하세요.
