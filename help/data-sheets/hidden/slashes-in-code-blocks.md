---
title: 코드 블록 UGP-11189의 슬래시
description: 코드 블록 UGP-11189 테스트의 슬래시
hide: true
hidefromtoc: true
source-git-commit: 2255dad674f1b4d456ffb50ebec9313bc4b3d7f5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# 코드 블록의 슬래시

1. 다음 명령을 실행합니다.

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. 명령을 실행합니다(이스케이프 처리).

   ```bash
   vendor/bin/magento-patches -n status |grep "27015&bsol;|Status"
   ```

코드 블록에 없음

vendor/bin/magento-patches -n 상태 |grep &quot;27015\|상태&quot;

이스케이프 처리됨:

vendor/bin/magento-patches -n 상태 |grep &quot;27015&amp;bsol;|상태&quot;

