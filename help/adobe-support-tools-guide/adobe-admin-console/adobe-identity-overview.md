---
title: ID 개요
description: 조직의 ID 유형(Federated ID, Enterprise ID, Adobe ID 및 Personal Adobe ID)을 이해하고 선택하고 Admin Console에서 사용자 액세스를 관리합니다.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: c066e95c05f8e8a0953daecda9a220268d325f98
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 5%

---


# ID 개요

엔터프라이즈 및 팀에 적용됩니다.

Adobe의 id 관리 시스템은 관리자가 애플리케이션 및 서비스에 대한 사용자의 액세스 권한을 만들고 관리할 수 있도록 도와줍니다. Adobe은 사용자를 인증하고 권한을 부여하는 데 사용할 수 있는 이러한 ID 유형 또는 계정을 제공합니다.

## Adobe Admin Console의 ID 유형

ID 유형을 사용하면 조직이 사용자의 계정 및 데이터를 다양한 수준으로 제어할 수 있습니다. ID 모델을 선택하면 조직의 자산 저장 및 공유 방법에 상당한 영향을 미칩니다. Federated ID 및 Enterprise ID 모델은 조직에서 만들고 관리하는 반면 Adobe ID는 개인이 만들고 관리합니다.

다음 표는 조직에 가장 적합한 ID 모델을 선택하는 방법을 안내합니다.

