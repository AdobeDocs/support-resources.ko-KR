---
title: Self Service Excellence 협업 설명서 구문 및 서식 안내서
description: Markdown 스타일링에 대한 기본 소개
mini-toc-levels: 1
hide: true
hidefromtoc: true
source-git-commit: 77a5127250ffbc9d490579188e8469d4c3dac4c3
workflow-type: tm+mt
source-wordcount: '4238'
ht-degree: 13%

---

# Markdown 구문 스타일 안내서

이 페이지에서는 Markdown(.md) 형식을 사용하여 디지털 경험 기술 설명서 작성을 위한 Markdown 구성 요소를 보여 줍니다. 이 페이지에는 Adobe 직원에 대한 세부 정보가 포함되어 있습니다.

EDS

자세한 내용은 여기 를 참조하십시오. [Adobe.com](https://www.adobe.com/kr/){rel=nofollow}

<!--
* You can [view a basic sample file](sample.md) or [view a sample file with advanced syntax examples](sample-full.md)
-->

>[!TIP]
>
>시청 [AdobeDocs Markdown 비디오](https://video.tv.adobe.com/v/26165).

대부분의 경우 텍스트 서식을 지정하는 표준 GFM(git-flavored markdown) 구문을 따릅니다. 그러나 일부 구문(예: 가로줄)은 지원되지 않으므로 설명서 요구 사항에 맞게 다양한 방법으로 Markdown을 확장했습니다.

## 기본 텍스트 서식

단락에는 Markdown으로 된 특별한 구문이 필요하지 않습니다. 각 단락 사이에 빈 줄을 추가합니다.

텍스트 서식을 다음으로 지정 **굵게**, 두 개의 별표로 묶습니다.

```
This text is **bold**.
```

텍스트 서식을 *기울임꼴*&#x200B;로 지정하려면 한 개의 별표로 묶습니다.

```
This text is *italic*.
```

텍스트 서식을 둘 다로 지정하려면 ***굵은 기울임꼴***, 3개의 별표로 묶습니다.

```
This is text is both ***bold and italic***.
```

Markdown 서식 문자를 무시하려면 `\` 문자 앞:

`This is not \*italicized\* type.`

렌더링됨: \*italicized\* 유형이 아닙니다.

## 배지

진행 중입니다. Loc를 기다리는 중입니다.

<!--

See the [dev version of this article](https://experienceleague-dev.corp.adobe.com/docs/authoring-guide-exl/using/markdown/syntax-style-guide.html#badges) for an example. Or [this one](https://experienceleague-dev.corp.adobe.com/docs/internal-test/test/badge.html).

There are two ways to create badges:

* **Metadata badge** - Specify the badge information in metadata so that the badge appears above the title in the article. This is especially useful for adding a badge to all articles in a guide or repo via the TOC.md or metadata.me files.
* **Inline badge** - Specify the badge information on its own line or in a heading, table, or other page element.

![badge examples](assets/badge-examples.png)

**Badge syntax**

*Metadata*: `badge: "Beta Content" type="Informative" url="https://www.example.com" tooltip="Go to example.com"`

*Inline*: `[!BADGE Beta Content]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

**Examples**

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

**Rendered**

|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|

**More details**

* Only the badge label is required. The `type`, `url`, and `tooltip` parameters are optional. The `type` parameter determines the color. The `url` parameter lets users click the badge to open an article. The `tooltip` parameter displays the tooltip text on mouseover.
* If you want multiple badges to appear at the top of the page, use different badge names. For example, you can create badge names such as `badgeBeta` or `badgeWeb`. Example:

  ```
  badge1: "Beta"
  badge2: "Campaign Web"
  ```

* For metadata badges, make sure that all values are wrapped in quotes. For inline badges, make sure that `url` and `tooltip` are wrapped in quotes.
* Valid type values include *Informative* (default, blue), *Positive* (green), *Negative* (red), *Neutral* (dark gray), and *Caution* (yellow). 

-->

## 블록 인용

작성 시스템에서는 blockquotes 구문(`>` 줄 시작 부분에서) 팁, 메모 및 비디오에 대한 사용자 지정 Markdown 확장을 식별합니다. 를 추가하여 실제 블록 따옴표를 만들 수 있습니다. `>` 단락 앞에 문자 표시

>이것은 큰 따옴표입니다.

```
>This is a blockquote quotation.
```

## 코드 블록(줄){#code-block}

**사용 시기**

문장에서 코드 일부를 인라인으로 렌더링하는 데 사용됩니다. 전체 펜싱된 코드 블록이 필요하지 않은 쿠키 이름, 파일 이름, 값 또는 명령을 호출하는 데 이상적입니다.

의 코드 블록 내에 있는 콘텐츠는 그대로 렌더링되고 현지화되지 않습니다. (이 규칙의 한 가지 예외는 다음과 같습니다. `!UICONTROL` 및 `!DNL` 구문: 게시를 위해 패키지하는 동안 제거됩니다.)

또한 유효성을 검사해서는 안 되는 샘플 URL에 대해 코드 블록을 사용합니다. `https://www.example.com`

**구문**

코드 블록은 단일 백틱을 사용하여 강조 표시할 코드 요소를 묶습니다.

```
This is `inline code` within a paragraph of text.
```

**예**

This is `inline code` within a paragraph of text.

>[!TIP]
>
>또한 텍스트를 삼중 백틱(&grave;&grave;&grave;)으로 둘러싸서 인라인 코드 블록을 만들 수도 있습니다. 이 기능은 인라인 코드 블록 내에서 백틱 문자를 참조해야 할 때 특히 유용합니다. 예:
>
&grave;&grave;&grave;`Use a back tick (`&grave;`) for formatting`&grave;&grave;&grave;

## 코드 블록(펜싱)

**사용 시기**

코드 블록을 사용하여 코드 구문을 표시합니다. 펜싱된 코드 블록은 삼중 백틱 을 사용하여 강조 표시할 코드 요소를 둘러쌉니다. 펜싱된 코드 블록의 위와 아래에 빈 줄을 추가합니다.

코드 블록은 현지화되지 않습니다.

>[!TIP]
>
펜싱된 코드 블록을 만들 때 언어를 지정합니다. 언어를 지정하면 해당 언어와 관련된 구문을 강조 표시하고 **복사** 단추입니다. 언어를 지정하는 경우 줄 번호를 표시할 수도 있습니다.

**구문**

코드 줄 앞과 뒤에 세 개의 백틱( &grave;&grave;&grave; )을 사용합니다. 열린 줄무늬와 닫힌 줄무늬가 같은 수의 공백으로 들여쓰도록 하십시오. 최적의 렌더링을 위해 코드 언어를 지정합니다.

&grave;&grave;&grave;`javascript`

**예**

```javascript
var visitor = Visitor.getInstance("INSERT-MARKETING-CLOUD-ORGANIZATION ID-HERE", {
     trackingServer: "INSERT-TRACKING-SERVER-HERE", // same as s.trackingServer
     trackingServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE", // same as s.trackingServerSecure

     // To enable CNAME support, add the following configuration variables
     // If you are not using CNAME, DO NOT include these variables
     marketingCloudServer: "INSERT-TRACKING-SERVER-HERE",
     marketingCloudServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE" // same as s.trackingServerSecure
});
```

### 코드 블록의 구문 강조 표시

Experience League는 코드 블록에 대한 구문 강조를 지원합니다. 구문이 제대로 강조 표시되도록 하려면 `java` 백틱 시작 세트 뒤에 언어를 지정해야 합니다. 유효한 언어 목록은 [https://prismjs.com](https://prismjs.com/#supported-languages)를 참조하십시오. 누락된 언어가 있으면 Jira 티켓을 기록하십시오.

### 코드 블록의 줄 번호 매기기

줄 번호 매기기를 활성화하려면 언어 뒤에 `{line-numbers="true"}`를 추가합니다.

줄 번호의 예(&grave;&grave;&grave;`html {line-numbers="true"}`):

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**줄에 번호 매기기 시작 _**

1이 아닌 숫자에서 번호 매기기를 시작하려면 줄 번호 구문 뒤에 `start-number="n"`을 추가합니다.

새로운 시작 줄의 예(&grave;&grave;&grave;`html {line-numbers="true" start-line="7"}`):

```html {line-numbers="true" start-line="7"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### 코드 블록의 줄 강조 표시

코드 블록 내의 행을 강조 표시하려면 행 번호 구문 뒤에 `highlight="n"`을 추가합니다. `11-13, 16`을 지정하면 11~13행과 16행이 강조 표시됩니다.

강조 표시된 줄의 예(&grave;&grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`):

```html {line-numbers="true" start-line="7" highlight="11-13, 16"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### 코드 블록의 변수 서식

변수 구문 예: `<i>italic</i>` 는 코드 블록에서 지원되지 않습니다. 가변 텍스트를 표시하려면 꺾쇠 괄호를 사용하는 옵션이 있습니다 `< >`.

## 축소 가능한 섹션

축소 가능한 섹션(또는 **어코디언**&#x200B;기본적으로 숨겨져 있는 ). 제목을 클릭하여 섹션을 확장하거나 축소할 수 있습니다.

접을 수 있는 텍스트를 사용하여 FAQ 페이지 간소화 또는 중첩된 목록으로 복잡한 절차 클러스터링과 같은 복잡한 콘텐츠를 단순화할 수 있습니다. 예를 들어 하위 단계 집합을 표시하는 대신 하위 단계를 &quot;세부 정보 보기&quot; 섹션으로 축소할 수 있습니다.

**구문**

```
+++See details
This is text inside a collapsible section.

* Bullet one
* Bullet two
* Bullet three

+++
```

**예**

+++자세한 내용 참조 축소 가능한 섹션 내의 텍스트입니다.

* 글머리 기호 1
* 글머리 기호 2
* 글머리 기호 3

+++

**참고**

* 축소 가능한 섹션 내에 축소 가능한 섹션을 중첩하지 마십시오. 중첩된 축소 가능 섹션은 올바르게 렌더링되지 않습니다. 하지만 유효성 검사가 실패하지 않으므로 사용자에게는 `+++` 중첩된 섹션의 구문
* 축소 가능한 섹션 내에 글머리 기호 목록 및 코드 블록과 같은 항목 위아래에 빈 줄을 추가해야 합니다. 그렇지 않으면 유효성 검사 오류가 발생합니다.
* 접을 수 있는 섹션 내에 제목을 추가할 수 있지만 권장되지는 않습니다.
* [데스크탑의 복잡한 콘텐츠에 아코디언이 항상 정답인 것은 아닙니다](https://www.nngroup.com/articles/accordions-complex-content/)
* 접을 수 있는 부분의 한 가지 역사적 단점은 다음과 같습니다. **페이지에서 찾기** (Ctrl/Cmd+F) 축소된 텍스트를 무시합니다. Safari에서는 여전히 적용되지만 Chrome에서는 더 이상 적용되지 않습니다. 페이지에서 찾기는 Chrome에서 축소된 텍스트를 검색합니다.
* 의 예 [유지 보수 업데이트](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=en) 축소 가능한 섹션을 사용하는 페이지입니다.

## 주석 및 비고

렌더링된 도움말 시스템에는 주석이 표시되지 않습니다. 주석을 사용하여 본인 또는 다른 작성자를 위한 메모를 남깁니다. 텍스트의 초안 섹션에 주석을 사용할 수도 있습니다.

주석의 경우, 도움말 시스템에서 렌더링되지 않지만 GitHub.com에서 Markdown 파일을 편집하는 사용자에게 표시됩니다. 주석에 기밀 정보를 포함하지 마십시오.

```
<!-- standard comment code -->

DO NOT USE the following:
<!--> bad comment syntax <-->
```

문서를 편집하지 않는 한 이 아래 텍스트(&quot;내가 표시되지 않음&quot;)를 볼 수 없습니다.

<!--
You can't see me (unless you're editing in Git).
-->

**미리 알림:** 주석(설명)은 공개 도움말 문서에는 표시되지 않습니다. 그러나 사용자가 보고 편집할 수 있는 공개 Markdown 파일에서는 주석이 표시됩니다.

>[!IMPORTANT]
>
블록 구성 요소(예: 글머리 기호 목록, 특히 중첩된 글머리 기호 목록) 내에 주석을 추가하지 마십시오. 주석은 글머리 기호 목록이 렌더링되는 방법을 변경할 수 있습니다.
>
TOC.md 파일에서 TOC 목록 가운데 있는 줄을 주석 처리하지 않습니다. 이렇게 하면 목차 목록이 손상되어 유효성 검사 오류가 발생할 수 있습니다. 대신 TOC의 주석을 파일의 끝으로 이동합니다.

## CONTEXTUALHELP

작성자는 제품 팀과 함께 작업하여 Experience Cloud 또는 Experience Platform 제품 UI에 도움말 팝오버를 추가할 수 있습니다. 예:

```markdown
>[!CONTEXTUALHELP]
>id="platform_destinations_activate_mandatorykey_4"
>title="About mandatory attributes"
>abstract="Select the XDM schema attributes that all exported profiles should include. Profiles without the mandatory key are not exported to the destination. Not selecting a mandatory key exports all qualified profiles regardless of their attributes."
>additional-url="http://www.adobe.com/go/destinations-mandatory-attributes-en" text="Learn more in documentation"
```

## 정의 목록

정의 목록의 경우 표준 Markdown 구문은 아직 지원되지 않습니다. 대신 다음과 같은 수동 서식을 사용합니다.

```
**Frog** - An amphibious green creature. Likes flies.
```

렌더링됨:

**개구리** 수륙양용 녹색 생물. 파리를 좋아해요

<!--
A definition list is a Markdown extension that supports the Definition List component in AEM. A definition list consists of a term and its definition.

**When to use**

Using a definition list is optional. To define lists of features or options, you can use either the definition list syntax or use basic Markdown formatting, such as applying bold to option names.

**Syntax**

```
Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
```

**Example**

Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
-->

## 파일 다운로드

.zip 또는 기타 다운로드 가능한 파일을 assets 디렉터리에 업로드한 다음 연결합니다. .zip 파일인 경우 링크를 클릭하면 파일이 다운로드됩니다. PDF 또는 PNG와 같은 파일 형식으로 브라우저에서 열 수 있는 경우, 링크를 클릭하면 새 탭이 열립니다. 이러한 파일의 경우 압축하거나 링크를 마우스 오른쪽 버튼으로 클릭하고 다운로드하는 지침을 제공하는 것이 좋습니다.

`Download` &amp;lbrack;`download-test.zip`&amp;rbrack;`(assets/download-test.zip)`

렌더링됨:

다운로드 [download-test.zip](assets/download-test.zip)

>[!NOTE]
>
다운로드 파일 및 이미지의 최대 파일 크기는 100MB입니다. github.com 제한 사항입니다. git.corp.adobe.com 제한은 더 높지만(250MB) 파일을 github.com 미러에 복사할 수 있어야 합니다.

## 제목 {#headings}

Markdown에서는 파운드 기호(`#`)을 클릭하여 제목 수준을 식별합니다. 첫 번째 수준(`#`)는 메타데이터 헤더에도 지정되는 문서 제목이며, 동일한 상태로 유지합니다. 두 번째 수준(`##`)는 mini-TOC에 포함될 페이지의 기본 제목을 나타냅니다. AEM(chl-author)로 작성하는 데 익숙한 경우 레벨 2 머리글(`##`) AEM의 &quot;제목 1&quot; 구성 요소에 매핑합니다.

제목의 최대 문자 수: 69자(영어) / 120자(LOC).

```
# This is level 1 (article title)

## This is level 2
   
### This is level 3
```

**제목 우수 사례**

* 수준 1 제목(`#`)는 각 문서의 메타데이터 뒤에 빈 줄을 따릅니다.
* 레벨 2에서 이동( )과 같은 레벨을 건너뛸 수 없습니다.`##`)에서 레벨 4(`####`).
* 빈 줄 포함 *다음 이전* 및 *이후* 각 제목.
* 머리글에 숫자가 포함된 경우, 다음과 같이 숫자로 시작하지 않는 명시적 머리말 ID를 지정합니다. `## Release notes for 2016 {#release-notes-2016}`.
* 3개의 제목 수준만 권장합니다. 레벨 4 이상은 현재 제대로 렌더링되지 않습니다.
* 머리글은 사용자가 클릭하여 섹션으로 이동할 수 있도록 오른쪽 탐색에 표시됩니다. 기본적으로 오른쪽 탐색에는 두 수준의 제목이 나타납니다. 레벨 수를 변경하려면 `mini-toc-levels` 다음과 같은 메타데이터 `mini-toc-levels: 3`.

**제목 ID**

제목 ID(ID라고도 함) *앵커 ID*)를 사용하여 문서 내의 섹션에 대한 사용자 지정 딥 링크를 만들 수 있습니다. 제목 ID를 지정하려면 다음 형식을 사용하십시오.

