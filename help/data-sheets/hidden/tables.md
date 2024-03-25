---
title: 표
description: Markdown 표 및 HTML 표 작업
hide: true
hidefromtoc: true
exl-id: 5ce746fc-6835-4bee-85c5-5ad5176baca0
source-git-commit: 6893d1e41c3899c3ab6a9b02b305161eb3f7e049
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 3%

---

# 표

매트가 여기 계속 있었어요

EDS

표준 Markdown에서는 기본 테이블만 지원합니다. AdobeDocs Markdown에는 다음과 같은 옵션이 있습니다.

* 기본 Markdown 표
* HTML 테이블
* 단락 나누기에 대한 HTML 구문이 제한된 Markdown 표(`<p>`), 줄 바꿈(`<br>`) 및 기본 목록(`<ul>`, `<ol>`).

## HTML 표를 Markdown 표로 변환

경우에 따라 HTML 테이블을 Markdown 테이블 또는 Markdown 텍스트로 변환할 수 있습니다. 모양을 개선하거나 유효성 검사 오류를 해결하거나 앞으로 더 쉽게 편집할 수 있도록 해야 할 수 있습니다.

안타깝게도 HTML 표를 잘 변환하는 단일 도구를 찾을 수 없었습니다. 우리는 보통 적절한 Markdown 표를 함께 깎아내기 위해 몇 가지 도구를 조합해서 사용한다.

