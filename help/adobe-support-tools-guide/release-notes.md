---
title: 새로운 EXL 사례 양식 릴리스 정보
description: EXL 사례 양식에 대한 최신 릴리스 정보입니다.
feature: Release Notes
source-git-commit: 421ef19ed939cd757e3182c8fa5bbda13fd7561e
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 6%

---


# 새로운 EXL 사례 양식 릴리스 정보

새로운 사례 생성 환경에서는 문제 해결을 간소화하기 위해 새로 고침된 양식을 도입했으며 다음과 같은 내용이 포함됩니다.

![신규](../adobe-support-tools-guide/assets/new.svg) - 새로운 기능
![수정 사항](../adobe-support-tools-guide/assets/fix.svg) - 수정 사항 및 개선 사항
![버그](../adobe-support-tools-guide/assets/bug.svg) - 알려진 문제

## 릴리스 1.0 - 향상된 사례 만들기 양식

*2026년 1월 15일 금요일*

![새로 만들기](../adobe-support-tools-guide/assets/new.svg) 사례 양식은 안내식 흐름으로 구성되어 있으므로 각 단계에서 필요한 정보를 사용자가 이해할 수 있습니다.

- [!UICONTROL 제품 선택]
- [!UICONTROL 문제 세부 정보]
- [!UICONTROL 시스템 정보]
- [!UICONTROL 영향]
- [!UICONTROL 연락처 정보]
- [!UICONTROL 검토 및 제출]

![새로 만들기](../adobe-support-tools-guide/assets/new.svg) 실행 가능한 세부 정보를 캡처하고 문제 해결을 가속화하기 위해 **새 [!UICONTROL 재현 단계] 필드**&#x200B;를 추가했습니다.

![새로 만들기](../adobe-support-tools-guide/assets/new.svg) 권한 있는 제품에 대해 **추가 [!UICONTROL 환경 컨텍스트] 필드**&#x200B;를 추가하여 중요한 세부 정보를 캡처합니다.

- **Marketo**
   - Munchkin ID
- **Adobe Target**
   - 활동 이름
   - 사이트 URL(태그 속성 이름)/HAR 또는 Assurance 로그
- **Adobe Analytics**
   - RSID
   - 사이트 URL(태그 속성 이름)/HAR 또는 Assurance 로그/cURL/디버그 로그
   - Workspace 바로 가기 링크
- **Adobe Journey Optimizer(AJO)**
   - 여정 ID 또는 여정 URL
   - 프로필 예
- **Real-Time Customer Data Platform(RTCDP)**
   - 영향을 받는 구성 요소 ID(대상 ID, 프로필 ID, 대상 ID, 데이터 세트 ID 또는 데이터 흐름 ID)
   - HAR 파일/Assurance 로그
- **Customer Journey Analytics(CJA)**
   - Workspace 프로젝트
   - 태그 속성 이름


![새로 만들기](../adobe-support-tools-guide/assets/new.svg) 사례 만들기 흐름을 중단하지 않고 유용한 지침을 표시하기 위해 **AI 기반 [!UICONTROL 권장 사항 패널]**&#x200B;을 추가했습니다.

![새로 만들기](../adobe-support-tools-guide/assets/new.svg) 입력한 모든 정보를 통합적으로 볼 수 있도록 하고 사용자가 다음 작업을 수행할 수 있도록 하는 [!UICONTROL 검토 요약] 단계를 추가했습니다.

- 한 곳에서 사례 세부 정보 검토
- 편집하려면 이전 단계로 돌아가십시오.
- 진행률을 잃지 않고 요약으로 돌아가기

![수정](../adobe-support-tools-guide/assets/fix.svg) 대/소문자 설명 필드 이름이 *[!UICONTROL (으)로 바뀌었습니다. 명확성을 위해 문제를 설명&quot;]*&#x200B;하십시오.

![확인](../adobe-support-tools-guide/assets/fix.svg) 필수 필드 표시기로 별표(*)를 추가하여 완전성을 보장하고 제출 오류를 줄입니다.