```
## Creating processing rules {#processing-rules}
```

제목 ID는 소문자로 하이픈을 넣어야 합니다.

제목에 제목 ID를 지정하지 않으면 기본 제목 ID는 &quot;슬러지화&quot;(소문자 및 하이픈 넣기) 제목입니다. 예를 들어 `## Creating widgets and Such` 제목에 `#creating-widgets-and-such` 앵커.

## HTML 구문 {#html}

보안 및 접근성을 포함한 다양한 이유로 Markdown에서 사용할 수 있는 HTML 구문을 제한합니다. 다음 목록은 지원되는 HTML 구문을 보여 줍니다. 이 목록에 없는 모든 HTML 구문은 유효성 검사 오류가 발생합니다.

```html
<table>
<tbody>
<td>
<tfoot>
<thead>
<th>
<tr>
<col>
<colgroup>
<p> (paragraph break)
<ul> (unordered list / numbered list)
<ol> (ordered list / bullet list)
<li> (list item)
<br> (line break)
<b>
<caption>
<i>
<strong> (bold)
<u> (underline)
<s> (strikethrough)
<span>
<sub> (subscript)
<sup> (superscript)
<a>
<img>
<div>
<em> (emphasis, italics)
<pre> (codeblock)
<code>
<codeblock>
```

