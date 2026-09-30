---
title: 운영 준비
description: Adobe Commerce 판매자가 휴가철과 같이 트래픽이 많은 이벤트에 대비할 수 있는 환경을 준비하는 데 도움이 되는 운영 준비 권장 사항입니다.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bcd8874c-7b93-5596-bdaa-22660e84df14
    internal-label: Deploy
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 938d2364-5176-55ec-80f1-9415253e5e51
    internal-label: Site Management
  - id: b48dbafb-4193-5648-b9d9-bf96e9c9a411
    internal-label: Backend Development
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
    internal-label: Admin tools and workspace
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
    internal-label: Admin workspace
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: c89c0345d0e483463ab44195c2d5c0cb18d1d4c5
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%
---

# 운영 준비

이 섹션에서는 휴가철과 같은 트래픽이 많은 이벤트에 대해 Adobe Commerce 환경(Commerce on cloud infrastructure 및 온프레미스)을 준비하기 위한 기술 권장 사항을 제공합니다.

## 모든 보안 및 성능 패치 적용 {#apply-all-security-and-performance-patches}

배포 중단을 방지하기 위해 코드를 동결하기 전에 모든 업데이트를 완료합니다.

## 휴일 전 상태 검사 실행 {#run-pre-holiday-health-checks}

백업, cron 상태 및 캐시 warmup 스크립트를 테스트하여 로드 중 원활한 작업을 보장합니다.

## 모니터링 플레이북 설정 {#establish-monitoring-playbooks}

피크 기간 동안 연중무휴 24시간 응답을 위해 경고 임계값, 에스컬레이션 단계 및 연락처 정보를 문서화합니다.

## 문서 롤백 계획 {#document-rollback-plans}

버전 관리된 롤백 전략을 유지 관리하여 배포 예외 항목에서 신속하게 복구할 수 있습니다.

