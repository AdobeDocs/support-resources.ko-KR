---
title: 숨겨진 문제 해결
description: 숨겨진 문제
type: Troubleshooting
hide: true
hidefromtoc: true
exl-id: dfb54d2d-e4f4-420f-8e91-f1aba704cb31
source-git-commit: a9acc52cf5469ffeb9711ac6f4b52d54bb99086f
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---

# 숨겨진 문제 해결

이 페이지에 적용된 `type: Troubleshooting`이(가) 있습니다. 왼쪽 탐색 기능이 있나요?

## 코드 테이블

**테이블 외부**

```json
PrimaryIdentities [
  {"id": "ccid-2", "namespace": "CCID"},
  {"id": "ecid-1", "namespace": "ECID"},
  {"id": "ecid-2", "namespace": "ECID"}
  ]
NonPrimaryIdentities [
  {"id": "ccid-1", "namespace": "CCID"},
  {"id": "ecid-3", "namespace": "ECID"}
  ]
  "id": "ccid-1",
    "namespace": "CCID"
```

테이블의 **스트레이트 코드**

<table>
    <tr>
      <th>정렬된 ID 목록</th>
      <th>선택한 ID</th>
    </tr>
    <tr>
      <td><code>PrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-2", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-1", "namespace": "ECID"},<br/>&nbsp;&nbsp;{"id": "ecid-2", "namespace": "ECID"}<br/>&nbsp;]<br/>&nbsp;NonPrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-1", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-3", "namespace": "ECID"}<br/>]</code> </td>
      <td><code>"id": "ccid-1",<br/>&nbsp;"namespace": "CCID"</code> </td>
    </tr>
  </table>

**테이블에서 사전 언어 코드 사용**

<table>
    <tr>
      <th>정렬된 ID 목록</th>
      <th>선택한 ID</th>
    </tr>
    <tr>
      <td><pre lang="json"><code>PrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-2", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-1", "namespace": "ECID"},<br/>&nbsp;&nbsp;{"id": "ecid-2", "namespace": "ECID"}<br/>&nbsp;]<br/>&nbsp;NonPrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-1", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-3", "namespace": "ECID"}<br/>]</pre></code> </td>
      <td><pre lang="json"><code>"id": "ccid-1",<br/>&nbsp;"namespace": "CCID"</pre></code> </td>
    </tr>
  </table>

## 새 탭이 있는 딥링크

여기를 클릭하세요. [새 탭에서 열린 문서에 대한 상대 링크](hidden/bug-fixes.md#test-for-autoactivate){target=_blank}

```
Click here: [Relative link to article open in new tab](hidden/bug-fixes.md#test-for-autoactivate){target=_blank}
```
