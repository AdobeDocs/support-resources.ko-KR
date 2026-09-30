---
title: 모범 사례 및 안정성
description: Adobe Commerce 판매자가 휴가철과 같이 트래픽이 많은 이벤트에 대비할 수 있는 환경을 준비하는 데 도움이 되는 모범 사례 및 안정성 권장 사항입니다.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/iA6ioGYYgQSotPrPqujDBdRcjBLUQXMGXfwlcSMGjkM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 4%
---

# 모범 사례 및 안정성

이 섹션에서는 휴가철과 같은 트래픽이 많은 이벤트에 대해 Adobe Commerce 환경(Commerce on cloud infrastructure 및 온프레미스)을 준비하기 위한 기술 권장 사항을 제공합니다.

>[!NOTE]
>
>**(클라우드 전용)**(으)로 표시된 단계는 클라우드 인프라의 Commerce에 적용됩니다. 대부분의 다른 권장 사항은 온-프레미스 배포에도 적용됩니다.

## 최신 버전의 Adobe Commerce으로 업그레이드 {#upgrade-to-latest-version-of-adobe-commerce}

사이트가 지원되지 않는 버전의 Adobe Commerce에 있지 않은지 확인하십시오. 해당 버전은 사이트의 성능에 영향을 주고 보안 문제에 대한 취약성을 높일 수 있습니다. 최신 버전의 Adobe Commerce으로 업그레이드하여 보안을 유지하고 휴가철을 준비하십시오.