>[!NOTE]
>조직이 Adobe의 엔터프라이즈 스토리지 모델로 업데이트되지 않았으며 개인 사용자에 대해 Adobe ID를 계속 사용하고 있는 경우 아래 [ID 유형 표](https://helpx.adobe.com/kr/enterprise/using/identity.html#using-personal-adobe-id)의 설명을 참조하십시오.

<table>
<thead>
<tr>
<th scope="col">ID 유형</th>

<th scope="col" style="text-align: center;">
  <img src="./assets/federated-id.png" alt="Federated ID 아이콘"><br>
  Federated ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/enterprise-id.png" alt="Enterprise ID"><br>
  Enterprise ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/adobe-id.png" alt="Adobe ID"><br>
  Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>주요 서비스</strong></th>
<td>조직에서 만들고, 소유하고, 관리합니다. 조직은 사용자 자격 증명을 관리하고 SAML2 ID 공급자(IdP)를 통해 SSO(Single Sign-On)를 사용합니다.</td>
<td>조직에서 만들고, 소유하고, 관리합니다. 조직은 확인된 도메인에 사용자 계정을 만들 수 있는 배타적 권한을 갖습니다.</td>
<td>최종 사용자가 생성, 소유 및 관리합니다. Adobe에서 인증을 수행하고 최종 사용자가 id를 관리합니다. <a href="https://helpx.adobe.com/kr/enterprise/using/storage-for-business.html">저장소 모델</a>에 따라 사용자 또는 기업이 파일 및 데이터를 계속 제어합니다. Adobe ID 계정은 확인되지 않은 도메인, 공개 도메인 또는 신뢰할 수 있는 도메인에서 만들어집니다. 아래의 노트 섹션의 포인트 2를 참조하십시오.</td>
</tr>
<tr>
<th scope="row"><strong>계정 및 데이터 소유권</strong></th>
<td colspan="2">조직 소유 및 제어</td>
<td>엔터프라이즈 스토리지용 조직 소유 및 사용자 스토리지용 사용자 소유</td>
</tr>
<tr>
<th scope="row"><strong>보안 및 모니터링</strong></th>
<td colspan="2">
  <ul>
    <li>감사 로그</li>
    <li>콘텐츠 로그</li>
    <li>공유 제한 사항</li>
    <li>조직의 인증 설정</li>
  </ul>
</td>

<td>
  <ul>
    <li>콘텐츠 로그</li>
    <li>공유 제한 사항</li>
    <li>암호 정책</li>
  </ul>
</td>

</tr>
<tr>
<th scope="row"><strong>암호 재설정</strong></th>
<td colspan="2">지원되지 않음</td>
<td><a href="https://helpx.adobe.com/kr/manage-account/using/change-or-reset-password.html">계정 암호 재설정</a></td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud for enterprise 및 Document Cloud for enterprise</strong></th>
<td colspan="3">지원됨</td>
</tr>
<tr>
<th scope="row"><strong>팀용 Creative Cloud 및 팀용 Document Cloud</strong></th>
<td colspan="2">지원되지 않음</td>
<td>지원됨</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td colspan="3">지원됨</td>
</tr>
<tr>
<th scope="row"><strong>추천 대상</strong></th>
<td>
  <ul>
    <li>이미 SSO 또는 SAML을 사용 중인 조직</li>
    <li>기존 디렉터리 서비스(예: Google 및 Azure AD)</li>
    <li>비 Adobe 서비스와의 간편한 통합 필요</li>
    <li>도메인의 소유권을 증명할 수 있음</li>
  </ul>
</td>
<td>
  <ul>
    <li>도메인의 소유권을 증명할 수 있음</li>
    <li>SSO 필요 없음</li>
  </ul>
</td>
<td>
  <ul>
    <li>Creative Cloud for teams</li>
    <li>조직은 소유하지 않는 도메인을 사용함</li>
    <li>공개 도메인(예: Hotmail, Gmail)</li>
    <li>Adobe Experience Manager Mobile과 같은 앱에 액세스</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>시작하기</strong></th>
<td><a href="https://helpx.adobe.com/kr/enterprise/using/set-up-identity.html">ID 설정</a></td>
<td><a href="https://helpx.adobe.com/enterprise/using/add-domains-directories.html#claim-domains">클레임 도메인</a></td>
<td><a href="https://helpx.adobe.com/kr/enterprise/using/users.html#add-users">사용자 추가</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. 팀의 Creative Cloud에 대한 암호 정책은 개인의 Creative Cloud에 대한 암호 정책과 동일합니다.
>1. Adobe ID 사용자는 Adobe ID 자격 증명 또는 소유 조직의 인증 모델(SSO, 2FA 등)을 통해 인증합니다. 이러한 시나리오에서는 사용자가 소유 조직의 SSO 페이지로 리디렉션됩니다. 인증 후 사용자는 [비즈니스 프로필을 선택](https://helpx.adobe.com/kr/enterprise/kb/enterprise-id-faq.html#choose-profile)해야 할 수 있습니다.

## 개인 Adobe ID 사용

Adobe은 Adobe의 엔터프라이즈 스토리지 모델을 사용하도록 모든 팀 및 엔터프라이즈 고객을 업데이트하고 있습니다. 조직에 회사 또는 학교 Adobe 앱 및 서비스에 액세스하기 위해 개인 Adobe ID를 사용하는 사용자가 있다면 다음 표를 참조하십시오.

### 개인 Adobe ID

<table>
<thead>
<tr>
<th scope="col">ID 유형</th>
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/personal-adobe-id.png" alt="Adobe ID"><br>
  개인 Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>주요 서비스</strong></th>
<td>최종 사용자가 생성, 소유 및 관리합니다. Adobe에서 인증을 수행하고 최종 사용자가 id를 관리합니다.</td>
</tr>
<tr>
<th scope="row"><strong>계정 및 데이터 소유권</strong></th>
<td>사용자 제어</td>
</tr>
<tr>
<th scope="row"><strong>보안 및 모니터링</strong></th>
<td>암호 정책. 아래의 참고 섹션에서 1번 포인트를 참조하십시오.</td>
</tr>
<tr>
<th scope="row"><strong>암호 재설정</strong></th>
<td><a href="https://helpx.adobe.com/kr/manage-account/using/change-or-reset-password.html">계정 암호를 다시 설정합니다.</a> 아래 메모 섹션에서 지점 2를 참조하세요.</td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud for enterprise 및 Document Cloud for enterprise</strong></th>
<td>지원됨</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td>지원됨</td>
</tr>
<tr>
<th scope="row"><strong>다음에 대해서만 사용 가능 / 권장</strong></th>
<td>
  <ul>
    <li>마이그레이션 전에 온보딩된 기업 및 팀 고객</li>
    <li>Creative Cloud for teams</li>
    <li>사용자의 손 안에 컨트롤 필요</li>
    <li>Digital Publishing Suite과 같은 앱에 액세스</li>
    <li>사용자가 조직에서 분리된 후 에셋을 소유합니다.</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>시작하기</strong></th>
<td><a href="https://helpx.adobe.com/kr/enterprise/using/users.html#add-users">사용자 추가</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. 팀의 Creative Cloud에 대한 암호 정책은 개인의 Creative Cloud에 대한 암호 정책과 동일합니다.
>1. [엔터프라이즈 스토리지](https://helpx.adobe.com/kr/enterprise/using/manage-adobe-storage.html)를 사용하는 기업 고객을 위한 Creative Cloud의 경우 관리자는 Admin Console에 Adobe ID 사용자를 추가할 수 있지만 제품 프로필에 추가할 수는 없습니다. 관리자는 Adobe ID 사용자를 다른 ID 유형으로 마이그레이션해야 합니다.
>1. **Adobe 라이선스 웹 사이트와 같이** Adobe ID만 지원하는 일부 제품 및 서비스가 있습니다.

## 비슷한 항목 더 보기

- [ID 설정](https://helpx.adobe.com/kr/enterprise/using/set-up-identity.html)
- [사용자 ID 전환](https://helpx.adobe.com/kr/enterprise/using/switch-user-identity.html)
- [Admin Console 개요](https://helpx.adobe.com/enterprise/using/admin-console-overview.html)
- [교육 FAQ](https://helpx.adobe.com/enterprise/using/education-faq.html)
- [사용자 추가 및 관리](https://helpx.adobe.com/kr/enterprise/using/users.html)