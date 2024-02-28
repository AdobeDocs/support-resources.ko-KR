---
title: 숨겨진 테스트 페이지
description: 이 페이지는 검색 및 TOC에서 숨겨짐
hide: true
hidefromtoc: true
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Premium 다운로드"
badgeExam: label="시험 ADO-E903" type="neutral"
source-git-commit: 0e4881c62b518866bd39d5c3f8eef0dc6063441b
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 94%

---

# 숨겨진 테스트 페이지

활성화됩니까? 오후 3시 10분 정도에 제출 여부를 다시 확인하십시오. 오후 3시 30분에 실시간 전송됩니까?

## 버튼

[단추 기본값](https://www.adobe.com/)

**[기본 단추](https://www.adobe.com/)**

_[단추 보조](https://www.adobe.com/)_

**_[단추 세 번째](https://www.adobe.com/)_**

## 미리보기 문제

다음 단락은 VSC 미리보기에서 제대로 렌더링되지 않습니다. 이유는 확실하지 않습니다.

[!DNL Adobe]에서 암호를 관리하는 경우, [Adobe 계정의 암호를 변경](https://helpx.adobe.com/kr/manage-account/using/change-or-reset-password.html){target="_blank"}할 수 있습니다.

## 메모 유형

지원되는 모든 메모 유형입니다.

>[!NOTE]
>
>표준 메모 블록입니다.

>[!TIP]
>
>표준 팁입니다.

>[!IMPORTANT]
>
>중요 메모입니다.

>[!WARNING]
>
>경고입니다.

>[!CAUTION]
>
>주의 사항입니다.

>[!ADMIN]
>
>ADMINISTRATION으로 렌더링되는 관리자 메모입니다. EXL 전용입니다.

>[!AVAILABILITY]
>
>가용성 메모입니다. EXL 전용입니다.

>[!PREREQUISITES]
>
>전제 조건 메모입니다. EXL 전용입니다.

>[!INFO]
>
>정보 메모입니다. EXL 전용입니다.

>[!ERROR]
>
>오류 메모입니다. EXL 전용입니다.

>[!SUCCESS]
>
>성공 메모입니다. EXL 전용입니다.

>[!MORELIKETHIS]
>
>* 1페이지
>* 2페이지

## 배지

배지는 콘텐츠 표시기로 사용되는 색상 레이블입니다. 예를 들어 배지를 추가하여 문서를 _Beta_&#x200B;로 또는 섹션을 _Premium_&#x200B;으로 표시할 수 있습니다. 배지 색상을 변경하고 URL과 도구 설명을 연결할 수 있습니다.

[!BADGE 배지 예]

두 가지 유형의 of 배지가 있으며 각각 다른 구문을 사용함:

* **메타데이터** - 페이지 상단 근처에 배지를 표시합니다.
* **인라인** - 구문이 있는 배지를 표시합니다.

### 메타데이터 배지

메타데이터에 배지 구문을 추가하면 문서의 페이지 제목(H1) 위에 배지가 배치됩니다.

예를 들면 _badge1_ 또는 _badge2_&#x200B;와 같이 배치 이름을 지정할 수 있습니다. 또는 보다 창의적인 작업을 수행할 수 있습니다(이름이 _배지_&#x200B;로 시작하는 경우).

메타데이터 예:

```
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
```

* **BadgePremium:** 이 예에서는 URL 및 도구 설명과 함께 Premium 배지가 표시됩니다.

* **BadgeExam:** 이 예에서는 시험 ID 번호와 함께 어두운 배지가 표시됩니다.

#### 인라인 배지

자체 줄이나 제목, 표 또는 기타 페이지 요소에 배지 정보를 지정합니다.

베타 레이블, 파란색, URL 및 도구 설명이 포함된 인라인 배지의 구문은 다음과 같습니다.

`[!BADGE Beta]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

### 사용 가능한 배지 색상

배지는 Adobe Spectrum에 정의된 색상을 사용함:

| 유형 | 배지 |
|---|---|
| 정보(기본) | [!BADGE Beta]{type=Informative url="https://www.example.com"} |
| 양수 | [!BADGE 새로운 기능]{type=Positive url=&quot;https://www.example.com&quot; tooltip=&quot;example.com으로 이동&quot;} |
| 음수 | [!BADGE 중단됨]{type=negative tooltip=&quot;이 기능은 이제 사용이 종료됩니다.&quot;} |
| 중립 | [!BADGE 아마도]{type=Neutral tooltip=&quot;라이더가 말에서 떨어졌습니다...&quot;} |
| 주의 사항 | [!BADGE 주의]{type=Caution tooltip=&quot;노란색 상태&quot;} |

구문 예

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off the horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

### 배지 요구 사항

* 메타데이터에는 배지 두 개만 허용됩니다. 이 규칙은 구성 가능하므로 예외가 필요한 경우 알려 주십시오.
* 배지 레이블만 필요합니다. `type`, `url` 및 `tooltip` 매개변수는 옵션입니다. `type` 매개변수는 색상을 결정합니다. `url` 매개변수를 사용하면 사용자가 배지를 클릭하여 문서나 페이지를 열 수 있습니다. `tooltip` 매개변수는 마우스를 올려놓으면 도구 설명 텍스트를 표시합니다.
* `TOC.md` 파일에 배지를 추가하면 안내서의 모든 문서에 배지가 표시됩니다. 배지에 대한 URL을 지정하여 문서로 이동하는 경우, 다른 폴더의 문서에 대한 계정의 상대 링크(예: `article.md`)가 아닌 루트 링크(예: `/help/guide/article.md`)를 사용해야 합니다.
* `metadata-new.md`에 배지를 추가하면 저장소의 모든 문서에 배지가 표시됩니다.
* 메타데이터 배지의 경우, 모든 값이 따옴표로 묶여 있는지 확인하십시오. 인라인 배지의 경우, `url` 및 `tooltip`이 따옴표로 묶여 있는지 확인하십시오.
* 유효한 유형 값으로는 *정보*(기본, 파란색), *양수*(녹색), *음수*(빨간색), *중립*(진한 회색) 및 *주의 사항*(노란색)이 있습니다.
* 배지 레이블이 현지화되었습니다.
* 여러 메타데이터 배지가 지정된 경우, `badge1:` 또는 `badgeWeb`과 같이 배지 이름을 기준으로 알파벳 순서로 배지가 표시됩니다.
* URL을 새 탭에서 열려면 다음 구문을 사용하십시오.

  ```
  [!BADGE Open in new tab]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Open adobe.com in new tab"}
  ```

  렌더링됨:

  [!BADGE 새 탭에서 열기]{type=Negative url="https://www.adobe.com newtab=true" tooltip="새 탭에서 adobe.com 열기"}

## 텍스트 강조 표시

Workfront 팀은 노란색 강조 표시를 사용하여 향후 기능의 미리보기를 표시할 수 있도록 요청했습니다. 작동 방식은 다음과 같습니다.

예 1:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

렌더링됨:

이 전체 단락은 강조 표시되어서는 안 됩니다. <span class="preview"> 강조 표시된 문장에서 이 단어는 **굴게** 표시됩니다.</span> 다음은 마지막 문장입니다.

예 2:

```
Highlighting should start after this paragraph.

<div class="preview">

Start of DIV.

This is a new paragraph, then an image

![image](/help/data-sheets/assets/BusinessSupportThumbnail.png)

Last highlighted item.

</div>

Not highlighted
```

렌더링됨:

강조 표시는 이 단락 뒤에서 시작되어야 합니다.

<div class="preview">

DIV의 시작입니다.

새로운 단락 다음 이미지입니다.

![이미지](/help/data-sheets/assets/BusinessSupportThumbnail.png)

마지막으로 강조 표시된 항목입니다.

</div>

강조 표시되지 않음

## 코드 블록의 구문 강조 표시

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