<!--
Bob: Check above no space char. (ignore the space; I can't add a codeblock inside this codeblock)
-->

이 목록에 HTML 구문을 추가하려면 티켓을 기록하거나 SSE 팀에 문의하십시오.

## 이미지 {#images}

사용 `![]()` 이미지 구문 대괄호 `[ ]` 대체 텍스트 및 괄호 포함 `( )` 이미지 위치와 마우스로 가리키는 텍스트(선택 사항)(도구 설명)를 포함합니다. 느낌표는 이미지와 링크를 구별합니다.

```
![alt text](assets/logo.png "Hover text")
```

![대체 텍스트](assets/logo.png "가리킨 텍스트")

공유 이미지의 경우 이미지를 루트 자산 폴더에 배치한 다음 저장소 내의 모든 파일에서 작동하는 루트 링크를 사용할 수 있습니다.

```
/help/assets/imagename.png
```

### 이미지 크기 조정 및 정렬

**이미지 속성(오른쪽으로 정렬된 이미지 포함)** ![대체 텍스트](assets/premium.png "Premium 가리키기 텍스트"){align="right"}

다음과 같은 구문을 사용하여 기본 이미지 너비나 가운데를 변경하거나 페이지 보기나 테이블 셀 내에서 이미지를 오른쪽 정렬합니다.

```
![Dive image alt text](assets/maui-dive.jpg "Hover text - Maui dive width is 300 pixels and centered"){width="300" align="center"}
```

렌더링됨:

![다이브 이미지 대체 텍스트](assets/maui-dive.jpg "가리킨 텍스트 - Maui 잠수 너비는 300픽셀이며 가운데에 배치됩니다."){width="300" align="center"}

* 큰 이미지의 경우 페이지 너비(최소 640픽셀 너비)에 맞게 축소할 수 있을 만큼 큰 이미지를 만드는 것이 좋습니다. 권장 너비는 1500픽셀입니다. 2500픽셀 또는 500KB보다 큰 이미지를 만들 필요가 없습니다. 이미지의 최대 파일 크기는 100MB입니다.
* 작은 이미지의 경우 원하는 너비(픽셀 단위)를 사용하여 이미지를 생성하거나 다음과 같은 너비 매개 변수를 사용합니다. `{width="250"}` (픽셀) 또는 `{width="50%"}` (원본 이미지 크기가 아닌 보기 영역의 백분율). 이미지의 배율이 비례적으로 조절됩니다. 이미지의 크기를 늘리거나 줄일 수 있으므로 픽셀화에 주의하십시오.
* 경우에 따라, 더 넓은 이미지(예: 도구 모음)는 축소되고 좁은 이미지(예: 패널)는 축소되지 않으므로 동일한 인터페이스의 이미지가 페이지에서 비율이 다르게 보일 수 있습니다. 이러한 경우 시각적 일관성을 향상시키기 위해 더 넓은 이미지를 축소하는 것이 좋습니다.
* 보기 영역 내에서 이미지 정렬을 변경할 수 있습니다. 다음 중 하나를 사용하십시오. `{align="center"}` 또는 `{align="right"}`. 다음 `valign` 매개 변수는 지원되지 않습니다.

>[!NOTE]
>
이미지의 최대 파일 크기는 100MB입니다. github.com 제한 사항입니다. git.corp.adobe.com 제한은 더 높지만(250MB) 파일을 github.com 미러에 복사할 수 있어야 합니다.

### 이미지 링크

사용자가 이미지를 클릭하여 다른 페이지로 이동할 수 있도록 하려면 이 형식을 사용합니다.

**구문**

```
[![image](assets/core-services_96.png)](https://www.adobe.com)
```

**예**

Adobe 웹 사이트로 이동하려면 이 이미지를 클릭하십시오.

[![이미지](assets/core-services_96.png)](https://www.adobe.com/kr/)

<!--
### Click-to-zoom images

Use the `zoomable` parameter to allow users to click an image to view an enlarged version of the image. When the user mouses over a zoomable image, the pointer becomes a magnifying glass. When clicked, the image expands to the full width of the browser. It can be dismissed with a close button.

**Example**

![Diving image](/help/test-guide/assets/maui-dive.jpg "Diving in Maui"){width="100" zoomable="yes"}

**Syntax**

```
![Diving image](/help/test-guide/assets/maui-dive.jpg "Diving in Maui"){width="100" zoomable="yes"}
```

-->

## 링크 및 상호 참조 {#links-and-cross-references}

외부 링크는 정방향이며 연결된 캡션 또는 순수 URL로 렌더링할 수 있습니다.

```
[Adobe](https://www.adobe.com)
```

렌더링됨:

[Adobe](https://www.adobe.com/kr/)

텍스트에 URL을 직접 추가하는 경우 자동으로 링크로 변환되지 않습니다. URL을 링크로 표시하려면 을 추가합니다. `< >` 구문. 예:

```
https://www.adobe.com

<https://www.adobe.com>
```

렌더링됨:

https://www.adobe.com/kr/

<https://www.adobe.com>

문서(상호 참조)에 대한 링크는 약간 더 복잡할 수 있습니다.

**옵션 1: 표준 상대 링크**

표준 상대 링크의 모양은 다음과 같습니다.

```
See [Overview example article](collaborative-doc-instructions/overview.md)
```

경로 이름은 소스 파일과 대상 파일의 위치를 모두 고려해야 합니다. 다음과 같은 모든 상대 링크 피연산자를 사용할 수 있습니다. `./` (현재 디렉터리), `../` (하나의 디렉토리로 돌아가기) 및 `../../` (2개의 디렉터리로 돌아가기).

**옵션 2: 루트 상대 링크**

이 유형의 링크의 장점은 대상 파일만 고려해야 한다는 것입니다. 소스 파일 위치에 관계없이 저장소 내의 모든 소스 파일에서 작동합니다.

```
/help/using/docile-rules/introduction.md
```

**딥링크**

문서 내의 제목에 연결하려면 대상 제목에 명시적인 제목 ID(&quot;앵커 ID&quot;라고도 함)가 있어야 합니다. 예:

`## Creating audience segments {#creating-audience-segments}`

동일한 페이지 내에서 이 머리글에 연결하려면 머리글 ID를 링크로 사용합니다.

`See [Creating audience segments](#creating-audience-segments)`

리포지토리의 다른 문서에서 이 머리글에 연결하려면 링크 끝에 제목 ID 접미사를 추가하십시오.

`See [Audiences: Creating audience segments](audiences.md#creating-audience-segments)`

**새 탭에서 열기**

다른 안내서로 이동할 때와 같이 링크가 새 탭을 열도록 하려면 `{target="_blank"}` 링크의 속성입니다.

예:

`[See What's new](whats-new.md){target="_blank"}`

## 메타데이터

Markdown 파일의 맨 위에 메타데이터를 추가합니다. 메타데이터 줄 다음의 다음 줄(및 빈 줄)은 문서 제목(# 제목)이어야 합니다.

```
---
title: Title for search optimization
description: This is the article description used for search optimization. Use common search keywords and synonyms.
---

# Article title
```

## 로컬라이제이션 태그: UICONTROL, DNL 및 DONOTLOCALIZE

모든 Markdown 도움말 콘텐츠는 초기에 기계 번역을 사용하여 현지화됩니다. 도움말이 현지화되지 않은 경우 기계 번역을 유지합니다. 단, 도움말 콘텐츠가 과거에 현지화된 경우 기계 번역된 콘텐츠는 인간 번역 과정의 플레이스홀더로서 기능합니다.

## 다음과 같음

문서의 끝에 관련 링크를 표시하려면 &quot;다음과 같음&quot; 구성 요소를 사용하십시오. 렌더링되면 MORELIKETHIS 구성 요소가 &quot;관련 문서&quot;로 렌더링됩니다(및 다른 언어로 현지화됨).

**구문**

![비슷한 구문](assets/morelikethis.png)

**예**

>[!MORELIKETHIS]
>
* [Article 1](https://helpx.adobe.com/kr/support/analytics.html)
* [Article 2](https://helpx.adobe.com/kr/support/audience-manager.html)

## 메모 / 지침

Markdown을 확장하여 메모, 팁, 중요 및 경고와 같은 다양한 유형의 메모를 포맷했습니다.

**구문**

```
>[!NOTE]
>
>This is a standard NOTE block.
```

**예**

>[!NOTE]
>
표준 메모 블록입니다.

**구문**

```
>[!TIP]
>
>This is a standard tip.
```

**예**

>[!TIP]
>
표준 팁입니다.

**구문**

```
>[!WARNING]
>
>This is a standard warning block.
```

**예**

>[!WARNING]
>
표준 경고 블록입니다.

**구문**

```
>[!IMPORTANT]
>
>This is a standard important block.
```

**예**

>[!IMPORTANT]
>
이는 표준 중요 블록입니다.

**구문**

```
>[!NOTE]
>
>This is a standard NOTE block.
>
>It includes multiple paragraphs.
```

**예**

>[!NOTE]
>
표준 메모 블록입니다.
>
여기에는 여러 단락이 포함됩니다.

새로 지원되는 메모 유형:

>[!ADMIN]
>
관리자 노트입니다. EXL 전용입니다.

>[!AVAILABILITY]
>
가용성 메모입니다. EXL 전용입니다.

>[!PREREQUISITES]
>
전제 조건 메모입니다. EXL 전용입니다.

>[!INFO]
>
정보 메모입니다. EXL 전용입니다.

>[!ERROR]
>
오류 메모입니다. EXL 전용입니다.

>[!SUCCESS]
>
성공 메모입니다. EXL 전용입니다.

## 번호 매기기 목록 및 글머리 기호 목록 {#lists}

번호 매기기 목록을 만들려면 줄을 다음으로 시작하십시오. `1.` 또는 `1)`에서 한 가지 방법을 선택하고 문서 내에서 일관되게 사용하십시오. 번호를 지정할 필요는 없습니다. GitHub에서 자동으로 수행합니다.

번호 사용 `1` 번호 매기기 목록의 모든 단계에 대해.

목록 앞과 뒤에 빈 줄을 추가합니다.

**구문**

```
1. This is step 1.

1. This is the next step.

   1. This is a sub-step

   1. This is a sub-step

1. This is yet another step, the third.
```

**예**

1. This is step 1.

   1. 하위 단계

   1. 하위 단계

1. This is the next step.

1. This is yet another step, the third.

글머리 기호 목록을 만들려면 줄을 다음으로 시작하십시오. `*` 또는 `-` 또는 `+`에서 한 가지 방법을 선택하고 문서 내에서 일관되게 사용하십시오. (다음과 같은 형식을 혼합하는 경우 `*` 및 `+`를 설치한 후 파일을 체크 인하면 Markdown 유효성 검사 오류가 발생합니다.)

**모범 사례:** 사용 `*` 총알용. Visual Studio 코드에서는 글머리 기호에 별표를 적용하므로 별표를 사용하여 무순서 목록 만들기를 자동화할 수 있습니다. (TOC.md 파일은 더하기 기호를 사용한다는 것을 알 수 있습니다 `+` 목록. 그것은 이주로부터 얻은 유보물입니다. 모든 유효한 글머리 기호 문자는 문서 내에서 일관적이기만 하면 작동합니다.)

**구문**

```
* First item in an unordered list.
* Another item.
* Here we go again.
```

**예**

* First item in an unordered list.
* Another item.
* Here we go again.

목록 내에 목록을 포함하고 목록 항목 사이에 내용을 추가할 수도 있습니다. 목록 항목 사이의 내용을 들여써서 새 목록을 시작하지 않도록 하십시오. 단계 사이의 항목은 텍스트 시작 부분(번호 매기기 목록은 공백 3개, 글머리 기호 목록은 공백 2개)으로 들여써야 합니다.

```
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/core-services_96.png)
   
1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |
   
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.
   
1. Do another step.

   This is an indented line.
```

**예**

1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/core-services_96.png)

1. Make sure that your table looks like this:

   | Hello | World |
   |---|---|
   | How | are you? |

1. This is the fourth step.

   >[!NOTE]
   >
   This is note text.

1. Do another step.

   들여쓴 줄입니다.

참고: 3이 아닌 6개 공백과 같이 너무 많이 들여쓰면 해당 줄의 콘텐츠가 코드 블록으로 처리됩니다.

## 음영 상자

음영 상자는 페이지의 나머지 부분에서 콘텐츠 섹션을 설정하는 데 유용합니다. 예를 들어 Workfront 팀은 특정 목적을 달성하기 위해 텍스트, 이미지 및 코드 샘플이 포함된 &quot;예제&quot; 상자를 추가하려고 합니다. 음영 상자는 &quot;직접&quot; 또는 &quot;사용 사례&quot; 섹션이나 확장된 참고 사항이나 팁에도 유용할 수 있습니다.

음영 상자를 만들려면 다음을 추가합니다 `>[!BEGINSHADEBOX]` 섹션 시작 부분에서 `>[!ENDSHADEBOX]` 끝에 있습니다. 이러한 시작 태그와 끝 태그 사이의 모든 컨텐츠는 회색 배경을 갖습니다. 레이블 추가 `BEGINSHADEBOX` (예: `>[!BEGINSHADEBOX "Use Case]` 는 굵게 표시된 음영 상자 제목을 만드는 선택적 방법입니다. 다음 줄에 굵은 텍스트나 머리글을 추가할 수도 있습니다.

예:

>[!BEGINSHADEBOX]

**HTML 테이블에서 테두리 제거**

경우에 따라 HTML 표를 사용하여 균형 잡힌 디자인을 만들지만 콘텐츠가 표처럼 보이지 않게 할 수 있습니다. 1행 HTML 테이블에 대한 테두리를 해제하려면 다음 구문을 사용합니다.

```
<table>
<tr style="border: 0;">
```

>[!NOTE]
>
남용하지 마세요. 일반 표의 경우 콘텐츠 간에 일관된 디자인을 유지하려고 합니다.

![테이블 팁](assets/table-no-border.png)

3열 테이블에서 `<td align="center">` 및 `<td align="right">` 셀 내용을 보기 영역 전체에 고르게 분포시킵니다. 만약 그렇지 않았다면, 나는 너에게 말했을 것이다.

이것이 그늘막 상자의 마지막 줄입니다.

>[!ENDSHADEBOX]

## 코드 조각 및 포함

리포지토리의 문서 간에 텍스트를 공유하려면 `_includes` 폴더의 폴더 `help` 폴더를 삭제합니다. 이 `_includes` 폴더에는 리포지토리의 다른 파일에서 참조(포함)할 수 있는 .md 파일이 있을 수 있습니다. 또한 `snippets.md` 이 리포지토리의 파일에는 리포지토리의 모든 파일에서 참조할 수 있는 Head2 앵커를 포함할 수 있습니다.

snippets.md 파일의 H2 참조: `{{id-name}}`

파일 포함 참조: `{{$include /help/_includes/filename.md}}`

## 표

표는 Markdown에서 문제가 될 수 있습니다. 이전 작성 시스템에서 표를 마이그레이션하면 간단한 표(셀당 한 줄)는 기본 Markdown 표로 서식 지정됩니다(기본 설정). 더 많은 고급 표의 형식은 HTML 형식입니다.

>[!TIP]
>
시청 [Markdown 표 비디오](https://video.tv.adobe.com/v/26220)

네이티브 테이블은 Markdown에서 더 잘 보이는 경우가 많습니다. 열은 콘텐츠에 따라 크기가 조정됩니다. HTML 테이블은 동일한 너비의 열로 렌더링됩니다.

기본적으로 Markdown은 셀에서 여러 줄 또는 목록을 지원하지 않습니다. 그러나 셀에서 여러 줄을 허용하도록 Markdown 테이블이 확장되었습니다. `<p>` 또는 `<br>`) 또는 기본 목록(사용 `<ul><li>` 등).

>[!IMPORTANT]
>
이러한 HTML 코드를 Markdown 표에 추가할 때는 주의하십시오. 구문이 올바르지 않으면 문제를 정확하게 설명하지 않는 혼동 유효성 검사 오류가 발생합니다. HTML 구문을 검사하여 형식이 올바른지 확인합니다.

iframe, 셀 범위, 포함된 테이블과 같은 어떤 테이블에서도 허용되지 않습니다.

네이티브 Markdown 표(중첩된 목록 또는 복잡한 목록)에는 사용할 수 없습니다.

다음을 참조하십시오 [표](tables.md)

**구문**

```
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

**예**

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

간단한 표는 Markdown으로 적절히 작동합니다. 그러나 셀 내에 여러 단락이나 목록을 포함하는 표는 함께 사용하기 어렵습니다. 이러한 내용의 경우 제목 및 텍스트와 같이 서로 다른 형식을 사용하는 것이 좋습니다.

**단락 나누기 및 목록이 있는 Markdown 표**

```
| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | first paragraph in cell<p>second paragraph in cell(`<p>`)<br>line break (`br`) | row 1 column 3 |
| row 2 | bullet list<ul><li>item 1</li><li>item 2</li><li>item 3</li></ul> | row 2 column 3 |
```

**예**

| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | 셀의 첫 번째 단락<p>셀의 두 번째 단락(`<p>`)<br>줄 바꿈(`br`) | row 1 column 3 |
| row 2 | 글머리 기호 목록<ul><li>항목 1</li><li>항목 2</li><li>항목 3</li></ul> | row 2 column 3 |

**줄 바꿈과 가짜 목록이 있는 Markdown 표**

수동 글머리 기호를 사용한 해결 방법

```
| Color | Things to Do |
|--- |--- |
| Red | * Read <br> * Write <br> * Study |
| Blue | * Swim <br> * Run <br> * Lift <br> **Note**: Remember to train smart.|
```

**예**

| 색상 | 할 일 |
|--- |--- |
| 빨간색 | * 읽기 <br> * 쓰기 <br> * 연구 |
| 파란색 | 수영 <br> * 실행 <br> * 상승도 <br> **참고**: 현명하게 훈련해야 합니다. |
.32


## 탭

탭은 서로 다른 콘텐츠를 표시하는 섹션 상단의 클릭 가능한 영역입니다. 탭을 클릭하면 탭의 내용이 표시되고 다른 탭의 내용은 숨겨집니다.

탭 집합을 만들려면 다음을 추가하십시오. `>[!BEGINTABS]` 탭 집합 시작 부분에서 `>[!ENDTABS]` 마지막 탭 뒤에. 추가 `>[!TAB <tab title>]` 각 탭 섹션에 태그를 추가하고 그 아래에 각 탭의 내용을 추가합니다.

**탭 구문**

```
>[!BEGINTABS]

>[!TAB iOS]

This content appears in the iOS tab.

>[!TAB Android]

This content appears in the Android tab.

>[!TAB Windows]

This content appears in the Windows tab.

>[!TAB MacOS]

This content appears in the MacOS tab.

>[!TAB Linux]

This content appears in the Linux tab.

>[!ENDTABS]
```

**렌더링됨**

>[!BEGINTABS]

>[!TAB iOS]

이 콘텐츠는 iOS 탭에 표시됩니다.

>[!TAB Android]

이 콘텐츠는 Android 탭에 표시됩니다.

>[!TAB Windows]

이 콘텐츠는 Windows 탭에 나타납니다.

>[!TAB MacOS]

이 콘텐츠는 MacOS 탭에 표시됩니다.

>[!TAB 리눅스]

이 콘텐츠는 Linux 탭에 나타납니다.

>[!ENDTABS]

**탭 메모**

* 사용자는 페이지 내 검색(Ctrl+F/Cmd+F)을 사용하여 표시되지 않는 탭 내에서 콘텐츠를 찾을 수 없습니다.
* 탭 제목이 사용자 브라우저의 페이지 보기 너비를 초과할 경우 가로 스크롤 막대가 나타납니다.
* 탭 제목은 서식을 지정할 수 없습니다. 추가하는 모든 구문은 제목의 일부로 전달됩니다. 예를 들어, `>[!TAB **iOS**]` 다음과같이 표시됩니다. `**iOS**`.
* 한 페이지에 여러 개의 탭 세트를 만들 수는 있지만 한 탭 세트를 다른 탭 세트 내에 중첩할 수는 없습니다.
* 음영 처리된 배경이 탭 세트에 적용되어 사용자가 탭 콘텐츠를 다른 콘텐츠와 구별할 수 있습니다.

## 텍스트 강조 표시

Workfront 팀은 노란색 강조 표시를 사용하여 향후 기능의 미리보기를 표시할 수 있도록 요청했습니다. 작동 방식은 다음과 같습니다.

예:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

렌더링됨:

이 전체 단락은 강조 표시되어서는 안 됩니다. <span class="preview"> 강조 표시된 문장에서 이 단어는 **굴게** 표시됩니다.</span> 다음은 마지막 문장입니다.

일반적으로 를 사용합니다. `<span class="preview">` 단락이나 단락 내의 텍스트를 강조 표시하고 `<div class="preview">` 여러 단락 및 구성 요소에 사용할 수 있습니다.

>[!NOTE]
>
메모 및 표와 같은 특정 페이지 요소의 강조 표시를 개선하는 작업이 아직 진행 중입니다. 부적절한 렌더링이 표시되면 언제든지 JIRA 버그를 기록할 수 있습니다. 진행 중입니다.
>
VSC 미리 보기는 아직 강조 표시를 지원하지 않습니다.

## 비디오

비디오는 기본적으로 Markdown으로 렌더링되지 않습니다. 비디오 인라인을 표시하려면 구성 요소 표시기를 사용하십시오 `[!VIDEO]` url을 클릭합니다.

**구문**

```
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

**예**

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

## 추가 Markdown 구문 정보

### 확장된 Markdown 구성 요소

일반적인 Markdown에 포함되지 않은 항목을 지원하려면 Markdown을 확장해야 합니다.

특수 구성 요소는 대괄호와 느낌표와 블록 유형에 대한 참조를 사용하여 포함된 블록 인용으로 선언됩니다. 예를 들어 메모를 선언하는 방법은 다음과 같습니다.

```
>[!NOTE]
>
>This is a note.
```

* 메모, 중요, 팁, 주의 및 경고를 포함한 메모(경고)
* 포함된 비디오
* 비슷한 항목 더 보기(관련 문서)
* 현지화를 위한 다양한 UI 태그
* 제목, 이미지 및 코드 블록에 대한 구성 요소 속성
* 축소 가능한 섹션
* 텍스트 강조 표시
* 페이지 탭

Markdown 블록 따옴표 사용( `>` )를 클릭하여 메모와 같은 단락 기반 구성 요소를 함께 연결합니다. 미리보기를 개선하려면 섹션의 시작 바로 뒤에 블록 따옴표 기호(`>`). 섹션을 종료하려면 빈 줄을 추가합니다.

구성 요소 내에 하위 구성 요소를 사용해야 하는 경우 추가 블록 따옴표(`>  >`)을 클릭하여 제품에서 사용할 수 있습니다. 예를 들어 DONOTLOCALIZE 섹션 내의 NOTE는 `>  >`.

경우에 따라 제목과 같은 Markdown 요소에 대한 특정 설정을 지원해야 합니다. 기본 설정을 변경해야 하는 경우 프랑스식 중괄호로 매개 변수를 추가합니다 `{# }` 구성 요소 뒤에.

### 빈 줄

빈 줄이 있는 텍스트 벽에 숨쉴 공간을 추가할 수 있습니다. 사용 `<br>&nbsp;` 를 해결 방법으로 사용하여 빈 줄을 추가합니다.

예: 이것은 정말 긴 텍스트가 될 수 있는 첫 번째 문장입니다. 이 단락과 다음 단락 사이에 빈 줄을 삽입하겠습니다.

<br> 

이 기능은 여기에서 그다지 인상적이지 않을 수 있지만, 페이지가 너무 복잡하다고 생각되면 빈 행을 사용해 보십시오.

### &quot;이스케이프&quot;할 문자 {#characters-to-escape}

여러 문자(`# { } [ ] < > * + - . !`)는 Markdown이나 HTML에서 제목, 이미지, 목록 및 기타 구성 요소를 만드는 특별한 의미를 갖습니다. 이러한 문자를 사용하면 렌더링 엔진은 사용자가 코드를 추가하고 있다고 생각합니다. 그러나 경우에 따라 텍스트에 이러한 문자를 표시할 수 있습니다. 그러려면 문자를 &quot;이스케이프&quot;해야 합니다. 가장 쉬운 이스케이프 메서드는 문자 앞에 백슬래시(`\`). 예를 들어 `#` 문자로 해석되지 않도록 문자를 입력하면 `\#`:

`\# This is not a heading`

**렌더링됨:**

\# 제목이 아닙니다.

백슬래시는 다음 문자로만 작동합니다. `# { } [ ] * + - . !`. 꺾쇠 괄호와 같은 문자를 이스케이프 처리해야 하는 경우 `<yourname>`)를 사용하면 텍스트를 백틱으로 묶어 인라인 코드 블록을 적용하거나 문자 대신 HTML 엔티티 코드를 사용할 수 있습니다. 일반적인 HTML 코드의 예:

* `&lt;` (&lt;)
* `&gt;` (>)
* `&amp;` (&amp;)
* `&Hat;` (^)
* `&mdash;` (—)
* `&ndash;` (-)

HTML 엔티티의 전체 목록은 [Freeformatter 웹 사이트](https://www.freeformatter.com/html-entities.html). 이렇게 하면 모든 특수 문자를 조회할 수 있습니다.

>[!NOTE]
>
&quot;파일 선택 > 다른 이름으로 저장&quot;과 같은 체인 단계의 경우 `>` 다른 문자 옆에 있지 않아서 문자입니다. 변수: `<filename>` 두 코드 블록 중 하나를 사용하여 꺾쇠 괄호를 이스케이프합니다. `backticks` 또는 문자 코드(`&lt;filename&gt;`).

코드 블록에서 HTML 엔티티를 사용하는 경우 엔티티 텍스트가 특수 문자로 변환되지 않습니다. 예를 들어, `&gt;` 코드 블록에 &quot;&quot;로 표시됨 `&gt;` &quot;>&quot; 대신&quot;을 클릭합니다.

역따옴표( &grave; )를 이스케이프 처리하려면 다음을 사용합니다. `&grave;` 또는 인라인 코드 블록을 감싸는 트리플 백 틱 내에 백 틱 을 삽입합니다.

### 지원되지 않는 항목

지원하지 않을 예정인 몇 가지 Git 맛보기 Markdown 항목이 있습니다. 사용하는 미리보기 도구를 통해 이러한 기능 중 일부를 사용할 수 있지만 사용하지 마십시오.

**작업 목록**

지원되지 않음

```
* [x] Set up Jersey Shore recording
* [x] Buy donuts with sprinkles
* [x] Take nap
* [ ] Wash ferret
```

**이모지**

지원되지 않음

```
:bowtie:
```

**가로 규칙**

지원되지 않음

```
***
```

**블록 인용**

우리는 블록 따옴표 (`>` 참고 사항 및 비디오와 같은 확장된 Markdown 구문을 나타내는 ( 줄의 시작 부분에서) 다음에 설명되어 있습니다. 하지만 다음을 사용할 수도 있습니다. `>` 블록 인용 섹션을 만드는 구문입니다.

>[!NOTE]
>
세 개가 아닌 여섯 개 공백과 같이 너무 많이 들여쓰면 내용이 블록 따옴표로 렌더링됩니다. 콘텐츠를 실수로 블록 인용으로 렌더링하지 않으려면 적절한 들여쓰기 양을 사용합니다.
