---
title: ID 및 SSO(Single Sign-On) 설정
description: 조직 시스템 관리자가 Adobe ID, Enterprise ID 또는 Federated ID을 사용하여 Adobe Admin Console에서 사용자 ID와 SSO(Single Sign-On)를 설정하는 방법을 알아봅니다.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 0c2992946f1cdbbcfb44a2baf37888bd05b2253b
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 1%

---

# ID 및 SSO(Single Sign-On) 설정

**적용 대상:** Enterprise

Adobe Admin Console에서 ID를 설정하는 방법을 알아봅니다. Adobe ID, Enterprise ID 및 Federated ID을 비교하고 Adobe 앱에 대한 보안 액세스를 위해 SSO(Single Sign-On)를 구성합니다.

직원이 기존 조직 자격 증명으로 [로그인](https://adminconsole.adobe.com/settings/)할 수 있도록 ID를 구성하고 SSO(Single Sign-On)를 설정하십시오.

다음은 [ID 및 SSO(YouTube) 설정](https://youtu.be/V57lU4zaSBs)방법을 보여주는 비디오 튜토리얼입니다.

## 주요 용어 및 개념

### 디렉토리

Admin Console의 디렉토리는 사용자와 같은 리소스 및 인증과 같은 정책을 보유하는 엔티티입니다. 이러한 디렉토리는 LDAP 또는 Active 디렉토리와 유사합니다.

### ID 공급자(IdP)

ID 공급자(IdP)는 다음과 같은 조직의 ID 공급자입니다.

- Active Directory
- Microsoft Azure
- Ping
- 옥타
- 공통적
- 쉽볼렛

### 관련 담당자

| 역할 | 책임 |
|------|----------------|
| 시스템 관리자 | IdP 디렉터리 관리자 및 DNS 관리자와 함께 Admin Console에서 ID를 설정합니다. |
| DNS 관리자 | DNS 토큰을 업데이트하여 도메인 소유권의 유효성을 검사합니다. |
| IdP(ID 공급자) 디렉토리 관리자 | IdP 포털 및 관련 커넥터를 처리합니다. |

### Adobe ID

최종 사용자가 생성, 소유 및 관리합니다. Adobe에서 인증을 수행하고 최종 사용자가 id를 관리합니다. [저장소 모델](https://helpx.adobe.com/enterprise/using/storage-for-business.html)에 따라 사용자 또는 기업이 파일 및 데이터를 계속 제어합니다.

엔터프라이즈 스토리지 모델로 업데이트된 조직의 경우, 자산과 데이터는 조직에서 제어합니다. 업데이트하지 않은 조직의 경우 개인이 Adobe ID 자산을 소유 및 제어합니다.

### Enterprise ID

조직에서 만들고, 소유하고, 관리합니다. Adobe은 Enterprise ID을 호스팅하고 인증을 수행하지만 조직에서는 Enterprise ID을 유지 관리합니다. 관리자는 Enterprise ID을 만들고 사용자에게 발급합니다. 관리자는 계정을 인계받거나 Enterprise ID을 삭제하여 관련 데이터에 대한 액세스를 영구적으로 차단함으로써 제품 및 서비스에 대한 액세스를 취소할 수 있습니다. 자세한 내용을 보려면 [여기](https://helpx.adobe.com/enterprise/using/setup-enterprise-id.html)를 클릭하세요.

### Federated ID

조직에서 만들고 소유하고 페더레이션을 통해 Enterprise 디렉터리에 연결됩니다. 이 조직은 SAML2 ID 공급자(IdP)를 통해 자격 증명을 관리하고 Single Sign-On을 처리합니다.

다음은 Federated ID를 권장하는 몇 가지 요구 사항 및 시나리오입니다.

- 조직의 엔터프라이즈 디렉토리를 기반으로 사용자를 프로비저닝하려는 경우
- 사용자 인증을 관리하려는 경우.
- 사용자가 사용할 수 있는 앱 및 서비스에 대해 엄격한 제어를 유지해야 하는 경우.

## SSO(Single Sign-On) 없이 ID 설정

조직이 현재 다른 애플리케이션에서 SSO를 사용하고 있지 않은 경우 Adobe ID 또는 Enterprise ID을 사용할 수 있습니다.

## Adobe ID 사용

Adobe이 모든 조직을 [엔터프라이즈 스토리지 모델](https://helpx.adobe.com/enterprise/using/storage-for-business.html)&#x200B;(으)로 업데이트하는 중입니다. 이를 통해 조직은 사용자의 에셋과 데이터를 보다 세밀하게 제어할 수 있습니다.

Admin Console에 [사용자를 추가](https://helpx.adobe.com/kr/enterprise/using/users.html)하세요.

## Enterprise ID으로 ID 설정

SSO를 사용하지 않고 사용자의 데이터를 보다 세밀하게 제어하려면 Enterprise ID 디렉토리를 설정할 수 있습니다. 관리자만 Enterprise ID을 만들고 사용자에게 발급합니다.

Enterprise ID 디렉터리를 만들기 위한 요구 사항 및 단계는 [Enterprise ID으로 조직 설정](https://helpx.adobe.com/enterprise/using/setup-enterprise-id.html)을 참조하십시오.

## SSO(Single Sign-On)를 사용하여 ID 설정

SSO를 사용하려면 Federated ID 계정으로 사용자 ID를 설정해야 합니다.

다음과 같은 경우에는 Federated ID를 사용하는 것이 좋습니다.

- 사용자가 사용할 수 있는 앱 및 서비스에 대해 엄격한 제어를 유지해야 합니다.
- 사용자 인증을 관리하려는 경우
- 조직의 엔터프라이즈 디렉터리를 기반으로 사용자를 프로비저닝하려고 합니다.

## 새 SSO 통합 설정

Microsoft Azure AD, Google과 같이 인기 있는 ID 공급자를 사용하거나 다른 SAML 기반 IdP를 사용하여 조직과 Adobe 제품 간에 SSO를 설정할 수 있습니다.

**Azure AD**(권장) - [Azure AD 커넥터와 SSO 및 사용자 동기화 설정](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html)

**다른 SAML IdP** - [다른 SAML 공급자와 SSO 설정](https://helpx.adobe.com/enterprise/using/create-directory.html)

**Google**(권장) - [Google 커넥터를 사용하여 SSO 및 사용자 동기화 설정](https://helpx.adobe.com/enterprise/using/setup-sso-google.html)

## 기존 SSO 설정 관리

조직과 Adobe 간에 SSO를 설정한 후 다음을 사용하여 설정을 관리하고 변경하십시오.

도메인 및 디렉터리를 관리하는 방법을 알아봅니다.

- [사용자 관리](https://helpx.adobe.com/kr/enterprise/using/users.html) 및 [그룹](https://helpx.adobe.com/enterprise/using/user-groups..html)
- [도메인을 디렉터리에 연결](https://helpx.adobe.com/enterprise/using/add-domains-directories.html#link-domains-to-directoies)하여 앱, 서비스 및 설정에 대한 사용자 액세스를 제어합니다.
- 다른 조직에서 요구하는 도메인을 사용하려면 [디렉터리 트러스트를 관리합니다](https://helpx.adobe.com/enterprise/using/directory-trust.html)

ID 공급자를 변경하는 방법에 대해 알아봅니다.

- 사용자의 작업을 중단하지 않고 [IdP 변경](https://helpx.adobe.com/enterprise/using/migrate-authentication-provider.html)
- [도메인 간 이동](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html#move-domains-across-directories)
- [기존 디렉터리 사용자 제거](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)
- [이전/미청구 도메인 및 빈 디렉터리 삭제](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html#delete)

## 오류 및 일반적인 질문

SSO 설정 및 관리 시 발생할 수 있는 일반적인 질문 및 오류에 대한 해결 방법:

### Azure AD - FAQ 및 문제 해결

#### FAQ

- [Azure AD 커넥터 FAQ](https://helpx.adobe.com/enterprise/using/azure-ad-connector-faq.html)
- [디렉터리 및 도메인을 삭제하는 방법](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#Deletedirectoriesandremovedomains)

#### 문제 해결

- [사용자 액세스 거부](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#sync-issues)
- [동기화 문제](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#sync-issues)

### 기타 SAML IdP - FAQ 및 문제 해결

#### FAQ

[SAML 통합 FAQ](https://helpx.adobe.com/enterprise/using/sso-faq.html)

#### 문제 해결

- [일반 SSO 문제 해결](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html)
- [&quot;액세스 거부&quot; 오류](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html#Error_Access_Denied_logging_in)
- [&quot;다른 사용자가 현재 로그인되어 있습니다.&quot; 오류](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html#ErrorAnotheruseriscurrentlyloggedin)
- [SAML 추적 수행](https://helpx.adobe.com/enterprise/kb/perform-a-saml-trace.html)

### GOOGLE - FAQ

- [Google 커넥터 FAQ](https://helpx.adobe.com/enterprise/using/google-federation-faq.html)
- [디렉터리 및 도메인을 삭제하는 방법](https://helpx.adobe.com/enterprise/using/setup-sso-google.html#Deletedirectoriesandremovedomains)

## 대화에 참여

공동 작업하고, 질문하고, 다른 관리자와 대화하려면 [Enterprise 및 Teams 커뮤니티](https://www.adobe.com/go/entcom)를 사용하세요.

## 법적 및 개인 정보 보호

- [법적 고지 사항](https://helpx.adobe.com/legal/legal-notices.html)
- [온라인 개인정보 처리방침](https://www.adobe.com/kr/privacy.html)
