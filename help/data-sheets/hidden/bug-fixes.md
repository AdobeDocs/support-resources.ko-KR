---
title: 버그 수정(숨김)
description: 내부 테스트용 테스트 페이지
hide: true
hidefromtoc: true
source-git-commit: 57c0a39d3b2dcb50259ee285b1a61f8ad4db12ea
workflow-type: tm+mt
source-wordcount: '1817'
ht-degree: 28%

---

# 버그 수정

## UGP-10584 인라인 배지가 작동하지 않음

이 배지는 글머리 기호 항목과 동일한 줄에 있어야 합니다.

* [[!DNL Mixpanel]](note-test.md) [!BADGE 메모]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE 표]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE 구문 스타일 안내서]{type=Positive}

## UGP-10560 - 접을 수 있는 섹션의 배지

+++ 이전 버전

### V1.16 릴리스

_2023년 2월 13일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 제품 비디오는 이제 카탈로그 서비스 API에서 지원됩니다.
![수정](assets/package.png) 이제 고정 가격이 적용된 번들 제품이 지원됩니다.
![수정](assets/package.png) 이제 품절 옵션이 PDP 위젯에 표시됩니다.

#### 알려진 제한 사항

다음 기능은 아직 지원되지 않습니다.

* 동적 특성 페이로드의 최대 크기는 9MB입니다.
* 그룹 제품 가격. 간단한 제품 가격으로 계산할 수 있습니다.
* 이미지 배열에서는 첫 번째 이미지만 역할을 포함합니다.

API Mesh 및 Core GraphQL API를 사용하면 다음 제한 사항을 해결할 수 있습니다.

