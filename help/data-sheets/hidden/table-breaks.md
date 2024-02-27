---
title: 테이블 나누기
description: 다른 테이블 나누기 테스트
hide: true
hidefromtoc: true
source-git-commit: cd9f841a3f720ee366b33f3a78f7ca731c0b865a
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 28%

---

# 테이블 나누기

## 를 사용하는 표준 Markdown 표 `<br>`

**고정`Green<br>Red<br>Blue`**

|  | 숫자 | 색상 |
|---|---|---|
| 후아니야 | 17 | 녹색<br>빨간색<br>파란색 |
| 마리아 | 23 | 노란색<br>갈색 |

{style="table-layout:fixed"}

**자동`Green<br>Red<br>Blue`**

|  | 숫자 | 색상 |
|---|---|---|
| 후아니야 | 17 | 녹색<br>빨간색<br>파란색 |
| 마리아 | 23 | 노란색<br>갈색 |

{style="table-layout:auto"}

## double이 있는 Markdown 표 `<br>`s

**고정`Green<br><br>Red<br><br>Blue`**

|  | 숫자 | 색상 |
|---|---|---|
| 후아니야 | 17 | 녹색<br><br>빨간색<br><br>파란색 |
| 마리아 | 23 | 노란색<br><br>갈색 |

{style="table-layout:fixed"}

**자동`Green<br><br>Red<br><br>Blue`**

|  | 숫자 | 색상 |
|---|---|---|
| 후아니야 | 17 | 녹색<br><br>빨간색<br><br>파란색 |
| 마리아 | 23 | 노란색<br><br>갈색 |

{style="table-layout:auto"}

## 가 있는 Markdown 표 `<p>`

**고정`Green<p>Red<p>Blue`**

|  | 숫자 | 색상 |
|---|---|---|
| 후아니야 | 17 | 녹색<p>빨간색<p>파란색 |
| 마리아 | 23 | 노란색<p>갈색 |

{style="table-layout:fixed"}

**자동`Green<p>Red<p>Blue`**

|  | 숫자 | 색상 |
|---|---|---|
| 후아니야 | 17 | 녹색<p>빨간색<p>파란색 |
| 마리아 | 23 | 노란색<p>갈색 |

{style="table-layout:auto"}

|  | 숫자 | 색상 |
|---|---|---|
| 후아니야 | 17 | 이게 색깔이야 **녹색** 그리고 그것은 문제로서 다른 줄에 래핑하기 위한 것이며, 위 단락 깨짐을 테스트하기 위한 수단입니다. <p>이게 색깔이야 **빨강** 그리고 그것은 문제로서 다른 줄에 래핑하기 위한 것이며, 위 단락 깨짐을 테스트하기 위한 수단입니다. <p>이게 색깔이야 **파랑** 그리고 그것은 문제로서 다른 줄에 래핑하기 위한 것이며, 위 단락 깨짐을 테스트하기 위한 수단입니다. |
| 마리아 | 23 | 노란색<p>갈색 |

{style="table-layout:fixed"}

|  | 숫자 | 색상 |
|---|---|---|
| 후아니야 | 17 | 이게 색깔이야 **녹색** 그리고 그것은 문제로서 다른 줄에 래핑하기 위한 것이며, 위 단락 깨짐을 테스트하기 위한 수단입니다. <p>이게 색깔이야 **빨강** 그리고 그것은 문제로서 다른 줄에 래핑하기 위한 것이며, 위 단락 깨짐을 테스트하기 위한 수단입니다. <p>이게 색깔이야 **파랑** 그리고 그것은 문제로서 다른 줄에 래핑하기 위한 것이며, 위 단락 깨짐을 테스트하기 위한 수단입니다. |
| 마리아 | 23 | 노란색<p>갈색 |

{style="table-layout:auto"}
