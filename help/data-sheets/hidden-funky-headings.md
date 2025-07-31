---
title: 태그 라이브러리
description: Granite, CQ 및 Sling 태그 라이브러리를 사용하면 템플릿 및 구성 요소의 JSP 스크립트에 사용할 특정 기능에 액세스할 수 있습니다
contentOwner: Guillaume Carlino
products: SG_EXPERIENCEMANAGER/6.5/SITES
topic-tags: platform
content-type: reference
solution: Experience Manager, Experience Manager Sites
hide: true
hidefromtoc: true
role: Developer
exl-id: d024b7e9-1e8e-4aa3-bbb8-7bc92d143a1f
source-git-commit: 3f2ed618aa8e5d738315a0ff114551c183761a7d
workflow-type: tm+mt
source-wordcount: '2458'
ht-degree: 0%

---

# 태그 라이브러리{#tag-libraries}

Granite, CQ 및 Sling 태그 라이브러리를 사용하면 템플릿 및 구성 요소의 JSP 스크립트에 사용할 특정 기능에 액세스할 수 있습니다.

## **굵은 머리글**

이것은 위의 굵은 제목입니다.

2025년 7월 30일 목요일

## *기울임꼴 머리글*

이것은 위의 기울임꼴 제목입니다.

## Granite 태그 라이브러리 {#granite-tag-library}

Granite 태그 라이브러리에는 유용한 기능이 포함되어 있습니다.

Granite UI 구성 요소의 jsp 스크립트를 개발할 때 스크립트 상단에 다음 코드를 포함하는 것이 좋습니다.

```xml
<%@include file="/libs/granite/ui/global.jsp"%>
```

전역 도 Sling 라이브러리를 선언합니다.

```xml
<%@taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling" %>
```

### &lt;ui:includeClientLib> {#ui-includeclientlib}

`<ui:includeClientLib>` 태그에는 js, css 또는 테마 라이브러리일 수 있는 AEM html 클라이언트 라이브러리가 포함되어 있습니다. 다른 유형의 여러 포함(예: js 및 css)의 경우, 이 태그는 jsp에서 여러 번 사용해야 합니다. 이 태그는 ` [com.adobe.granite.ui.clientlibs.HtmlLibraryManager](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/javadoc/com/adobe/granite/ui/clientlibs/HtmlLibraryManager.html)` 서비스 인터페이스의 편리한 래퍼입니다.

여기에는 다음과 같은 속성이 있습니다.

**categories** - 쉼표로 구분된 클라이언트 라이브러리 범주 목록입니다. 여기에는 해당 카테고리의 모든 JavaScript 및 CSS 라이브러리가 포함됩니다. 요청에서 테마 이름이 추출됩니다.

해당 값: `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeIncludes`

**테마** - 쉼표로 구분된 클라이언트 라이브러리 범주 목록입니다. 지정된 카테고리에 대한 모든 테마 관련 라이브러리(CSS 및 JS 모두)가 여기에 포함됩니다. 요청에서 테마 이름이 추출됩니다.

해당 값: `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeThemeInclude`

**js** - 쉼표로 구분된 클라이언트 라이브러리 범주의 목록입니다. 여기에는 해당 카테고리의 모든 JavaScript 라이브러리가 포함됩니다.

해당 값: `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeJsInclude`

**css** - 쉼표로 구분된 클라이언트 라이브러리 범주의 목록입니다. 여기에는 해당 카테고리의 모든 CSS 라이브러리가 포함됩니다.

해당 값: `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeCssInclude`

**테마** - 테마 또는 테마가 아닌 라이브러리만 표시하는 플래그를 포함해야 합니다. 생략하면 두 세트가 모두 포함됩니다. 순수 JS 또는 CSS에만 적용됩니다(범주 또는 테마 포함에 대해서는 해당되지 않음).

`<ui:includeClientLib>` 태그는 jsp에서 다음과 같이 사용할 수 있습니다.

```xml
<%-- all: js + theme (theme-js + css) --%>
<ui:includeClientLib categories="cq.wcm.edit" />

<%-- only js libs --%>
<ui:includeClientLib js="cq.collab.calendar, cq.security" />

<%-- theme only (theme-js + css) --%>
<ui:includeClientLib theme="cq.collab.calendar, cq.security" />

<%-- css only --%>
<ui:includeClientLib css="cq.collab.calendar, cq.security" />
```