| 도구 | 설명 |
|--- |--- |
| [Markdown 테이블 생성기](https://www.tablesgenerator.com/markdown_tables) | 처음부터 Markdown 표를 만드는 데 유용합니다. |
| [고급 테이블 변환기](https://tableconvert.com/html-to-markdown) | 표를 임의의 형식에서 임의의 형식으로 변환합니다. <p>**참고:** 변환하면 링크와 이미지가 병합됩니다. |
| [기본 테이블 html > markdown 변환기](https://jmalarcon.github.io/markdowntables/) | 단순 HTML 변환기 <p>**참고:** 변환하면 링크와 이미지가 병합됩니다. |
| [비테이블 HTML > Markdown 변환기](https://codebeautify.org/html-to-markdown) | HTML 테이블을 테이블이 아닌 Markdown 구문으로 변환합니다. 링크, 이미지 및 기타 병합된 항목을 복사하려면 위의 도구와 함께 사용하십시오. |

## 기본 Markdown 표

* 두 번째 행에는 표 속성을 결정하는 하이픈을 세 개 이상 추가해야 합니다. 예: `|--- |--- |--- |` 3열 테이블입니다.
* Markdown 테이블에는 하나 이상의 머리글 행과 본문 행이 있어야 합니다. 1행 또는 1셀 Markdown 표는 만들 수 없습니다(대신 HTML 사용).
* 각 행에 동일한 수의 파이프( &amp;vert; )가 있는지 확인합니다. 표 셀 내에 파이프 문자를 포함해야 하는 경우 해당 문자 앞에 백슬래시(`\|`) 또는 HTML 엔티티 코드 사용(`&vert;`).
* 표에서 코드 블록을 사용할 때는 주의하십시오. 인라인 코드 블록이 불균형적인 열 폭을 초래할 수 있습니다.
* 자동 또는 고정을 지정하여 테이블 렌더링 방법을 변경할 수 있습니다. 다음을 참조하십시오 [테이블 렌더링 방법 변경](#table-rendering).

## 보너스 HTML을 사용하여 Markdown 표 만들기

마이그레이션을 용이하게 하기 위해 HTML 단락 나누기(`<p>`), 줄 바꿈(`<br>`) 및 기본 HTML 목록(`<ul>` 및 `<ol>`) 내의 아무 곳에나 삽입할 수 있습니다.

**줄 바꿈과 목록이 있는 Markdown 표**

```
| Header 1 | Header 2 | Header 3 |
|--- |--- |--- |
| Normal row | row 1 column 2 | row 1 column 3 |
| Line break | first line in cell<br>second line in cell | row 1 column 3 |
| Bullet list | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul> | row 2 column 3 |
| Bullet list with line break | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul><br>This is a new line after the bullet list | row 2 column 3 |
```

**예**

| 머리글 1 | 머리글 2 | 머리글 3 |
|--- |--- |--- |
| 일반 행 | row 1 column 2 | row 1 column 3 |
| 줄 바꿈 | 셀의 첫 번째 라인<br>셀의 두 번째 라인 | row 1 column 3 |
| 글머리 기호 목록 | 글머리 기호 목록:<ul><li>항목 1</li><li>항목 2</li><li>항목 3</li></ul> | row 2 column 3 |
| 줄 바꿈이 있는 글머리 기호 목록 | 글머리 기호 목록:<ul><li>항목 1</li><li>항목 2</li><li>항목 3</li></ul><br>글머리 기호 목록 다음에 나오는 새 줄입니다. | row 2 column 3 |

>[!IMPORTANT]
>
>네이티브 테이블에서 HTML을 사용하려면 적절한 HTML 구문을 사용해야 합니다. HTML 구문에서 실수가 발생하면 이해하기 어려운 유효성 검사 오류가 발생합니다. 작업을 다시 확인하십시오.

## HTML 테이블 작업

마이그레이션 도구는 원래 표에서 가능한 한 많은 서식을 유지하려고 했습니다. 이 HTML 구문은 대부분 무시되지만 이 구문 중 일부는 유효성 검사 오류가 발생합니다.

**샘플 마이그레이션된 HTML 테이블**

```
<table> 
 <tbody>
  <tr>
   <th>Property</th> 
   <th>Type</th> 
   <th>Value Description</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i>(Required)</i> A multi-value string of badge images up to the number of badgingLevels. The badge image paths must be ordered so the first is awarded to the highest expert. If there are less badges than indicated by badgingLevels, the last badge in the array fills out the rest of the array. Example entry:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Long</td> 
   <td><i><p>(Optional)</i> Specifies the levels of expertise to be awarded. For example, if there should be an <code>expert </code>and an <code>almost expert</code> (two badges), then the value should be set to 2. The badgingLevel should correspond with the number of expert-related badge images listed for the badgingPath property. Default is 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>String</td> 
   <td><p><i>(Required)</i> Identifies the scoring engine as either "basic" or "advanced". Set to "advanced" else the default is "basic".</p></td> 
  </tr>
 </tbody>
</table>
```

**렌더링됨**

<table> 
 <tbody>
  <tr>
   <th>속성</th> 
   <th>유형</th> 
   <th>값 설명</th> 
  </tr>
  <tr>
   <td>배지 경로</td> 
   <td>String[]</td> 
   <td><p><i>(필수)</i> 배지 레벨 수까지 배지 이미지의 다중 값 문자열. 배지 이미지 경로의 순서를 지정해야 하므로 첫 번째 경로가 가장 높은 전문가에게 수여됩니다. 배지가 badgingLevels로 표시된 것보다 적으면 배열의 마지막 배지가 나머지 배열을 채웁니다. 예제 항목:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>배지 레벨</td> 
   <td>길게</td> 
   <td><p><i>(선택 사항)</i> 수여할 전문 지식 수준을 지정합니다. 예를 들어, <code>expert </code>및 <code>almost expert</code> (배지 2개), 그런 다음 값을 2로 설정해야 합니다. 배지 수준은 badgingPath 속성에 대해 나열된 전문가 관련 배지 이미지 수와 일치해야 합니다. 기본값은 1입니다.</p></td> 
  </tr>
  <tr>
   <td>배지 유형</td> 
   <td>문자열</td> 
   <td><p><i>(필수)</i> 채점 엔진을 "기본" 또는 "고급"으로 식별합니다. "고급"으로 설정하거나 기본값이 "기본"입니다.</p></td> 
  </tr>
 </tbody>
</table>

**HTML 테이블을 사용해야 하는 경우**

* 열 균형을 맞추기
* 테이블 헤더를 생략하려면 Markdown 테이블에 헤더 행이 있어야 합니다.
* 한 행 테이블의 테두리를 제거하려면(`<tr style="border: 0;">`).
* 열 또는 행 범위를 추가합니다.
* 표 셀 내에서 텍스트를 정렬합니다.

**HTML 테이블 작업에 대한 참고 사항**

* HTML 표에는 Markdown 구문을 사용하지 마십시오. 예를 들어 다음을 추가하는 경우 `[!NOTE]` HTML 테이블에 있는 그대로 렌더링됩니다.`[!NOTE]`). 대신, 메모 및 이미지와 같은 것에 대해 HTML 구문을 사용하십시오.

  페이지가 렌더링되기 전에 UICONTROL 및 DNL 태그가 제거되므로 Loc 태그는 이 규칙의 예외입니다.

* 일부 HTML 구문은 표에서 지원되지 않습니다. EXL로 렌더링할 때 너비, 높이, 색상 및 기타 HTML 구문 요소는 무시됩니다. 이러한 값이 유효성 검사 오류가 발생하지 않는 한 에 둘 수 있습니다.
* 텍스트를 정렬하려면 `align: "left|center|right"` HTML. 예를 들어 표 셀의 내용을 가운데로 정렬하려면 `<td align="center">`.
* HTML 테이블에는 중첩 테이블을 포함할 수 없습니다.

>[!TIP]
>
>1행 HTML 테이블에 대한 테두리를 해제하려면 다음 구문을 사용합니다.
>
>```
><table>
><tr style="border: 0;">
>```

## 테이블 렌더링 방법 지정 {#table-rendering}

다음 두 가지 방법으로 표를 렌더링할 수 있습니다.

* **고정** (현재 기본값) - 이미지가 있는 HTML 테이블을 포함하여 테이블을 렌더링하기 위한 사용자 지정 규칙을 포함합니다. 표는 스크롤하지 않고 전체 폭으로 렌더링되며, 이로 인해 텍스트가 겹치는 경우가 있습니다.
* **자동** - GFM(Git-flavored Markdown)과 유사합니다. 표는 스크롤할 수 있으므로 텍스트가 겹치지 않습니다.

대부분의 경우 표는 동일한 모양으로 렌더링됩니다. 그러나 테이블에 겹치는 텍스트가 포함되어 있으면 `auto` 태그에 가깝게 배치하십시오. 또는 이미지 카드가 있는 HTML 테이블이 제대로 렌더링되지 않는 경우 `fixed` 태그에 가깝게 배치하십시오.

기본값을에서 변경하는 것을 고려 중입니다. `fixed` 끝 `auto`.

## Markdown 표 편집

기본 Markdown 테이블이 렌더링되는 방법을 지정하려면 다음 구문 라인 중 하나를 테이블 뒤에 추가하고 앞 뒤에 빈 라인을 추가합니다.

* `{style="table-layout:auto"}`
* `{style="table-layout:fixed"}`

![테이블 렌더링](assets/table-render.png)

### HTML 테이블 편집

HTML 테이블이 렌더링되는 방법을 지정하려면 테이블의 첫 번째 행에 있는 다음 구문 라인 중 하나를 사용합니다.

* `<table style="table-layout:auto">`
* `<table style="table-layout:fixed">`

```
<table style="table-layout:fixed">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```

### 자동 또는 고정 사용 시기

**겹치는 텍스트**

사용 `auto` 긴 코드 블록 또는 텍스트가 있는 테이블에서 텍스트가 겹치는 경우 `fixed` (기본값)이 선택되어 있습니다.

*고정(기본값)*

| Insights 지표 | 설명 | ID 쿼리 매개 변수 |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | 한 데이터 세트 또는 모든 데이터 세트에 대해 잘못된 &quot;유형&quot; 메시지의 총 수입니다. | 데이터 세트 ID |
| **timeseries.data.collection.validation.category.range.count** | 하나의 데이터 세트 또는 모든 데이터 세트에 대해 잘못된 &quot;범위&quot; 메시지의 총 수입니다. | 데이터 세트 ID |
| **timeseries.data.collection.validation.category.format.count** | 하나의 데이터 세트 또는 모든 데이터 세트에 대해 잘못된 &quot;형식&quot; 메시지의 총 수입니다. | 데이터 세트 ID |
| **timeseries.data.collection.validation.category.pattern.count** | 한 데이터 세트 또는 모든 데이터 세트에 대해 잘못된 &quot;패턴&quot; 메시지의 총 수입니다. | 데이터 세트 ID |
| **timeseries.data.collection.validation.category.presence.count** | 한 데이터 세트 또는 모든 데이터 세트에 대해 잘못된 &quot;현재 상태&quot; 메시지의 총 수입니다. | 데이터 세트 ID |
| **timeseries.data.collection.validation.category.enum.count** | 하나의 데이터 세트 또는 모든 데이터 세트에 대해 잘못된 &quot;enum&quot; 메시지의 총 수입니다. | 데이터 세트 ID |

{style="table-layout:fixed"}

*자동*

| Insights 지표 | 설명 | ID 쿼리 매개 변수 |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | 한 데이터 세트 또는 모든 데이터 세트에 대해 잘못된 &quot;유형&quot; 메시지의 총 수입니다. | 데이터 세트 ID |
| **timeseries.data.collection.validation.category.range.count** | 하나의 데이터 세트 또는 모든 데이터 세트에 대해 잘못된 &quot;범위&quot; 메시지의 총 수입니다. | 데이터 세트 ID |
| **timeseries.data.collection.validation.category.format.count** | 하나의 데이터 세트 또는 모든 데이터 세트에 대해 잘못된 &quot;형식&quot; 메시지의 총 수입니다. | 데이터 세트 ID |
| **timeseries.data.collection.validation.category.pattern.count** | 한 데이터 세트 또는 모든 데이터 세트에 대해 잘못된 &quot;패턴&quot; 메시지의 총 수입니다. | 데이터 세트 ID |
| **timeseries.data.collection.validation.category.presence.count** | 한 데이터 세트 또는 모든 데이터 세트에 대해 잘못된 &quot;현재 상태&quot; 메시지의 총 수입니다. | 데이터 세트 ID |
| **timeseries.data.collection.validation.category.enum.count** | 하나의 데이터 세트 또는 모든 데이터 세트에 대해 잘못된 &quot;enum&quot; 메시지의 총 수입니다. | 데이터 세트 ID |

{style="table-layout:auto"}

**균형 잡힌 이미지가 있는 표 HTML**

사용 `fixed` 균형이 맞지 않는 균형잡힌 이미지가 필요한 HTML 테이블용 `auto` 이(가) 선택되어 있습니다. 이 예제에서 이미지의 크기는 같지만 중간 열에 더 많은 텍스트가 있습니다.

*자동*

<table style="table-layout:auto">
<tr>
  <td>
    <a href="note-test.md">
    <img alt="리드" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="note-test.md"><strong>Adobe 리드에 대한 워크플로</strong></a>
    </div>
    <em>리드 작성자를 위한 기본 편집 워크플로우입니다.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="드물게" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>자주 사용하지 않는 사용자를 위한 워크플로우</strong></a>
    </div>
    <em>주필이 아니라고요? 기여를 하는 가장 쉬운 방법에 대해 알아보십시오. 주필이 아니라고요? 기여를 하는 가장 쉬운 방법에 대해 알아보십시오. 주필이 아니라고요? 기여를 하는 가장 쉬운 방법에 대해 알아보십시오. 주필이 아니라고요? 기여를 하는 가장 쉬운 방법에 대해 알아보십시오. 주필이 아니라고요? 기여를 하는 가장 쉬운 방법에 대해 알아보십시오. 주필이 아니라고요? 기여를 하는 가장 쉬운 방법에 대해 알아보십시오.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="유효성 검사" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>유효성 검사</strong></a>
    </div>
    <em>유효성 검사 오류를 해결하는 방법에 대해 알아봅니다.</em>
    <br>
  </td>
</tr>
</table>

*수정됨 (여러 가지 방법으로)*

<table style="table-layout:fixed">
<tr>
  <td>
    <a href="note-test.md">
    <img alt="리드" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="note-test.md"><strong>Adobe 리드에 대한 워크플로</strong></a>
    </div>
    <em>리드 작성자를 위한 기본 편집 워크플로우입니다.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="드물게" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>자주 사용하지 않는 사용자를 위한 워크플로우</strong></a>
    </div>
    <em>주필이 아니라고요? 기여를 하는 가장 쉬운 방법에 대해 알아보십시오. 주필이 아니라고요? 기여를 하는 가장 쉬운 방법에 대해 알아보십시오. 주필이 아니라고요? 기여를 하는 가장 쉬운 방법에 대해 알아보십시오. 주필이 아니라고요? 기여를 하는 가장 쉬운 방법에 대해 알아보십시오. 주필이 아니라고요? 기여를 하는 가장 쉬운 방법에 대해 알아보십시오. 주필이 아니라고요? 기여를 하는 가장 쉬운 방법에 대해 알아보십시오.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="유효성 검사" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>유효성 검사</strong></a>
    </div>
    <em>유효성 검사 오류를 해결하는 방법에 대해 알아봅니다.</em>
    <br>
  </td>
</tr>
</table>
