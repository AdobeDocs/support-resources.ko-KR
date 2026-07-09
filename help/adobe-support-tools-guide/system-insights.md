---
title: 시스템 통찰력
description: 시스템 인사이트는 Adobe Commerce 환경에서 발생할 수 있는 문제를 사전에 식별합니다. 사례 생성 중 통찰력을 검토하면 해결 시간을 줄이고, 중단을 방지하고, 안정적이고 안전한 배포를 지원합니다.
autotag-review: '2026-07-06T16:24:45.881Z'
TQID: 'https://experienceleague.adobe.com/jSV4V0a4G9gPqbFSURQSP2ctdKob7eu71JB7am0ZwSo'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: ada6c0ec0c6814e3176d3b6c953455be019bc703
workflow-type: tm+mt
source-wordcount: 738
ht-degree: 1%

---

# 시스템 통찰력

System Insights는 Adobe 제품 설정에서 성능, 보안 및 기능에 걸쳐 잠재적인 문제를 식별하는 데 도움이 되는 사전 예방 결과를 제공합니다. 이러한 통찰력은 API, New Relic 및 [!DNL Splunk]을(를) 포함한 관찰 가능성 도구에서 수집된 원격 분석 데이터를 기반으로 성능 저하, 보안 취약성 또는 잘못된 구성과 같은 위험을 표시합니다.

시스템 인사이트는 사례 생성 프로세스 중에 표시되며 진단 및 해결 시간을 단축하는 데 도움이 됩니다.

## 시스템 인사이트 생성 방법

Adobe 팀은 일반적인 지원 문제와 새로운 트렌드를 지속적으로 분석합니다. 이러한 결과를 기반으로 Adobe은 시스템에 자동화된 검사를 추가합니다.

이러한 검사는 제품 설정을 검사하여 구성 오류, 작업 중단 또는 기능 문제 또는 시스템 중단을 초래할 수 있는 상태와 같은 문제를 감지합니다.

검사를 통해 Adobe 제품 및 지원 팀에서 정의한 안전 범위 밖의 값이나 상태를 식별하면 시스템이 이를 시스템 Insight으로 표시합니다.

## 시스템 통찰력이 중요한 이유

시스템 통찰력을 정기적으로 검토하면 시스템 안정성이나 고객 경험에 영향을 미치기 전에 문제를 조기에 식별하는 데 도움이 됩니다. 이 사전 예방적 접근 방식은 다음과 같습니다.

- 플랫폼 신뢰성 향상
- 다운타임 감소
- Adobe 권장 모범 사례를 유지 관리하는 데 도움이 됩니다.

## 가용성 및 범위

