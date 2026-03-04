---
title: Adobe Commerce 클라우드 프로젝트에 사용자를 추가할 수 없음
description: 이 문서에서는 Adobe Commerce 클라우드 프로젝트에 사용자를 추가할 수 없는 경우에 대한 솔루션을 제공합니다.
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
exl-id: 2dc52d5e-0930-48c4-986e-ce3f9f6f8221
source-git-commit: 755c6dc9cff041b9ca9183fbecde21f90fbaee1a
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---

# Adobe Commerce 클라우드 프로젝트에 사용자를 추가할 수 없음

이 문서에서는 클라우드 프로젝트에 사용자를 추가하려고 하지만 실패하고 오류가 발생하는 경우를 위한 솔루션을 제공합니다. *사용자 XXX가 없습니다*.

## 영향을 받는 제품 및 버전

* 클라우드 인프라의 Adobe Commerce, [지원되는 모든 버전](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## 문제

이 문서에서는 Adobe Commerce 클라우드 프로젝트에 사용자를 추가할 수 없는 경우에 대한 솔루션을 제공합니다.

## 원인

프로젝트에 사용자로 추가하려면 먼저 [https://accounts.magento.cloud](https://accounts.magento.cloud)에서 사용자 계정을 만들고 Adobe SSO에 연결해야 합니다. 사용자에게 Adobe 계정이 있지만 Commerce(magento.com) 계정이 없는 경우 먼저 계정을 만들어야 합니다.

## 솔루션

1. 사용자에게 [https://accounts.magento.cloud](https://accounts.magento.cloud)에 로그인하도록 요청하세요. 사용자는 이미 동일한 이메일 주소를 사용하여 Adobe에 등록해야 합니다.
   >[!NOTE]
   >[https://account.adobe.com](https://account.adobe.com)에 계정을 만들거나 보유하고 있다고 해서 사용자가 [https://accounts.magento.cloud](https://accounts.magento.cloud)에 계정이 있는 것은 아닙니다. 사용자는 먼저 [Commerce 계정을 만들어야](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account) 합니다.

1. 사용자가 이미 Adobe 계정을 가지고 있지만 로그인할 수 없는 경우 [문제 이유](https://experienceleague.adobe.com/home#support)가 [!UICONTROL 사용자 관리]&#x200B;(으)로 설정된 *지원 요청*&#x200B;을 제출하도록 요청하세요.

1. 사용자가 [https://accounts.magento.cloud](https://accounts.magento.cloud)에 성공적으로 로그인하면 사용자를 프로젝트에 추가할 수 있습니다. 자세한 단계는 Commerce on Cloud Infrastructure Guide에서 [사용자 추가 및 액세스 관리](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access)를 참조하십시오.

## 관련 읽기:

* Commerce on Cloud Infrastructure 안내서의 [사용자 액세스 관리](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html).
* [Adobe Commerce 지원 또는 클라우드 계정에 로그인할 수 없음](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html)
