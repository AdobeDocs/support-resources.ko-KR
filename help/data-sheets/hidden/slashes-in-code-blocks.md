---
title: 코드 블록 UGP-11189의 슬래시
description: 코드 블록 UGP-11189 테스트의 슬래시
hide: true
hidefromtoc: true
source-git-commit: 4fc9b739d18941d276b88f8799163523c8bd5f85
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 4%

---

# 코드 블록의 슬래시

1. 다음 명령을 실행합니다.

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. 다음 단계

코드 블록에 없음

vendor/bin/magento-patches -n 상태 |grep &quot;27015\|상태&quot;

이스케이프 처리된 백슬래시:

vendor/bin/magento-patches -n 상태 |grep &quot;27015&bsol;|상태&quot;