시스템 인사이트는 현재 Adobe Commerce에만 사용할 수 있습니다. 이러한 통찰력은 Experience League 지원에서 사례 만들기 프로세스 중에 나타나며 [사이트 전체 분석 도구(SWAT)](https://experienceleague.adobe.com/ko/docs/commerce-operations/tools/site-wide-analysis-tool/intro)를 통해서도 사용할 수 있습니다.

>[ !Note]
>
>시스템 인사이트는 프로덕션 환경에 대한 데이터만 표시합니다.

## 시스템 통찰력 액세스

시스템 인사이트는 서비스 케이스 만들기 워크플로우 전체에 나타납니다. 문제 세부 정보를 입력하면 화면 오른쪽의 AI 기반 권장 사항 섹션 아래에 **[!UICONTROL 시스템 인사이트]** 패널이 나타납니다. AI 기반 권장 사항에 대한 자세한 내용은 Adobe 고객 지원 경험 문서에서 [지원 티켓 작성](https://experienceleague.adobe.com/ko/docs/support-resources/adobe-support-tools-guide/adobe-customer-support-experience#fill-out-the-support-ticket)을 참조하십시오.

패널에는 특정 프로젝트 인스턴스의 범위가 지정되는 인사이트의 스크롤할 수 있는 목록이 표시됩니다. 범위 지정은 **[!UICONTROL 프로젝트 URL]** 필드에 입력한 정보를 기반으로 합니다. 인사이트가 올바른 환경을 반영하도록 하려면 **[!UICONTROL 프로젝트 URL]**&#x200B;을(를) 정확하게 입력하십시오.

패널이 로드되면 사용자 환경에 대해 플래그가 지정된 insight 카드의 스크롤 가능한 목록이 표시됩니다. 각 insight 카드에는 다음이 포함됩니다.

- 문제를 요약하는 제목입니다
- insight에 대한 간략한 설명

![지원 리소스에 액세스](/help/adobe-support-tools-guide/assets/access-support-resources.png)

전체 insight 세부 사항을 보려면 목록에서 insight 카드를 선택하십시오. 상세 보기는 다음 정보를 제공합니다.

- Insight 이름
- insight에 플래그가 지정된 Adobe 제품
- 다음과 같이 분류된 insight 유형:
   - [!UICONTROL 기능]
   - [!UICONTROL 성능]
   - [!UICONTROL 보안]
- 심각도를 나타내는 [!UICONTROL 위험 수준]
- [!UICONTROL 마지막 확인 실행]은 검색 결과가 검색된 시기를 나타냅니다.
- [!UICONTROL Insight Source], 사이트 전체 분석 도구(SWAT) 제공
- 문제 및 잠재적 영향에 대한 자세한 설명과 함께 문제를 조사하고 해결하기 위해 실행 가능한 단계입니다. 상세 보기는 또한 이 유형의 문제의 일반적인 원인을 설명하고 추가 참조를 위해 관련 Adobe 설명서에 대한 링크를 포함합니다.

![대소문자 확인](/help/adobe-support-tools-guide/assets/click-case-card.png)

insight에서 직접 문제가 발생할 수 있으므로 진행하기 전에 패널에서 모든 통찰력을 검토하십시오.

## insight에서 작업 수행

insight을 검토한 후 다음 작업 중 하나를 선택합니다.

### 사례 만들기 계속

문제가 지속되거나 추가 지원이 필요한 경우 **[!UICONTROL 사례 만들기 계속]**&#x200B;을 선택하세요. 이전에 입력한 사례 정보가 모두 유지됩니다.

### 문제를 해결됨으로 표시

insight에서 문제가 해결되고 지원 사례가 더 이상 필요하지 않으면 **[!UICONTROL 해결된 문제]**&#x200B;를 선택하십시오.

이 옵션을 선택한 경우:

- 확인 대화 상자가 나타납니다.
- 이 대화 상자는 입력한 모든 사례 데이터가 영구적으로 지워짐을 나타냅니다.

insight의 ![작업](/help/adobe-support-tools-guide/assets/issue-resolved.png)

**[!UICONTROL 완료]**&#x200B;를 선택하여 확인하고 **[!UICONTROL 내 사례]** 페이지로 돌아갑니다. insight 세부 사항 보기로 돌아가려면 **[!UICONTROL 취소]**&#x200B;를 선택하십시오.

![대/소문자 양식 지우기](/help/adobe-support-tools-guide/assets/clear-case-form.png)

## insight에 대한 피드백 제공

각 insight 세부 사항 보기의 하단에서 insight이 유용했는지 여부에 대한 피드백을 제공할 수 있습니다. 이 피드백은 Adobe이 시스템 인사이트의 관련성과 정확성을 지속적으로 개선하는 데 도움이 됩니다.

![피드백 제공](/help/adobe-support-tools-guide/assets/submit-feedback.png)

피드백을 제공하려면 다음 작업을 수행하십시오.

1. insight 세부 사항 보기를 엽니다.
2. 패널 하단으로 스크롤합니다.
3. **[!UICONTROL 프롬프트를 찾습니다. 유용했습니까? 피드백을 보냅니다.]**
4. 다음 옵션 중 하나를 선택합니다.
   - insight이 유용한 경우 **엄지손가락 위로** 아이콘
   - insight이 유용하지 않은 경우 **아래로** 아이콘
5. (선택 사항) 추가 설명을 입력합니다.
6. 피드백을 보내려면 **[!UICONTROL 제출]**&#x200B;을 선택하고, 제출하지 않고 피드백 섹션을 닫으려면 **[!UICONTROL 취소]**&#x200B;를 선택하십시오.
