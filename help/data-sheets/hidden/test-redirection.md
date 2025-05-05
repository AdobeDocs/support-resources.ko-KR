---
title: 테스트 페이지 리디렉션(숨김)
description: 내부 테스트용 테스트 페이지
hide: true
hidefromtoc: true
exl-id: 07e6051d-b29c-4ac3-980c-d064487c2804
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 12%

---

# 테스트 페이지 리디렉션(숨김)

리디렉션이 있는 숨겨진 테스트 페이지

## 표준 1:1 리디렉션

EXL: <https://experienceleague.adobe.com/docs/workfront/using/review-and-approve-work/proofing/create-proofs/create-proofs--in-wf.html?lang=ko>

EDS: <https://eds.experienceleague.adobe.com/en/docs/workfront/using/review-and-approve-work/proofing/create-proofs/create-proofs--in-wf>

EXL: <https://experienceleague.adobe.com/docs/workfront/using/product-announcements/product-releases/quarterly-release/release-20-2/2020.2-release-overview.html?lang=ko>

EDS: <https://eds.experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/quarterly-release/release-20-2/2020.2-release-overview>

## 와일드카드 리디렉션

(다대일) `https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/?lang=ko*`

* EXL: <https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/bubba.html?lang=ko>
* EDS: <https://eds.experienceleague.adobe.com/en/docs/analytics/analyze/reports-analytics/bubba>

(1:1) `https://experienceleague.adobe.com/docs/primetime/aiq-help/(*)`

* EXL: <https://experienceleague.adobe.com/docs/primetime/aiq-help/account-iq-components/segments-timeframe.html?lang=ko>
* EDS: <https://eds.experienceleague.adobe.com/en/docs/primetime/aiq-help/account-iq-components/segments-timeframe>

(1:1) `https://experienceleague.adobe.com/docs/adobe-campaign-insider-events/events/(*)`

* EXL: <https://experienceleague.adobe.com/docs/adobe-campaign-insider-events/events/2022/microsoft.html?lang=ko>
* EDS: <https://eds.experienceleague.adobe.com/en/docs/adobe-campaign-insider-events/events/2022/microsoft>

## 기타 리디렉션

랜딩 페이지, 기타 도메인, nginx 구성

<https://one.workfront.com/s/managed-content-videos/welcome-to-workfront-MCFSRY5DWNL5EENJI3JD6XIB3TOM>

<https://experienceleague.adobe.com/docs/events.html?lang=ko>
