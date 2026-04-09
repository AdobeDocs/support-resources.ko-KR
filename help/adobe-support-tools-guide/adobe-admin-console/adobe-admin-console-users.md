---
title: Adobe Admin Console 사용자
description: Adobe Admin Console에서 사용자를 관리하는 전략을 계획합니다. 관리자와 최종 사용자를 추가하고, 사용자 관리 방법을 선택하고, 라이선스를 할당합니다.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: d92f4190b68a480409f4126a877de3469ed836f0
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 3%

---

# Adobe Admin Console 사용자

엔터프라이즈 및 팀에 적용됩니다.

이 문제 중 하나를 직면하고 있습니까? 문제를 선택하여 해결 방법을 확인하십시오.

- [관리자 역할 관리](https://helpx.adobe.com/kr/enterprise/using/admin-roles.html)
- [다운로드 설치 문제](https://helpx.adobe.com/kr/download-install.html)
- [Enterprise ID 사용자 암호 재설정](https://helpx.adobe.com/kr/enterprise/kb/enterprise-id-faq.html#faq)
- [Federated ID 오류 해결](https://helpx.adobe.com/kr/enterprise/kb/tshoot-fed-id.html)
- [사용자 삭제 또는 삭제된 사용자 복원](https://helpx.adobe.com/kr/enterprise/using/manage-directory-users.html)

**Adobe Admin Console - 사용자** — [YouTube 시청](https://youtu.be/w8b36YX2TEM)

## Adobe Admin Console에 사용자를 추가하는 이유

>[!NOTE]
>
>Adobe Admin Console의 관리자로서 [ID 유형](https://helpx.adobe.com/kr/enterprise/using/identity.html)을(를) 선택하고 [ID를 설정](https://helpx.adobe.com/kr/enterprise/using/set-up-identity.html)한 후 다음 작업은 Admin Console에 사용자를 추가하는 것입니다.

Adobe enterprise 및 teams는 크게 두 가지 유형의 사용자를 정의합니다.

### 관리자(관리자)

Enterprise 또는 Teams 관리자는 Admin Console에서 관리 작업을 수행합니다. 관리자를 추가하여 Adobe 제품 액세스, 사용 및 기타 관리 작업을 세분화하고 관리할 수 있는 유연한 관리 계층 구조를 정의할 수 있습니다.

모든 관리자를 Admin Console에 추가해야 합니다. 관리자 권한을 추가하면 해당 [관리자 역할](https://helpx.adobe.com/kr/enterprise/using/admin-roles.html)을(를) 기반으로 합니다.

### 최종 사용자

최종 사용자는 조직 또는 기관이 Adobe과의 계약 일부로 획득한 Adobe 제품 및 서비스를 사용하는 조직 또는 기관의 사용자입니다.

## 사용자 관리 전략 결정

요구 사항에 따라 사용자를 *개별적으로*&#x200B;추가, 제거 또는 업데이트하거나 사용 가능한 *일괄 업로드 방법* 중 하나를 사용합니다. 다음 매트릭스를 참조하여 사용자 관리를 계획하십시오.

>[!NOTE]
>
>새로운 Adobe 엔터프라이즈 또는 팀 고객의 경우 Admin Console에서 사용자 관리를 시작하기 전에 이 표를 살펴보는 것이 좋습니다. 기존 고객은 특히 한 ID 유형에서 다른 ID 유형으로 마이그레이션하려는 경우 이를 사용할 수 있습니다([ID 유형 편집](https://helpx.adobe.com/kr/enterprise/using/switch-user-identity.html) 참조).

<table>
<thead>
<tr>
<th scope="col"></th>
<th scope="col"><strong>개별(Admin Console)</strong></th>
<th scope="col"><strong>CSV 일괄 업로드(Admin Console)</strong></th>
<th scope="col"><strong>Azure / Google 커넥터</strong></th>
<th scope="col"><strong>사용자 동기화 도구</strong></th>
<th scope="col"><strong>사용자 관리 REST API</strong></th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>적용 대상</strong></th>
<td colspan="2">Adobe 팀 및 엔터프라이즈 고객</td>
<td colspan="3">Adobe 엔터프라이즈 고객</td>
</tr>
<tr>
<th scope="row"><strong>설명</strong></th>
<td>Admin Console에서 개별적으로 사용자를 관리합니다.</td>
<td>Admin Console에서 CSV 파일 업로드를 통해 사용자를 관리합니다.</td>
<td>기존 Azure AD 포털 또는 Google 페더레이션을 기반으로 사용자(및 그룹)를 관리합니다.</td>
<td colspan="2">조직의 LDAP를 기반으로 사용자(및 그룹)를 관리합니다.</td>
</tr>
<tr>
<th scope="row"><strong>사용자 추가</strong></th>
<td><strong>Admin Console</strong>의 <strong>사용자</strong> 탭 <a href="https://helpx.adobe.com/kr/enterprise/using/manage-users-individually.html#add-users">자세히 보기</a>.</td>
<td><strong>Admin Console</strong>에서 <strong>CSV로 사용자 추가</strong>를 사용하십시오. <a href="https://helpx.adobe.com/kr/enterprise/using/bulk-upload-users.html">자세히 보기</a>. <em>(기본 CSV 템플릿 사용)</em></td>
<td><a href="https://helpx.adobe.com/kr/enterprise/using/sso-setup-azure.html">Azure</a> 또는 <a href="https://helpx.adobe.com/kr/enterprise/using/setup-sso-google.html">Google</a>에서 사용자를 추가하십시오. 또는 <strong>Admin Console</strong>을 통해 게시할 수 있습니다.</td>
<td colspan="2">조직의 LDAP에 사용자를 추가해야 합니다.</td>
</tr>
<tr>
<th scope="row"><strong>사용자 제거</strong></th>
<td><strong>Admin Console</strong>에서 사용자를 선택하고 제거합니다. <a href="https://helpx.adobe.com/kr/enterprise/using/manage-users-individually.html#remove-users">자세히 보기</a>.</td>
<td><strong>Admin Console</strong>의 <strong>사용자</strong> 탭에서 <strong>CSV로 사용자 제거</strong>를 선택합니다. <a href="https://helpx.adobe.com/kr/enterprise/using/bulk-upload-users.html#remove-users">자세히 보기</a>. <em>(기본 CSV 템플릿 사용)</em></td>
<td><a href="https://helpx.adobe.com/kr/enterprise/using/sso-setup-azure.html">Azure</a> 또는 <a href="https://helpx.adobe.com/kr/enterprise/using/setup-sso-google.html">Google</a>에서 사용자를 제거해야 합니다.</td>
<td colspan="2">사용자 정보가 동기화 상태인지 확인하십시오. <strong>주의:</strong> 조직의 LDAP에 없는 사용자는 Admin Console에서 제거됩니다.</td>
</tr>
<tr>
<th scope="row"><strong>사용자 세부 정보 편집</strong></th>
<td>사용자를 선택한 다음 Admin Console에서 <strong>사용자 세부 정보 편집</strong>을 선택하십시오. <a href="https://helpx.adobe.com/kr/enterprise/using/manage-users-individually.html#edit-user-details">자세히 보기</a>.</td>
<td><strong>Admin Console</strong>의 <strong>사용자</strong> 탭에서 <strong>CSV로 사용자 세부 정보 편집</strong>을 선택합니다. <a href="https://helpx.adobe.com/kr/enterprise/using/bulk-upload-users.html#edit-user-details">자세히 보기</a>. <em>(기본 CSV 템플릿 사용)</em></td>
<td><a href="https://helpx.adobe.com/kr/enterprise/using/sso-setup-azure.html">Azure</a> 또는 <a href="https://helpx.adobe.com/kr/enterprise/using/setup-sso-google.html">Google</a>에서 모든 사용자 정보를 변경해야 합니다.</td>
<td colspan="2">사용자 정보가 동기화 상태인지 확인하십시오.</td>
</tr>
<tr>
<th scope="row"><strong>지원되는 ID 유형</strong></th>
<td colspan="2">모두</td>
<td>Federated ID</td>
<td colspan="2">Federated ID 및 Enterprise ID</td>
</tr>
<tr>
<th scope="row"><strong>최대 작업당 업데이트 수</strong></th>
<td>10</td>
<td>25,000(<em>5,000(최적의 성능을 위해)</em>)</td>
<td colspan="3">무제한(조직의 LDAP에 매핑)</td>
</tr>
<tr>
<th scope="row"><strong>필요</strong></th>
<td>Adobe Admin Console</td>
<td>.csv 파일 형식 만들기 및 업데이트(권장: Microsoft Excel 사용)</td>
<td>Azure AD 또는 Google 페더레이션을 설정해야 합니다.</td>

<td>
  <ul>
    <li>macOS 터미널 또는 Windows 명령 프롬프트</li>
    <li>LDAP 이해</li>
  </ul>
</td>

<td>REST API 사용을 위한 프로그래밍 언어(Python 등)에 대한 작업 지식</td>
</tr>
<tr>
<th scope="row"><strong>자세히 보기</strong></th>
<td><a href="https://helpx.adobe.com/kr/enterprise/using/manage-users-individually.html">개별 사용자 관리</a></td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/kr/enterprise/using/bulk-upload-users.html">
        사용자 관리 | CSV 일괄 업로드
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/kr/enterprise/kb/troubleshoot-bulk-user-csv-upload.html">
        대량 사용자 CSV 업로드 문제 해결
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/kr/enterprise/using/sso-setup-azure.html">
        Azure AD 커넥터
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/kr/enterprise/using/setup-sso-google.html">
        Google 페더레이션 커넥터
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://adobe-apiplatform.github.io/user-sync.py/en/">
        사용자 동기화 정보
      </a>
    </li>
    <li>
      <a href="https://github.com/adobe-apiplatform/user-sync.py">
        Git 저장소
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/kr/enterprise/using/user-sync.html">
        단계별 안내서
      </a>
    </li>
  </ul>
</td>
<td><a href="https://developer.adobe.com/umapi/">UMAPI 정보</a></td>
</tr>
</tbody>
</table>

## 다음 단계

### 패키지 만들기

추가되면 사용자는 지정된 앱 및 서비스를 할당 받을 준비가 된 것입니다.

라이선스 방법에 따라 최종 사용자에게 라이선스를 할당합니다.

- **명명된 사용자 라이선스:** 이러한 사용자를 **제품**([팀의 경우](https://helpx.adobe.com/kr/enterprise/using/assign-licenses-to-teams-users.html)) 또는 **제품 프로필**([기업의 경우](https://helpx.adobe.com/kr/enterprise/using/manage-product-profiles.html))에 추가하여 Adobe 제품 및 서비스 권한을 부여합니다. 자세한 내용은 [지정 사용자 라이선스 패키지를 만드는 방법](https://helpx.adobe.com/kr/enterprise/using/create-nul-packages.html) 및 [제품 프로필](https://helpx.adobe.com/kr/enterprise/using/manage-product-profiles.html#create-product-profile)을 참조하세요.
- **공유 장치 라이선스:** [추가된 사용자](https://helpx.adobe.com/kr/enterprise/using/sdl-deployment-guide.html#add-users-admin-console)는 **조직 사용자만 액세스할 수 있는 구성된 공유 장치를 사용할 수 있습니다**. 자세한 내용은 [SDL 패키지 만들기](https://helpx.adobe.com/kr/enterprise/using/create-sdl-packages.html)를 참조하십시오.

### 패키지 배포

패키지를 만든 후 다음 방법 중 하나를 사용하여 클라이언트 컴퓨터에 배포합니다.

- 클라이언트 시스템으로 이동하여 패키지 파일(Windows 또는 macOS)을 두 번 클릭합니다.
- Windows 명령 프롬프트 또는 macOS 터미널을 사용합니다.
- 타사 도구 사용:
   - [Microsoft Intune](https://helpx.adobe.com/kr/enterprise/kb/deploy-packages-using-ms-intune.html)
   - [SCCM(Microsoft System Center Configuration Manager)](https://helpx.adobe.com/kr/enterprise/kb/deploy-packages-using-sccm.html)
   - [Apple 원격 데스크톱(ARD)](https://helpx.adobe.com/kr/enterprise/kb/deploy-packages-using-ard.html)
   - [JAMF Pro](https://helpx.adobe.com/kr/enterprise/kb/deploy-packages-using-jamf-pro.html)
   - [뭉키](https://helpx.adobe.com/kr/enterprise/kb/deploy-packages-using-munki.html)

## 관련 읽기

- [사용자 관리 | 개별적으로](https://helpx.adobe.com/kr/enterprise/using/manage-users-individually.html)
- [사용자 관리 | 일괄 CSV 업로드](https://helpx.adobe.com/kr/enterprise/using/bulk-upload-users.html)
- [디렉터리 사용자 관리](https://helpx.adobe.com/kr/enterprise/using/manage-directory-users.html)
- [관리 콘솔](https://helpx.adobe.com/kr/enterprise/using/admin-console.html)
- [사용자를 제품 프로필에 할당(기업 및 기관의 경우)](https://helpx.adobe.com/kr/enterprise/using/manage-product-profiles.html#assign-users)
- [팀 사용자에게 라이선스 할당](https://helpx.adobe.com/kr/enterprise/using/assign-licenses-to-teams-users.html)
- [비즈니스 저장소 모델](https://helpx.adobe.com/kr/enterprise/kb/business-storage-model-introduction.html)