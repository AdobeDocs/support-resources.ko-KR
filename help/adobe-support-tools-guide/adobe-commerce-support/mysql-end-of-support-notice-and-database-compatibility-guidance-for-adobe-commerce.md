---
title: Adobe Commerce에 대한 MySQL 지원 종료 알림 및 데이터베이스 호환성 지침
description: 이 문서에서는 지원되는 Adobe Commerce 버전에 대한 MySQL 지원 종료 타임라인 및 데이터베이스 호환성 지침에 대해 설명합니다.
solution: Commerce
source-git-commit: 2198e1882260ca17b8b99f7ed6d415791ec0d177
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Adobe Commerce에 대한 MySQL 지원 종료 알림 및 데이터베이스 호환성 지침

이 문서에서는 지원되는 Adobe Commerce 버전에 대한 MySQL EOS(지원 종료) 및 데이터베이스 호환성에 대한 중요한 정보를 제공합니다.
Adobe은 판매자가 이 발표를 검토하고 플랫폼 안정성을 유지하고 지원 요구 사항을 준수하도록 조치를 취할 것을 강력히 권장합니다.
[MariaDB에 대한 업그레이드 필수 구성 요소](https://experienceleague.adobe.com/ko/docs/commerce-operations/implementation-playbook/best-practices/maintenance/mariadb-upgrade) 및 [시스템 요구 사항](https://experienceleague.adobe.com/ko/docs/commerce-operations/installation-guide/system-requirements)에서 자세히 알아보세요.

## MySQL 8.0 지원 종료(EOS)

MySQL 8.0은 2026년 4월 30일에 지원 종료(EOS)됩니다.
이 날짜 이후, 다음 Adobe Commerce 버전은 MySQL 8.0 이후 릴리스된 MySQL 버전과의 호환성을 지원하거나 유지하지 않습니다.

* Adobe Commerce 2.4.7
* Adobe Commerce 2.4.6
* Adobe Commerce 2.4.5

Adobe은 이러한 Adobe Commerce 릴리스에서 최신 MySQL 주요 버전에 대한 유효성을 검사하거나 지원을 제공하지 않습니다.

## 온-프레미스 고객에 대한 필수 작업

다음 버전을 실행하는 Adobe Commerce 온-프레미스 설치는 데이터베이스 서버를 호환되는 MariaDB 버전으로 마이그레이션하는 것이 좋습니다.

* 2.4.5
* 2.4.6
* 2.4.7

MariaDB는 이러한 릴리스에서 완벽하게 지원되며 향후 권장되는 데이터베이스 플랫폼입니다.

* 2.4.5
* 2.4.6
* 2.4.7

데이터베이스 서버를 호환되는 MariaDB 버전으로 마이그레이션하는 것이 좋습니다.
MariaDB는 이러한 Adobe Commerce 버전에 대해 완전히 지원되며 권장 데이터베이스 플랫폼입니다.

## Adobe Commerce 2.4.8 및 2.4.9의 MySQL 지원

Adobe Commerce 2.4.8 및 2.4.9는 MySQL을 지원하는 마지막 Adobe Commerce 버전입니다.

이러한 버전의 경우:
* MySQL 8.4는 Adobe Commerce에서 지원하는 최종 MySQL 버전입니다.
* 8.4 이후 릴리스된 MySQL 버전은 Adobe Commerce에서 인증되거나 지원되지 않습니다.

## 향후 방향: 기본 데이터베이스 플랫폼인 MariaDB

앞으로 Adobe Commerce은 MariaDB를 기본 및 권장 데이터베이스 플랫폼으로 계속 지원합니다.

Adobe은 장기적인 호환성을 유지하고 정렬을 지원하기 위해 다음 고객이 MariaDB로의 마이그레이션을 계획할 것을 강력히 권장합니다.
* 모든 Adobe Commerce 2.4.8 및 2.4.9 온프레미스 고객
* 이전에 지원되는 Adobe Commerce 버전을 실행하는 고객
