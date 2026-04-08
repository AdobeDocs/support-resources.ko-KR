---
title: Experience League 지원 릴리스 노트
description: Experience League 지원에 대한 최신 릴리스 정보입니다.
feature: Release Notes
exl-id: 875ad82e-56b5-4d58-9237-bb7aa0d9ffaf
source-git-commit: 2d3eefd7816fbd25898549b20a0ae913b8b51391
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 2%

---

# Experience League 지원 릴리스 노트

이러한 릴리스 노트에는 Experience League 지원에 대한 업데이트가 포함되어 있으며 다음이 포함되어 있습니다.

새 기능 ![개](../adobe-support-tools-guide/assets/new.svg)개
![수정](../adobe-support-tools-guide/assets/fix.svg) 수정 사항 및 개선 사항
![버그](../adobe-support-tools-guide/assets/bug.svg) 알려진 문제

## 2026년 4월 9일 - 콜백 요청 기능 확장

이제 Marketo 제품 사용자가 콜백 요청 기능을 사용할 수 있습니다.

## 2026년 3월 30일 - 고급 사례 양식

![새로 만들기](../adobe-support-tools-guide/assets/new.svg) 사례 양식은 사용자가 각 단계에서 필요한 정보를 이해하는 데 도움이 되는 안내식 흐름으로 구성되어 있습니다.

- [!UICONTROL 제품 선택]
- [!UICONTROL 문제 설명]
- [!UICONTROL 시스템 정보]
- [!UICONTROL 우선 순위 및 비즈니스 영향]
- [!UICONTROL 연락처 정보 및 감시자 목록]
- [!UICONTROL 검토 및 제출]

![새로 만들기](../adobe-support-tools-guide/assets/new.svg) **[!UICONTROL 문제 설명]**&#x200B;을(를) 기반으로 자동 제목 생성을 추가했습니다. 이렇게 하면 사용자에게 사례를 제출하기 전에 편집할 수 있는 옵션을 제공하는 동안 제목을 자동으로 생성할 수 있습니다.

![새로 만들기](../adobe-support-tools-guide/assets/new.svg)에서 **[!UICONTROL 을(를) 추가함&quot;문제가 재현될 수 있습니까?&quot;문제 해결을 개선하는 데 도움이 되는]** 옵션입니다. 사용자가 **[!UICONTROL 예]**&#x200B;를 선택하면 문제를 재현하는 데 필요한 단계를 제공하라는 메시지가 표시됩니다. *아니요*&#x200B;를 선택한 경우 사용자는 사례 제출을 계속할 수 있습니다.

![새로 만들기](../adobe-support-tools-guide/assets/new.svg) 환경 또는 인스턴스에 최근 변경 내용이 있는지 여부를 나타내는 옵션을 추가했습니다. **[!UICONTROL 예]**&#x200B;를 선택하면 변경 내용에 대한 추가 세부 정보를 입력하라는 메시지가 표시됩니다.

![새로 만들기](../adobe-support-tools-guide/assets/new.svg) 권한 있는 제품에 대해 **추가 [!UICONTROL 환경 컨텍스트] 필드**&#x200B;를 추가하여 중요한 세부 정보를 캡처합니다.

- **Marketo**
   - Munchkin ID
- **Adobe Target**
   - 활동 이름
   - 사이트 URL(태그 속성 이름)
- **Adobe Analytics**
   - RSID
   - 사이트 URL(태그 속성 이름) / cURL
   - Workspace Shortlink
- **Adobe Journey Optimizer(AJO)**
   - 여정 ID 또는 URL/캠페인 ID 또는 URL/채널 ID 또는 URL/Offer Decisioning ID 또는 URL
   - 프로필 예
   - 샌드박스 이름
- **Real-Time Customer Data Platform(RTCDP)**
   - 영향을 받는 구성 요소 ID(대상 ID/대상 ID/데이터 세트 ID/데이터 흐름 ID/병합 정책 ID/스키마 ID/Source ID/배치 ID)
   - 프로필 예
   - 샌드박스 이름
- **Adobe Experience Platform(AEP)**
   - 영향을 받는 구성 요소 ID(대상 ID/대상 ID/데이터 세트 ID/데이터 흐름 ID/병합 정책 ID/스키마 ID/Source ID/배치 ID)
   - 프로필 예
   - 샌드박스 이름
- **Customer Journey Analytics(CJA)**
   - Workspace 프로젝트 URL
   - 연결 ID/오류 메시지/코드
   - 데이터 보기 ID

![새로 만들기](../adobe-support-tools-guide/assets/new.svg) 사례 만들기 흐름을 중단하지 않고 유용한 지침을 표시하기 위해 **AI 기반 [!UICONTROL 권장 사항 패널]**&#x200B;을 추가했습니다.

![새로 만들기](../adobe-support-tools-guide/assets/new.svg) 입력한 모든 정보를 통합적으로 볼 수 있도록 하고 사용자가 다음 작업을 수행할 수 있도록 하는 **[!UICONTROL 검토 요약]** 단계를 추가했습니다.

- 한 곳에서 사례 세부 정보 검토
- 편집하려면 이전 단계로 돌아가십시오.
- 진행률을 잃지 않고 요약으로 돌아가기

![수정](../adobe-support-tools-guide/assets/fix.svg) 대/소문자 설명 필드 이름이 *[!UICONTROL (으)로 바뀌었습니다. 명확성을 위해 문제를 설명&quot;]*&#x200B;하십시오.

![수정](../adobe-support-tools-guide/assets/fix.svg) 별표(*)를 필수 필드 표시기로 추가하여 완전성을 보장하고 제출 오류를 줄입니다.

## 2026년 3월 18일 - 콜백 요청 기능 확장

이제 Experience League에서 콜백 요청 옵션을 제공하여 화면 공유 기능을 통해 셀프 서비스 웹 모임 일정을 활성화하여 문제를 보다 빠르게 해결할 수 있습니다.

- 이 기능은 Adobe Experience Manager, Campaign 및 Workfront에서 사용할 수 있습니다.
- 고객은 자신의 편의에 따라 모임을 예약할 수 있고, 즉석 초대장도 받을 수 있다.
- Adobe Experience Manager P1 사례의 경우 즉각적인 콜백을 통해 중요한 문제 중에 더 빠른 참여를 보장하므로 다운타임과 비즈니스 영향을 최소화하는 데 도움이 됩니다.
