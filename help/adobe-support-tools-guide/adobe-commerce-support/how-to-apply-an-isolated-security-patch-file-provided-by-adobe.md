---
title: Adobe에서 제공하는 격리된 패치를 적용하는 방법
description: 이 문서에서는 Adobe Commerce 온-프레미스, Adobe Commerce 온-클라우드 인프라 및 Magento Open Source용 Isolated 패치를 적용하는 방법에 대해 설명합니다.
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
autotag-review: '2026-08-19T13:22:21.768Z'
TQID: 'https://experienceleague.adobe.com/tmaNqB6uOX2ukmfxQvcqFvYwm2UyO6USzb7t8hFQM1A'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
source-git-commit: 45b00b9b0d2ceb422747c0a4a34f060f33ab127b
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 0%

---

# Adobe에서 제공하는 격리된 패치를 적용하는 방법

이 문서에서는 Adobe Commerce 온-프레미스, Adobe Commerce 온-클라우드 인프라 및 Magento Open Source용 Isolated 패치를 적용하는 방법에 대해 설명합니다.

>[!WARNING]
>
>프로덕션 환경에 적용하기 전에 스테이징/통합 환경에서 패치를 적용하고 테스트하는 것이 좋습니다. 또한 조작하기 전에 최근 백업을 수행하는 것이 좋습니다.

## 클라우드 인프라에서 Adobe Commerce용 Isolated 패치를 적용하는 방법 {#cloud}

1. 프로젝트 루트에 이름이 `m2-hotfixes`인 디렉터리가 없는 경우 만드십시오.
1. `%patch_name%.patch` 파일을 `m2-hotfixes` 디렉터리에 복사합니다.
1. 코드 변경 사항을 추가, 커밋 및 푸시합니다.

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.patch patch"
   ```

   ```git
   git push origin
   ```

클라우드 프로젝트에 패치를 적용하는 방법에 대한 자세한 내용은 [패치 적용](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/upgrade/apply-patches)을 참조하십시오.

## Adobe Commerce 온-프레미스 및 Magento Open Source용 Isolated 패치를 적용하는 방법 {#commerce}

1. Adobe Commerce 온-프레미스 또는 Magento Open Source 루트 디렉터리에 패치를 업로드합니다.
1. 다음 SSH 명령을 실행합니다.

   ```bash
   patch -p1 < %patch_name%.patch
   ```

   (위 명령이 작동하지 않으면 `-p1` 대신 `-p2`을(를) 사용해 보십시오.)

1. 변경 내용을 반영하려면 **[!UICONTROL 시스템]** > **[!UICONTROL 캐시 관리]**&#x200B;의 [!UICONTROL 관리자]에서 캐시를 새로 고치십시오.