Adobe Commerce의 [최신 릴리스](https://experienceleague.adobe.com/ko/docs/commerce-operations/release/notes/overview)에는 이전 버전에서 업그레이드할 때 프로젝트에 도움이 되는 개선 사항 및 완화된 문제를 포함한 많은 [중요 보안 수정 사항](https://experienceleague.adobe.com/ko/docs/commerce-operations/release/notes/security-patches/overview)이 포함되어 있습니다.

지원되지 않는 버전의 Adobe Commerce에 대한 자세한 내용은 [Adobe Commerce 수명 주기 정책](https://experienceleague.adobe.com/ko/docs/commerce-operations/release/planning/lifecycle-policy)을 검토하십시오.

## 최신 ECE-Tools 및 Quality Patch Tool(QPT) 설치 {#install-latest-ece-tools-and-quality-patch-tool-qpt}

`--with-dependencies` 스위치를 사용하여 최신 `ece-tools` 모듈 및 해당 종속 모듈이 설치되었으므로 Adobe Commerce 버전에 필요한 모든 클라우드 패치가 올바르게 설치되어야 합니다. 단계는 [ECE-Tools 패키지 업데이트](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/dev-tools/ece-tools/update-package)를 참조하십시오.

품질 패치 도구에서 사용할 수 있는 패치 목록을 검토하고 Adobe Commerce 버전과 호환되는 성능 패치가 적용되었는지 확인합니다. [품질 패치 도구: 패치 검색](https://experienceleague.adobe.com/ko/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/patches-available-in-qpt-tool-overview)을 참조하십시오.

>[!NOTE]
>
>QPT는 Adobe Commerce 온 클라우드 인프라와 온프레미스 설치 모두에서 사용할 수 있습니다. 설치 및 사용 명령은 둘 간에 다릅니다. 클라우드의 경우 QPT는 ECE-Tools 패키지에 포함되어 있습니다.

## 로그 파일 검토 및 정리 {#review-and-clean-log-files}

클라우드 환경의 로그 파일(예: `~/var/log`의 응용 프로그램 로그 파일)을 검토하고 기본 또는 사용자 지정 로그 파일에 기록되는 자주 기록되는 레코드를 식별합니다. 자세한 내용은 [로그 보기 및 관리](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/develop/test/log-locations)를 참조하세요.

* 다음 기본 로그 파일을 검토하고 반복 오류를 수정하십시오. `~/var/log`, `~/var/log/exception.log`, `~/var/log/support_report.log`, `~/var/log/system.log`, `~/var/report`.
* 이전 문제 해결을 위해 이전에 추가된 디버그 로그를 제거합니다.

이러한 로그는 [!DNL New Relic]에서도 사용할 수 있습니다. [New Relic 로그 관리](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management)를 참조하세요.

## 디스크 크기 증가 모니터링 {#monitor-disk-size-growth}

클라우드 인프라의 Adobe Commerce에는 두 개의 기본 디스크 볼륨이 있습니다. 트래픽이 많을 때 이러한 볼륨을 모니터링하여 사용 가능한 공간이 충분한지 확인합니다. Adobe Commerce은 볼륨 중 하나가 사용률 70%를 초과하면 경고를 제공합니다.

* `/mnt/shared`(로그 및 미디어 파일을 포함한 공유 파일)
* `/data/mysql`(데이터베이스 볼륨)

자세한 내용은 [디스크 공간 관리](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/develop/storage/manage-disk-space)를 참조하십시오.

## 가장 느린 데이터베이스 요청 검토 {#review-slowest-database-requests}

[!DNL New Relic]에서 시간이 가장 많이 소요되는 데이터베이스 트랜잭션을 정기적으로 모니터링하고 검토하는 것이 중요합니다. 매우 느린 쿼리 및 구성 요소를 조사합니다.

* **가장 많은 시간이 걸리는 트랜잭션을 확인합니다.** **[!UICONTROL New Relic]** > **[!UICONTROL APM 및 서비스]** > 환경 선택 > **[!UICONTROL 데이터베이스]**, 가장 많은 시간이 걸리는 트랜잭션을 기준으로 정렬합니다.

* **MySQL 느린 쿼리 로그를 확인합니다.** 시스템에서 기록한 느린 쿼리에 대해 `mysql-slow.log`을(를) 검토합니다. 이러한 로그는 [!DNL New Relic]에서도 사용할 수 있습니다. **[!UICONTROL New Relic]** > **[!UICONTROL 로그]**(으)로 이동한 다음 `filePath:"/var/log/mysql/mysql-slow.log"`(으)로 필터링하세요.

[!DNL MySQL] 느린 쿼리 로그를 정기적으로 검토하여 느린 쿼리가 자주 실행되지 않는지 확인하십시오. 문제가 있는 것으로 식별한 쿼리를 해결하는 단계는 [데이터베이스 성능 문제 해결](https://experienceleague.adobe.com/ko/docs/commerce-operations/implementation-playbook/best-practices/maintenance/resolve-database-performance-issues)을 참조하십시오.

## cron 작업 구성 {#configure-cron-jobs}

Commerce의 모든 비동기 작업은 Linux cron 명령을 사용하여 수행됩니다.

Commerce은 색인 지정 및 큐 소비자 작업을 포함한 중요한 시스템 기능에 대한 적절한 cron 작업 구성에 따라 달라집니다. 이를 제대로 설정하지 못하면 Commerce이 예상대로 작동하지 않게 된다.

Unix crontab 파일에서 적절한 Unix 사용자를 사용하여 Commerce cron을 올바르게 설정하고 구성해야 합니다. 각 Unix 사용자는 자체 crontab 파일을 가지며, 이 파일은 해당 사용자에 대한 cron 작업을 실행하는 데 사용되는 구성입니다. 단계는 [cron 작업 구성 및 실행](https://experienceleague.adobe.com/ko/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs)을 참조하십시오.

`dev/tools/cron.sh` 스크립트가 제거되었기 때문에 더 이상 실행할 수 없습니다.

## 클라이언트측 설정 최적화 {#optimize-client-side-settings}

Commerce 인스턴스의 상점 응답성을 개선하려면 개발자 모드에서만 사용할 수 있는 **[!UICONTROL 스토어]** > **[!UICONTROL 구성]** > **[!UICONTROL 고급]** > **[!UICONTROL 개발자]**&#x200B;에서 다음 설정을 구성하십시오.

* **[!UICONTROL 표 설정]** > **[!UICONTROL 비동기 인덱싱]**: *[!UICONTROL 사용]*
* **[!UICONTROL CSS 설정]** — **[!UICONTROL CSS 파일 축소]**: *[!UICONTROL 예]*
* **[!UICONTROL JavaScript 설정]** — **[!UICONTROL JavaScript 파일 축소]**: *[!UICONTROL 예]*
* **[!UICONTROL JavaScript 설정]** — **[!UICONTROL JavaScript 번들 활성화]**: *[!UICONTROL 예]*(기본적으로 활성화되지 않음)
* **[!UICONTROL 템플릿 설정]** — **[!UICONTROL HTML 축소]**: *[!UICONTROL 예]*

클라우드의 Adobe Commerce은 항상 프로덕션 모드에서 실행되므로 대신 명령줄에서 각 옵션(예: `bin/magento config:set --lock-config dev/css/minify_files 1`)을 설정한 다음 결과 `app/etc/config.php` 변경 내용을 커밋하고 다시 배포합니다. CLI 경로의 전체 목록은 [리소스 파일 최적화](https://experienceleague.adobe.com/ko/docs/commerce-operations/implementation-playbook/best-practices/development/optimize-css-js-files)를 참조하십시오.
