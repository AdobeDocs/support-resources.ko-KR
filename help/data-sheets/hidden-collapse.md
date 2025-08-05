---
title: 섹션 버그 접기
description: UGP-13446 축소 가능한 섹션은 포함된 페이지 탭으로 인해 렌더링되지 않습니다.
hide: true
hidefromtoc: true
source-git-commit: f2d8eb9125df5f542c1ed075348586965f4adaad
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 7%

---

# 축소 가능한 섹션

<http://jira.corp.adobe.com/browse/UGP-13446> UGP-13446 축소 가능한 섹션은 포함된 페이지 탭으로 인해 렌더링되지 않습니다.

## 예

첫 번째는 페이지 탭으로, 두 번째는 페이지 탭으로

### 옵션 2: 페이지 탭 사용

+++ 6.5.18.0 - 6.5.22.0용 수동 핫픽스 설치

**1단계: 핫픽스 패키지 다운로드 및 추출**

- Adobe 소프트웨어 배포 포털에서 [ - 6.5.226.5.18.0용 ](https://www.adobe.com/kr/)핫픽스를 다운로드합니다.
- 로컬에서 추출

**2단계: 올바른 버전 폴더로 이동**

- 환경에 설치된 서비스 팩 버전에 따라 일치하는 폴더로 이동합니다.

  서비스 팩 20의 예 폴더는 다음과 같습니다.

  ```
  <extracted-hotfix>/SP20/
  ```

**3단계: 배포 디렉터리 찾기**

- JEE 서버의 AEM Forms에서

  ```
  [AEM installation directory]/deploy
  ```

  예: `adobe/adobe-experience-manager-forms/deploy`



**4단계: EAR 파일 업데이트 및 바꾸기**

>[!BEGINTABS]

>[!TAB JBos]

1. `adobe-core-jboss.ear`을(를) 열고 `adminui.war`을(를) 다음으로 바꾸기

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adminui.war
   ```

   예, `adobe-xxe-configuration-hotfix/SP20/jboss/adminui.war`

1. `adobe-core-jboss.ear` 내에서 `lib/` 폴더로 이동하여 `adobe-uisupport.jar`을(를) 다음으로 바꾸기:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   예, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. 귀를 막아라. 변경 사항이 제대로 저장되었는지 확인합니다.


1. `adobe-edcserver-jboss.ear` 바꾸기

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-edcserver-jboss.ear
   ```

   예, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-edcserver-jboss.ear`

1. `adobe-forms-jboss.ear` 바꾸기

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-forms-jboss.ear
   ```

   예, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-forms-jboss.ear`



>[!TAB WebLogic]

1. `adobe-core-weblogic.ear`을(를) 열고 `adminui.war`을(를) 다음으로 바꾸기

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adminui.war
   ```

   예, `adobe-xxe-configuration-hotfix/SP20/weblogic/adminui.war`

1. `adobe-core-weblogic.ear` 내에서 `adobe-uisupport.jar`을(를) 다음으로 바꾸기:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   예, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. 귀를 막아라. 변경 사항이 제대로 저장되었는지 확인합니다.


1. `adobe-edcserver-weblogic.ear` 바꾸기

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-edcserver-weblogic.ear
   ```

   예, `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-edcserver-weblogic.ear`

1. `adobe-forms-weblogic.ear` 바꾸기

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-forms-weblogic.ear
   ```

   예, `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-forms-weblogic.ear`

>[!TAB WebSphere]

1. `adobe-core-websphere.ear`을(를) 열고 `adminui.war`을(를) 다음으로 바꾸기

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adminui.war
   ```

   예, `adobe-xxe-configuration-hotfix/SP20/websphere/adminui.war`

1. `adobe-core-websphere.ear` 내에서 `adobe-uisupport.jar`을(를) 다음으로 바꾸기:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   예, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. 귀를 막아라. 변경 사항이 제대로 저장되었는지 확인합니다.


1. `adobe-edcserver-websphere.ear` 바꾸기

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-edcserver-websphere.ear
   ```

   예, `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-edcserver-websphere.ear`

1. `adobe-forms-websphere.ear` 바꾸기

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-forms-websphere.ear
   ```

   예, `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-forms-websphere.ear`

>[!ENDTABS]



**5단계: `adobe-rightsmanagement-<appserver>-dsc.jar`파일을**(으)로 업데이트

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

예, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**6단계: WebSphere 및 WebLogic에서 문서 보안을 위한 추가 구성**:

Document Security(이전의 Rights Management)를 사용하는 경우 AEM Forms 서버를 시작하기 전에 다음 Java 시스템 속성(JVM 인수)을 설정하십시오.

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**7단계: 구성 관리자 다시 실행**

- 구성 관리자를 실행하여 업데이트된 EAR을 다시 배포하고 핫픽스를 적용합니다

+++

### 옵션 2: 페이지 탭 없음

+++ 6.5.18.0 - 6.5.22.0용 수동 핫픽스 설치

**1단계: 핫픽스 패키지 다운로드 및 추출**

- Adobe 소프트웨어 배포 포털에서 [ - 6.5.226.5.18.0용 ](https://www.adobe.com/kr/)핫픽스를 다운로드합니다.
- 로컬에서 추출

**2단계: 올바른 버전 폴더로 이동**

- 환경에 설치된 서비스 팩 버전에 따라 일치하는 폴더로 이동합니다.

  서비스 팩 20의 예 폴더는 다음과 같습니다.

  ```
  <extracted-hotfix>/SP20/
  ```

**3단계: 배포 디렉터리 찾기**

- JEE 서버의 AEM Forms에서

  ```
  [AEM installation directory]/deploy
  ```

  예: `adobe/adobe-experience-manager-forms/deploy`



**4단계: EAR 파일 업데이트 및 바꾸기**

페이지 탭 삭제됨

**5단계: `adobe-rightsmanagement-<appserver>-dsc.jar`파일을**(으)로 업데이트

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

예, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**6단계: WebSphere 및 WebLogic에서 문서 보안을 위한 추가 구성**:

Document Security(이전의 Rights Management)를 사용하는 경우 AEM Forms 서버를 시작하기 전에 다음 Java 시스템 속성(JVM 인수)을 설정하십시오.

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**7단계: 구성 관리자 다시 실행**

- 구성 관리자를 실행하여 업데이트된 EAR을 다시 배포하고 핫픽스를 적용합니다

+++

Fin