* 최소 광고 가격
* [계층 가격](https://www.adobe.com/kr/)

### V1.13 릴리스

_2023년 10월 12일 금요일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 카탈로그 서비스가 다음을 지원합니다. `inStock` 제품 변형에 대한 플래그.
![신규](assets/package.png) `urlKey` 및 `externalId` GraphQL 스키마에 추가되었습니다.
![신규](assets/package.png) 이제 다운로드 가능한 제품 및 기프트 카드가 지원됩니다.

### V1.12 릴리스

_2023년 9월 19일 수요일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](https://www.adobe.com/kr/).
![수정](assets/package.png) 이 릴리스에는 서비스 측의 버그 수정 및 개선 사항이 포함되어 있습니다.

### V1.11 릴리스

_2023년 7월 18일 수요일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 카탈로그 서비스가 이제 다음을 지원합니다. [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) Recommendations 제품에 대한 GraphQL 쿼리.

### V1.10 릴리스

_2023년 6월 27일 수요일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 이제 카탈로그 서비스 API가 &quot;관련 제품&quot;을 지원합니다.

### V1.7 릴리스

_2023년 4월 12일 목요일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 이제 카탈로그 서비스가 삭제된 제품 변형을 정리합니다.
![수정](assets/package.png) 인프라 확장성 및 성능 향상

### V1.6 릴리스

_2023년 3월 28일 수요일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 에 견본이 추가되었습니다. [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) 쿼리.
![신규](https://www.adobe.com/kr/).

### V1.5 릴리스

_2023년 3월 6일 화요일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 추가됨 [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) GraphQL 기능.
![수정](assets/package.png) 향상된 성능 및 API 확장성.

### V1.4 릴리스

_2023년 2월 7일 수요일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 설치 단계를 간소화하기 위한 카탈로그 서비스 메타패키지가 게시되었습니다.
![수정](assets/package.png) API 확장성 및 성능 개선.

### V1.3 릴리스

_2023년 1월 17일 수요일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 온보딩 경험을 단순화하고 개선했습니다.
![신규](assets/package.png) 새 고객 샌드박스 엔드포인트는 사전 프로덕션 테스트에 사용할 수 있습니다.
![신규](assets/package.png) 가상 제품에 대한 지원이 추가되었습니다.
![수정](assets/package.png) API 확장성 및 성능 개선.

### V1.1 릴리스

_2022년 11월 18일 토요일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 카탈로그 서비스가 이제 Adobe의 [API 메쉬](https://developer.adobe.com/graphql-mesh-gateway/).
![수정](assets/package.png) API 확장성과 전반적인 성능이 개선되었습니다.

### V1.0 릴리스

_2022년 10월 4일 수요일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 이제 번들 및 그룹화된 제품을 지원합니다.
![신규](assets/package.png) B2B 가시성 재정의가 추가되었습니다. 이제 제품을 검색할 수 있으며 특정 고객 그룹을 위해 장바구니에 추가할 수 있습니다.
![수정](assets/package.png) 이제 서비스가 보다 안정적이고 성능이 향상되었습니다.

### 0.3 릴리스 - Beta+

_2022년 9월 12일 화요일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 변형 이미지 지원: 제품 이미지는 선택한 옵션에 따라 반환됩니다
![신규](assets/package.png) 가격 지원에 대한 역할: 특정 고객 그룹의 구성원만 제품 가격을 볼 수 있도록 허용
![수정](assets/package.png) 서비스의 안정성 및 성능 향상
![신규](assets/package.png) 카탈로그에서 제품이 삭제되면 업데이트가 수신됨

### 베타 릴리스

_2022년 8월 9일_

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](assets/package.png) 다음 `products` 및 `refineProduct` 쿼리는 다음 데이터를 반환합니다.

* 사전 정의된(시스템) 제품 속성.
* 동적 제품 속성을 확인하고 역할별로 필터링합니다(제품 표시 페이지/제품 목록 페이지).
* 제품 옵션.
* 제품 이미지를 만들고 역할(PDP/PLP)별로 필터링합니다.
* 간단한 제품에 대한 특정 가격 및 구성 가능한 제품에 대한 가격 범위입니다.
* 고객 그룹 가격 및 가격 범위. 고객 그룹이 없는 쇼핑객에 대해 대체 기본 가격을 반환합니다.
* B2B 고객별 가격을 사용하는 제품 유형입니다.

+++

## UGP-10565 - 텍스트 강조 표시

다음 앞에 텍스트 `<div class="preview">`

<div class="preview">

### Workfront 기본 필드 추가

사용자 정의 양식에 Workfront 기본 필드를 추가할 수 있습니다. 사용자 정의 양식을 오브젝트에 첨부하면 필드가 오브젝트 데이터에서 채워집니다. 예를 들어 프로젝트에 첨부된 사용자 정의 양식의 설명 필드는 프로젝트 설명을 가져옵니다. (데이터가 없는 경우 필드에 &quot;N/A&quot;가 표시될 수 있습니다.)

1. 화면 왼쪽에서 **기본 필드** 캔버스의 섹션으로 드래그합니다.
1. 화면 오른쪽에서 사용자 정의 필드에 대한 옵션을 구성합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">레이블</td> 
      <td> <p>(필수) 필드 위에 표시할 설명 레이블을 입력합니다. 언제든지 레이블을 변경할 수 있습니다.</p> <p><b>중요 사항</b>: 이 레이블에는 특수 문자를 사용하지 마십시오. 보고서에 올바로 표시되지 않습니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">이름</td> 
      <td> <p>(필수) 이 이름은 시스템이 필드를 식별하는 방법입니다.</p><p> 필드를 처음 구성할 때 레이블을 입력하면 이름 필드가 자동으로 채워집니다. 그러나 레이블 및 이름 필드는 동기화되지 않으므로 시스템에서 볼 수 있는 이름을 변경하지 않고도 사용자가 볼 수 있는 레이블을 자유롭게 변경할 수 있습니다.</p>
      <p><b>중요 사항</b>:
      <ul> 
      <li>그렇게 할 수도 있지만 본인이나 다른 사용자가 Workfront에서 사용자 정의 양식을 사용하기 시작한 후에는 이 이름을 변경하지 않는 것이 좋습니다. 이 필드를 사용하면 시스템은 이제 Workfront의 다른 영역에서 참조될 수 있는 필드를 더 이상 인식하지 못합니다.</p> </li>
      <li> <p>각 필드 이름은 조직의 Workfront 인스턴스에서 고유해야 합니다. 이렇게 하면 다른 사용자 정의 양식에 대해 이미 만들어진 파일을 다시 사용할 수 있습니다.</p> </li>
      <li><p>Workfront의 다른 영역에서 필드를 사용할 때 오류를 방지하려면 사용자 지정 필드 이름에 마침표/점 문자를 사용하지 않는 것이 좋습니다.</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">지침</td> 
      <td> <p>필드에 대한 추가 정보를 입력합니다. 사용자가 사용자 정의 양식을 작성할 때 물음표 아이콘 위로 마우스를 가져가 여기에 입력하는 정보가 포함된 도구 설명을 볼 수 있습니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">참조 필드</td> 
      <td><p>(필수) Workfront 기본 필드를 선택합니다.<p><p>양식 개체에 대한 네이티브 필드만 사용할 수 있습니다. 예를 들어 양식 디자이너 상단의 개체 유형 목록에 프로젝트가 표시되면 프로젝트에 대한 기본 필드는 선택할 수 있지만 작업에만 해당하는 필드는 선택할 수 없습니다.</p></td>
     </tr>
     <tr> 
      <td role="rowheader">크기</td> 
      <td>(선택 사항) 필요에 따라 필드의 표시 크기를 변경합니다.</td> 
     </tr> 
    </tbody> 
   </table>

1. 변경 사항을 저장하려면 를 클릭합니다. **적용** 양식을 계속 작성하려면 다른 섹션으로 이동하십시오.

   또는

   **저장 후 닫기**&#x200B;를 클릭합니다.

</div>

강조 표시 후 텍스트

## UGP-10566 - 링크 텍스트가 HTML 테이블의 일반 텍스트보다 작음

UGP-9780 참조

<table style="table-layout:auto"> 
<tbody> 
<tr>
<td>에 입력</td>
<td>설명</td>
<td>다음에 사용 가능: </td>
</tr>
<tr> 
    <td role="rowheader">레이블</td> 
    <td> <p>(필수) 사용자 정의 필드 위에 표시할 설명 레이블을 입력합니다. 언제든지 레이블을 변경할 수 있습니다. 자세한 내용은 <a href="https://www.adobe.com/kr/" class="MCXref xref">사용자 정의 양식에 사용자 정의 필드 추가</a> 이 문서에서.</p> <p><b>중요 사항</b>: 이 레이블에는 특수 문자를 사용하지 마십시오. 보고서에 올바로 표시되지 않습니다.</p> </td> 
    <td>
    <ul>
    <li>라디오 단추. 자세한 내용은 <a href="https://www.adobe.com/kr/">사용자 정의 양식에 사용자 정의 필드 추가</a> 이 문서에서. (클래스 없음)</li>
    <li>확인란 그룹</li>
    <li>드롭다운</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 - 이전 버그

메모(및 목록)에서 &quot;span&quot; 태그가 제대로 작동하지 않습니다.

새 댓글 달기 환경에서 사용할 수 있는 기능과 개체에 대한 자세한 내용은 [새 댓글 달기 환경](note-test.md).

1. 회신을 추가할 객체로 이동합니다.
1. 클릭 **업데이트**&#x200B;을(를) 클릭하고 **댓글** 개체 탭과 회신할 댓글 또는 회신을 찾습니다.

   또는

   <span class="preview">다음을 클릭합니다. **모두** 탭을 클릭한 다음 를 클릭합니다 **댓글로 회신** 를 클릭하여 댓글 탭에서 댓글을 열고 회신합니다. 모두 탭에서 회신할 수 없습니다.</span>

1. (선택 사항) 회신에 이전 업데이트의 텍스트를 포함하려면 **자세히** 회신할 댓글의 오른쪽 위 모서리에 있는 메뉴를 클릭한 다음 **견적 회신**. 이전 업데이트의 텍스트가 입력 영역에 세로로 회색 선으로 표시됩니다.
1. 클릭 **답변**.

   ![](assets/package.png)

   대화에 적극적으로 참여하는 사용자를 아래 부분에서 확인할 수 있습니다 **회신 추가...** 상자를 선택하면 더 이상 관련이 없는 항목을 추가하거나 제거할 수 있습니다. 이러한 사용자는 오브젝트에 가입된 사용자와 함께 오브젝트에 대한 업데이트 또는 회신이 이루어질 때마다 알림을 받습니다. 더 많은 사용자에 태그를 지정하여 회신에 추가할 수도 있습니다.  더 많은 사용자에 태그를 지정하려면 다음을 참조하십시오. [업데이트에 다른 사용자 태그 지정](note-test.md).

   >[!TIP]
   >
   >   기존 회신에 추가 회신을 추가하려면 **회신 추가...** 상자 또는 클릭 **답변** 원래 주석에. 답변은 스레드 끝에 추가됩니다.

1. 답글 입력을 시작하고 리치 텍스트 도구 모음에서 추가 옵션을 사용하십시오. 리치 텍스트 또는 기타 업데이트 기능 사용에 대한 자세한 내용은 [작업 업데이트](note-test.md).

1. 클릭 **제출** 회신을 저장합니다.

1. (선택 사항) **자세히** 회신을 관리할 추가 옵션을 보려면 회신할 댓글의 오른쪽 상단 모서리에 있는 메뉴를 참조하십시오. 자세한 내용은 [작업 업데이트](note-test.md).


## UGP-10614 - 이미지가 있는 문제 테이블

내 생각엔 `{width="20"}` 매개 변수로 인해 테이블에 문제가 발생합니다.

## Expert 및 Ultimate Success 플랜 비교

|  | Expert Success 플랜 | Ultimate Success 플랜 |
|--- |--- |--- |
|  | Expert Success 플랜을 사용하면 중요한 비즈니스 문제에 대한 기술 문제 해결 및 지침을 위해 **연중무휴 전문가 지원**&#x200B;을 이용할 수 있습니다. 또는 셀프 가이드 리소스, 전용 모범 사례, Adobe 전문가 및 동료의 온라인 커뮤니티를 활용하여 빠른 해결 방법을 찾을 수도 있습니다. <p> *모든 Adobe Experience Cloud 라이선스에 포함되어 있습니다.* | Ultimate Success 플랜을 통해 **전략적 지침과 사전 예방적 기술 상태를 경험하여 고성능 디지털 경험을 제공**&#x200B;할 수 있습니다. Adobe 환경은 귀사의 비즈니스를 잘 알고 비즈니스 영향에 대한 목표와 우선 순위에 맞는 로드맵 실행에 중점을 두는 전문가 팀의 지원을 받게 됩니다. |
| **성공 팀** | 지원 엔지니어로 구성된 팀 | 다음 포함 <ul><li> 지정된 기술 계정 관리자 </li><li> 지정된 고객 성공 관리자 </li><li> 지정된 지원 서비스 관리자</li><li> 성공 가속기를 제공하는 기술 엔지니어 및 전략 전문가로 구성된 팀 </li><li> 지원 엔지니어로 구성된 팀 </li></ul> |
| **사전 예방적 기술 + 운영 지원** | ![포함되지 않음 아이콘](../assets/Cross_red_circle.svg){width="20"} 포함되지 않음 | 다음 포함 <ul><li>업그레이드 및 마이그레이션 검토, 릴리스 준비 </li><li>제품 로드맵 검토</li><li> 기술 및 전략 로드맵 조정</li><li>주요 이벤트 준비 및 계획</li><li>적합하고 시기적절한 지원 계획</li><li>기술 모범 사례 및 업계 지침</li><li>제품 팀 지원/조정</li><li>주요 비즈니스 목표 달성을 위한 통합 계획 - MAP(Mutual Action Plan)</li></ul> |
| **기술 지원** | 다음 포함 <ul><li>**P1**: 24x7 문제 지원</li><li>**P2, P3, P4**: 업무 시간 지원</li><li>표준 중단 관리</li><li>풀링된 에스컬레이션 관리</li></ul> | 다음 포함 <ul><li>**P1**: 24x7 문제 지원</li><li>**P2/P3**: 주중 24시간 문제 지원</li><li>**P4**: 업무 시간 지원</li><li>우선 중단 관리</li><li>지정된 전문가 에스컬레이션 관리</li></ul> |
| **성공 가속기** | ![포함되지 않음 아이콘](../assets/Cross_red_circle.svg){width="20"} 포함되지 않음 | TAM 및 CSM이 정기적으로 예약하는 성공 가속기<p>*(자세한 내용은 성공 가속기 카탈로그 참조)* |
| **지원 채널** | 온라인, 전화, Experience League, 포럼 | 개인화된 온라인 포털, 우선 전화, Experience League, 포럼 |

{style="table-layout:fixed"}

## 추가 기능 지원

| 추가 기능 | Expert Success 플랜 | Ultimate Success 플랜 |
|--- |--- |--- |
| **이벤트 관리 추가 기능**<br>&#x200B;주요 이벤트의 전체 라이프사이클을 관리하는 데 필요한 엔드 투 엔드 리더십 및 지원을 제공합니다. | ![사용 가능한 아이콘](../assets/Plus_blue.svg){width="20"} 사용 가능 | ![사용 가능한 아이콘](../assets/Plus_blue.svg){width="20"} 사용 가능 |
| **기술 계정 디렉터 추가 기능**<br>&#x200B;비즈니스 성과를 극대화하기 위해 리더십 감독을 제공하고, 경영진 참여를 주도하며, 거버넌스를 보장하는 리드 기술 리소스 | ![사용 불가 아이콘](../assets/Cross_red_circle.svg){width="20"} 사용 불가 | ![사용 가능한 아이콘](../assets/Plus_blue.svg){width="20"} 사용 가능 |
| **고급 클라우드 지원 추가 기능**<br> Adobe Experience Manager as a Cloud Service 고객에게 최고 수준의 관리 및 가치 보증을 제공합니다. | ![사용 가능한 아이콘](../assets/Plus_blue.svg){width="20"} 사용 가능 | ![사용 가능한 아이콘](../assets/Plus_blue.svg){width="20"} 사용 가능 |
| **Mentor Sessions 추가 기능**<br>&#x200B;적시 교육 방식으로 기술 기반의 학습 과정을 제공합니다. | ![사용 가능한 아이콘](../assets/Plus_blue.svg){width="20"} 사용 가능 | ![사용 가능한 아이콘](../assets/green_checkmark.svg){width="20"} 포함됨 |
| **Developer Boost 추가 기능**<br>&#x200B;파손 수리 작업을 지원할 수 있는 필드 엔지니어링 전문가에 대한 액세스를 제공합니다. | ![사용 가능한 아이콘](../assets/Plus_blue.svg){width="20"} 사용 가능 | ![포함된 아이콘](../assets/green_checkmark.svg){width="20"} 포함됨 |
| **우선 순위 대기열 번들 추가 기능**<br> Mentor Sessions 및 Developer Boost에 대한 추가 액세스 권한으로 티켓을 먼저 처리하려면 줄을 건너뛰십시오. | ![사용 가능한 아이콘](../assets/Plus_blue.svg){width="20"} 사용 가능 | ![포함된 아이콘](../assets/green_checkmark.svg){width="20"} 포함됨 |

{style="table-layout:fixed"}