## CQ 태그 라이브러리 {#cq-tag-library}

CQ 태그 라이브러리에는 유용한 기능이 포함되어 있습니다.

스크립트에서 CQ 태그 라이브러리를 사용하려면 스크립트는 다음 코드로 시작해야 합니다.

```xml
<%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %>
```

>[!NOTE]
>
>`/libs/foundation/global.jsp` 파일이 스크립트에 포함되어 있으면 taglib이 자동으로 선언됩니다.

AEM 구성 요소의 jsp 스크립트를 개발할 때 스크립트 상단에 다음 코드를 포함하는 것이 좋습니다.

```xml
<%@include file="/libs/foundation/global.jsp"%>
```

sling, CQ 및 jstl taglibs를 선언하고 [`<cq:defineObjects />`](#amp-lt-cq-defineobjects) 태그에 정의된 규칙적으로 사용되는 스크립팅 개체를 노출합니다. 이렇게 하면 구성 요소의 jsp 코드가 단축되고 간소화됩니다.

### &lt;cq:text> {#cq-text}

`<cq:text>` 태그는 JSP에서 구성 요소 텍스트를 출력하는 편의 태그입니다.

여기에는 다음과 같은 선택적 속성이 있습니다.

**property** - 사용할 속성의 이름입니다. 이름은 현재 리소스를 기준으로 합니다.

**값** - 출력에 사용할 값입니다. 이 속성이 있으면 속성 속성 사용을 덮어씁니다.

**oldValue** - 비교 출력에 사용할 값입니다. 이 속성이 있으면 속성 속성 사용을 덮어씁니다.

**escapeXml** - 결과 문자열의 문자 &lt;, >, &amp;, &#39; 및 &quot;를 해당 문자 엔티티 코드로 변환할지 여부를 정의합니다. 기본값은 false입니다. 이스케이프는 선택적 형식 다음에 적용됩니다.

**format** - 텍스트 서식을 지정하는 데 사용할 선택적 java.text.Format.

**noDiff** - diff 정보가 있어도 diff 출력을 계산하지 않습니다.

**tagClass** - 비어 있지 않은 출력을 둘러싸는 요소의 CSS 클래스 이름입니다. 비어 있으면 요소가 추가되지 않습니다.

**tagName** - 비어 있지 않은 출력을 둘러싸는 요소의 이름입니다. 기본값은 DIV입니다.

**자리 표시자** - 편집 모드에서 null 또는 빈 텍스트에 사용할 기본값, 즉 자리 표시자입니다. 기본 검사는 선택적 서식 지정 및 이스케이프 후에 수행됩니다. 즉, 출력에 있는 그대로 기록됩니다. 기본값은 다음과 같습니다.

`<div><span class="cq-text-placeholder">&para;</span></div>`

**기본값** - null 또는 빈 텍스트에 사용할 기본값입니다. 기본 검사는 선택적 서식 지정 및 이스케이프 후 수행됩니다. 즉, 출력에 있는 그대로 기록됩니다.

JSP에서 `<cq:text>` 태그를 사용하는 방법에 대한 몇 가지 예는 다음과 같습니다.

```xml
<cq:text property="jcr:title" tagName="h2"/>
<cq:text property="jcr:description" tagName="p"/>

<cq:text value="<%= listItem.getTitle() %>" tagName="h4" placeholder="" />
<cq:text value="<%= listItem.getDescription() %>" tagName="p" placeholder=""/>

<cq:text property="jcr:title" value="<%= title %>" tagName="h3"/><%
    } else if (type.equals("link")) {
        %><cq:text property="jcr:title" value="<%= "\u00bb " + title %>" tagName="p" tagClass="link"/><%
    } else if (type.equals("extralarge")) {
        %><cq:text property="jcr:title" value="<%= title %>" tagName="h1"/><%
    } else {
        %><cq:text property="jcr:title" value="<%= title %>" tagName="h2"/><%

<cq:text property="jcr:description" placeholder="" tagName="small"/>

<cq:text property="tableData"
               escapeXml="false"
               placeholder="<img src=\"/libs/cq/ui/resources/0.gif\" class=\"cq-table-placeholder\" alt=\"\">"
    />

<cq:text property="text"/>

<cq:text property="image/jcr:description" placeholder="" tagName="small"/>
<cq:text property="text" tagClass="text"/>
```

### &lt;cq:setContentBundle> {#cq-setcontentbundle}

`<cq:setContentBundle>` 태그는 i18n 지역화 컨텍스트를 만들어 `javax.servlet.jsp.jstl.fmt.localizationContext` 구성 변수에 저장합니다.

여기에는 다음과 같은 속성이 있습니다.

**language** - 리소스 번들을 검색할 로케일의 언어입니다.

**source** - 로케일을 사용해야 하는 소스입니다. 다음 값 중 하나로 설정할 수 있습니다.

* **static** - 가능한 경우 `language` 특성에서 로케일을 사용하고 그렇지 않은 경우 서버 기본 로케일에서 사용합니다.

* **페이지** - 로케일은 현재 페이지 또는 리소스의 언어(사용 가능한 경우)에서 가져왔으며, `language` 특성(사용 가능한 경우)에서 가져왔으며, 그렇지 않은 경우 서버 기본 로케일에서 가져왔습니다.

* **요청** - 로케일은 요청 로케일(`request.getLocale()`)에서 가져옵니다.

* **auto** - 가능한 경우 `language` 특성에서 로케일을 사용하고, 가능한 경우 현재 페이지 또는 리소스의 언어에서 로케일을 사용하고, 그렇지 않은 경우 요청에서 사용합니다.

`source` 특성이 설정되지 않은 경우:

* `language` 특성이 설정된 경우 `source` 특성은 기본적으로 &quot;`static`&quot;(으)로 설정됩니다.

* `language` 특성이 설정되지 않은 경우 `source` 특성은 기본적으로 `auto`(으)로 설정됩니다.

표준 JSTL `<fmt:message>` 태그에서 &quot;콘텐츠 번들&quot;을 사용할 수 있습니다. 키별 메시지 조회는 두 배입니다.

1. 먼저 렌더링되는 기본 리소스의 JCR 속성을 번역에 대해 검색합니다. 간단한 구성 요소 대화 상자를 정의하여 해당 값을 편집할 수 있습니다.
1. 노드에 키와 정확히 같은 이름의 속성이 없는 경우 대체 항목은 슬링 요청(`SlingHttpServletRequest.getResourceBundle(Locale)`)에서 리소스 번들을 로드하는 것입니다. 이 번들의 언어 또는 로케일은 `<cq:setContentBundle>` 태그의 언어 및 원본 특성으로 정의됩니다.

`<cq:setContentBundle>` 태그는 jsp에서 다음과 같이 사용할 수 있습니다.

언어를 정의하는 페이지의 경우:

```xml
... %><cq:setContentBundle source="page"/><%  %>
<div class="error"><fmt:message key="Hello"/>
</div> ...
```

사용자 맞춤형 페이지의 경우:

```xml
... %><cq:setContentBundle scope="request"/><% %>
<div class="error"><fmt:message key="Hello"/>
</div> ...
```

### &lt;cq:include> {#cq-include}

`<cq:include>` 태그에 현재 페이지에 대한 리소스가 포함되어 있습니다.

여기에는 다음과 같은 속성이 있습니다.

**플러시**

* 대상을 포함하기 전에 출력을 플러시할지 여부를 정의하는 부울.

**경로**

* 현재 요청 처리에 포함될 리소스 개체의 경로입니다. 이 경로가 상대적인 경우 지정된 리소스를 포함하는 스크립트가 있는 현재 리소스의 경로에 추가됩니다. 경로 및 resourceType 또는 스크립트를 지정해야 합니다.

**resourceType**

* 포함할 리소스의 리소스 유형입니다. 리소스 유형이 설정된 경우 경로는 리소스 객체에 대한 정확한 경로여야 합니다. 이 경우 경로에 매개 변수, 선택기 및 확장을 추가할 수 없습니다.
* 포함할 리소스가 리소스로 확인할 수 없는 경로 속성으로 지정된 경우, 태그는 경로 및 이 리소스 유형에서 합성 리소스 객체를 만들 수 있습니다.
* 경로 및 resourceType 또는 스크립트를 지정해야 합니다.

**스크립트**

* 포함할 jsp 스크립트입니다. 경로 및 resourceType 또는 스크립트를 지정해야 합니다.

**ignoreComponentHierarchy**

* 스크립트 해상도에 대해 구성 요소 계층 구조를 무시할지 여부를 제어하는 부울입니다. true인 경우 검색 경로만 준수됩니다.

**예:**

```xml
<%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %><%
%><div class="center">
    <cq:include path="trail" resourceType="foundation/components/breadcrumb" />
    <cq:include path="title" resourceType="foundation/components/title" />
    <cq:include script="redirect.jsp"/>
    <cq:include path="par" resourceType="foundation/components/parsys" />
</div>
```

`<%@ include file="myScript.jsp" %>` 또는 `<cq:include script="myScript.jsp" %>`을(를) 사용하여 스크립트를 포함하시겠습니까?

* `<%@ include file="myScript.jsp" %>` 지시문은 JSP 컴파일러에 전체 파일을 현재 파일에 포함하도록 알립니다. 포함된 파일의 내용을 원본 파일에 직접 붙여넣은 것과 같습니다.
* `<cq:include script="myScript.jsp">` 태그를 사용하면 런타임 시 파일이 포함됩니다.

`<cq:include>` 또는 `<sling:include>`을(를) 사용하시겠습니까?

* AEM Adobe 구성 요소를 개발할 때는 `<cq:include>`을(를) 사용하는 것이 좋습니다.
* `<cq:include>`에서 script 특성을 사용할 때 해당 이름으로 스크립트 파일을 직접 포함할 수 있습니다. 이는 구성 요소 및 리소스 유형 상속을 고려하며, 선택기 및 확장을 사용하여 Sling의 스크립트 해상도를 엄격히 준수하는 것보다 간단한 경우가 많습니다.

### &lt;cq:includeClientLib> {#cq-includeclientlib}

>[!CAUTION]
>
>`<cq:includeClientLib>` AEM 5.6 이후 사용되지 않습니다. 대신 `<ui:includeClientLib>`을(를) 사용해야 합니다.

`<cq:includeClientLib>` 태그에는 js, css 또는 테마 라이브러리일 수 있는 AEM html 클라이언트 라이브러리가 포함되어 있습니다. 다른 유형의 여러 포함(예: js 및 css)의 경우, 이 태그는 jsp에서 여러 번 사용해야 합니다. 이 태그는 `com.day.cq.widget.HtmlLibraryManager` 서비스 인터페이스의 편리한 래퍼입니다.

여기에는 다음과 같은 속성이 있습니다.

**categories** - 쉼표로 구분된 클라이언트 라이브러리 범주 목록입니다. 여기에는 해당 카테고리의 모든 JavaScript 및 CSS 라이브러리가 포함됩니다. 요청에서 테마 이름이 추출됩니다.

해당 값: `com.day.cq.widget.HtmlLibraryManager#writeIncludes`

**테마** - 쉼표로 구분된 클라이언트 라이브러리 범주 목록입니다. 지정된 카테고리에 대한 모든 테마 관련 라이브러리(CSS 및 JS 모두)가 여기에 포함됩니다. 요청에서 테마 이름이 추출됩니다.

해당: `com.day.cq.widget.HtmlLibraryManager#`writeThemeInclude

**js** - 쉼표로 구분된 클라이언트 라이브러리 범주의 목록입니다. 여기에는 해당 카테고리의 모든 JavaScript 라이브러리가 포함됩니다.

해당 값: `com.day.cq.widget.HtmlLibraryManager#writeJsInclude`

**css** - 쉼표로 구분된 클라이언트 라이브러리 범주의 목록입니다. 여기에는 해당 카테고리의 모든 CSS 라이브러리가 포함됩니다.

해당 값: `com.day.cq.widget.HtmlLibraryManager#writeCssInclude`

**테마** - 테마 또는 테마가 아닌 라이브러리만 표시하는 플래그를 포함해야 합니다. 생략하면 두 세트가 모두 포함됩니다. 순수 JS 또는 CSS에만 적용됩니다(범주 또는 테마 포함에 대해서는 해당되지 않음).

`<cq:includeClientLib>` 태그는 jsp에서 다음과 같이 사용할 수 있습니다.

```xml
<%-- all: js + theme (theme-js + css) --%>
<cq:includeClientLib categories="cq.wcm.edit" />

<%-- only js libs --%>
<cq:includeClientLib js="cq.collab.calendar, cq.security" />

<%-- theme only (theme-js + css) --%>
<cq:includeClientLib theme="cq.collab.calendar, cq.security" />

<%-- css only --%>
<cq:includeClientLib css="cq.collab.calendar, cq.security" />
```

### &lt;cq:defineObjects> {#cq-defineobjects}

`<cq:defineObjects>` 태그는 개발자가 참조할 수 있는 스크립팅 개체를 정기적으로 사용하여 노출합니다. 또한 [`<sling:defineObjects>`](#amp-lt-sling-defineobjects) 태그에 정의된 개체를 노출합니다.

**componentContext**

* 요청의 현재 구성 요소 컨텍스트 개체(com.day.cq.wcm.api.components.ComponentContext 인터페이스)입니다.

**구성 요소**

* 현재 리소스의 현재 AEM 구성 요소 개체(com.day.cq.wcm.api.components.Component interface)입니다.

**currentDesign**

* 현재 페이지의 현재 디자인 개체(com.day.cq.wcm.api.designer.Design 인터페이스)입니다.

**currentPage**

* 현재 AEM WCM 페이지 개체(com.day.cq.wcm.api.Page 인터페이스)입니다.

**currentStyle**

* 현재 셀의 현재 스타일 개체(com.day.cq.wcm.api.designer.Style 인터페이스)입니다.

**디자이너**

* 디자인 정보에 액세스하는 데 사용되는 디자이너 개체(com.day.cq.wcm.api.designer.Designer 인터페이스)입니다.

**editContext**

* AEM 구성 요소의 편집 컨텍스트 개체(com.day.cq.wcm.api.components.EditContext 인터페이스).

**페이지 관리자**

* 페이지 수준 작업을 위한 페이지 관리자 개체(com.day.cq.wcm.api.PageManager 인터페이스)입니다.

**pageProperties**

* 현재 페이지의 페이지 속성 개체(org.apache.sling.api.resource.ValueMap).

**속성**

* 현재 리소스의 속성 개체(org.apache.sling.api.resource.ValueMap)입니다.

**resourceDesign**

* 리소스 페이지의 디자인 개체(com.day.cq.wcm.api.designer.Design 인터페이스).

**resourcePage**

* 리소스 페이지 개체(com.day.cq.wcm.api.Page 인터페이스)입니다.
* 여기에는 다음과 같은 속성이 있습니다.

**requestName**

* sling에서 상속

**responseName**

* sling에서 상속

**resourceName**

* sling에서 상속

**nodeName**

* sling에서 상속

**logName**

* sling에서 상속

**resourceResolverName**

* sling에서 상속

**slingName**

* sling에서 상속

**componentContextName**

* wcm별

**editContextName**

* wcm별

**속성 이름**

* wcm별

**pageManagerName**

* wcm별

**currentPageName**

* wcm별

**resourcePageName**

* wcm별

**pagePropertiesName**

* wcm별

**componentName**

* wcm별

**designerName**

* wcm별

**currentDesignName**

* wcm별

**resourceDesignName**

* wcm별

**currentStyleName**

* wcm별

**예**

```xml
<%@page session="false" contentType="text/html; charset=utf-8" %><%
%><%@ page import="com.day.cq.wcm.api.WCMMode" %><%
%><%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %><%
%><cq:defineObjects/>
```

>[!NOTE]
>
>스크립트에 `/libs/foundation/global.jsp` 파일이 포함되어 있으면 `<cq:defineObjects />` 태그가 자동으로 포함됩니다.

### &lt;cq:requestURL> {#cq-requesturl}

`<cq:requestURL>` 태그는 현재 요청 URL을 JspWriter에 씁니다. 두 태그 [`<cq:addParam>`](#amp-lt-cq-addparam) 및 [`<cq:removeParam>`](#amp-lt-cq-removeparam)은(는) 쓰기 전에 현재 요청 URL을 수정하기 위해 이 태그의 본문 내에서 사용할 수 있습니다.

다양한 매개 변수를 사용하여 현재 페이지에 대한 링크를 만들 수 있습니다. 예를 들어 요청을 변형할 수 있습니다.

`mypage.html?mode=view&query=something`에 `mypage.html?query=something`을(를) 연결합니다.

`addParam` 또는 `removeParam`을(를) 사용하면 지정된 매개 변수의 발생만 변경되며 다른 모든 매개 변수는 영향을 받지 않습니다.

`<cq:requestURL>`에 특성이 없습니다.

예:

```xml
<a href="<cq:requestURL><cq:removeParam name="language"/></cq:requestURL>">remove filter</a>
```

```xml
<a title="filter results" href="<cq:requestURL><cq:addParam name="language" value="${bucket.value}"/></cq:requestURL>">${label} (${bucket.count})</a>
```

### &lt;cq:addParam> {#cq-addparam}

`<cq:addParam>` 태그는 지정된 이름과 값을 가진 요청 매개 변수를 바깥쪽 [`<cq:requestURL>`](#amp-lt-cq-requesturl) 태그에 추가합니다.

여기에는 다음과 같은 속성이 있습니다.

**이름**

* 추가할 매개 변수의 이름

**값**

* 추가할 매개 변수의 값

**예:**

```xml
<a title="filter results" href="<cq:requestURL><cq:addParam name="language" value="${bucket.value}"/></cq:requestURL>">${label} (${bucket.count})</a>
```

### &lt;cq:removeParam> {#cq-removeparam}

`<cq:removeParam>` 태그는 바깥쪽 [`<cq:requestURL>`](#amp-lt-cq-requesturl) 태그에서 지정된 이름과 값을 가진 요청 매개 변수를 제거합니다. 값을 제공하지 않으면 지정된 이름의 모든 매개 변수가 제거됩니다.

여기에는 다음과 같은 속성이 있습니다.

**이름**

* 제거할 매개 변수의 이름

예:

```xml
<a href="<cq:requestURL><cq:removeParam name="language"/></cq:requestURL>">remove filter</a>
```

## Sling 태그 라이브러리 {#sling-tag-library}

Sling 태그 라이브러리에는 유용한 Sling 기능이 포함되어 있습니다.

스크립트에서 Sling 태그 라이브러리를 사용할 때 스크립트는 다음 코드로 시작해야 합니다.

```xml
<%@ taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling/1.0" %>
```

>[!NOTE]
>
>`/libs/foundation/global.jsp` 파일이 스크립트에 포함되면 sling taglib이 자동으로 선언됩니다.

### &lt;sling:include> {#sling-include}

`<sling:include>` 태그에 현재 페이지에 대한 리소스가 포함되어 있습니다.

여기에는 다음과 같은 속성이 있습니다.

**플러시**

* 대상을 포함하기 전에 출력을 플러시할지 여부를 정의하는 부울.

**리소스**

* 현재 요청 처리에 포함될 리소스 개체입니다. 리소스 또는 경로를 지정해야 합니다. 둘 다 지정하면 리소스가 우선합니다.

**경로**

* 현재 요청 처리에 포함될 리소스 개체의 경로입니다. 이 경로가 상대적인 경우 지정된 리소스를 포함하는 스크립트가 있는 현재 리소스의 경로에 추가됩니다. 리소스 또는 경로를 지정해야 합니다. 둘 다 지정하면 리소스가 우선합니다.

**resourceType**

* 포함할 리소스의 리소스 유형입니다. 리소스 유형이 설정된 경우 경로는 리소스 객체에 대한 정확한 경로여야 합니다. 이 경우 경로에 매개 변수, 선택기 및 확장을 추가할 수 없습니다.
* 포함할 리소스가 리소스로 확인할 수 없는 경로 속성으로 지정된 경우, 태그는 경로 및 이 리소스 유형에서 합성 리소스 객체를 만들 수 있습니다.

**replaceSelectors**

* 디스패치 시 선택기는 이 속성 값으로 대체됩니다.

**addSelectors**

* 디스패치 시 이 속성의 값이 선택기에 추가됩니다.

**replaceSuffix**

* 디스패치 시 접미사는 이 속성 값으로 대체됩니다.

>[!NOTE]
>
>`<sling:include>` 태그에 포함된 리소스 및 스크립트의 해상도가 일반 sling URL 해상도와 동일합니다. 기본적으로 현재 요청의 선택기, 확장 등은 포함된 스크립트에도 사용됩니다. 태그 특성을 통해 수정할 수 있습니다. 예를 들어 `replaceSelectors="foo.bar"`을(를) 사용하면 선택기를 덮어쓸 수 있습니다.

예:

```xml
<div class="item"><sling:include path="<%= pathtoinclude %>"/></div>
```

```xml
<sling:include resource="<%= par %>"/>
```

```xml
<sling:include addSelectors="spool"/>
```

```xml
<sling:include resource="<%= par %>" resourceType="<%= newType %>"/>
```

```xml
<sling:include resource="<%= par %>" resourceType="<%= newType %>"/>
```

```xml
<sling:include replaceSelectors="content" />
```

### &lt;sling:defineObjects> {#sling-defineobjects}

`<sling:defineObjects>` 태그는 개발자가 참조할 수 있는 다음과 같은 규칙적으로 사용되는 스크립팅 개체를 노출합니다.

**slingRequest**

* HTTP 요청 헤더 정보에 대한 액세스 권한을 제공하는 SlingHttpServletRequest 개체는 표준 HttpServletRequest를 확장하며 리소스, 경로 정보 및 선택기와 같은 Sling 관련 항목에 대한 액세스 권한을 제공합니다.

**slingResponse**

* 서버에서 만든 HTTP 응답에 대한 액세스를 제공하는 SlingHttpServletResponse 개체입니다. 이는 확장되는 HttpServletResponse와 동일합니다.**요청**
* 순수 HttpServletRequest인 표준 JSP 요청 개체입니다.**응답**
* 순수 HttpServletResponse인 표준 JSP 응답 개체입니다.

**resourceResolver**

* 현재 ResourceResolver 개체입니다. slingRequest.getResourceResolver() 와 동일합니다

.**sling**

* 스크립트에 대한 편의 메서드를 포함하는 SlingScriptHelper 개체로서, 주로 sling.include(&#39;/some/other/resource&#39;) 는 이 응답 내에 있는 다른 리소스의 응답(예: 헤더 html 코드 조각 포함)과 sling에서 사용할 수 있는 OSGi 서비스를 검색하기 위한 sling.getService(foo.bar.Service.class)를 포함합니다(스크립트 언어에 따른 클래스 표기법).

**리소스**

* 요청의 URL에 따라 처리할 현재 리소스 개체입니다. slingRequest.getResource() 와 동일합니다.

**currentNode**

* 현재 리소스가 JCR 노드를 가리키는 경우(일반적으로 Sling의 경우), 이렇게 하면 노드 개체에 직접 액세스할 수 있습니다. 그렇지 않으면 이 개체가 정의되지 않습니다.

**로그**

* 스크립트 내에서 Sling 로그 시스템에 로깅하기 위한 SLF4J 로거를 제공합니다(예: log.info(&quot;내 스크립트 실행&quot;)).

* 여기에는 다음과 같은 속성이 있습니다.

**requestName**

**responseName**

**nodeName**

l **ogName resourceResolverName**

**slingName**

**예:**

```xml
<%@page session="false" %><%
%><%@page import="com.day.cq.wcm.foundation.forms.ValidationHelper"%><%
%><%@taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling/1.0" %><%
%><sling:defineObjects/>
```

## JSTL 태그 라이브러리 {#jstl-tag-library}

[JavaServer Pages 표준 태그 라이브러리](https://www.oracle.com/java/technologies/java-server-tag-library.html)에는 유용한 표준 태그가 많이 포함되어 있습니다. 다음 코드 조각과 같이 `/libs/foundation/global.jsp`에 의해 core, formatting 및 function 태그가 정의됩니다.

### /libs/foundation/global.jsp 추출 {#extract-of-libs-foundation-global-jsp}

```xml
<%@taglib prefix="c" uri="https://java.sun.com/jsp/jstl/core" %>
<%@taglib prefix="fmt" uri="https://java.sun.com/jsp/jstl/fmt" %>
<%@taglib prefix="fn" uri="https://java.sun.com/jsp/jstl/functions" %>
```

앞에서 설명한 대로 `/libs/foundation/global.jsp` 파일을 가져온 후에는 `c`, `fmt` 및 `fn` 접두사를 사용하여 해당 taglib에 액세스할 수 있습니다. JSTL의 공식 설명서는 [Java™ EE 5 자습서 - JavaServer Pages 표준 태그 라이브러리](https://docs.oracle.com/javaee/5/tutorial/doc/bnakc.html)에서 확인할 수 있습니다.
