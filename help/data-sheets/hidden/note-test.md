---
description: 위젯 Data Warehouse에 연결 - 제품 설명서
title: 위젯 Data Warehouse에 연결
hide: true
hidefromtoc: true
exl-id: d6a7cff5-08f9-4c93-8765-46e692feaa0d
source-git-commit: 4145889fe291e80fa8d295368ead3e0075917e86
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 0%

---

# 위젯 Data Warehouse에 연결 {#connecting-to-the-widget-data-warehouse}

## 새 테스트

6월 27일

<ol><li>'{{name}}' 변수를 사용하십시오.</li></ol>

<ol><li>&lbrace;&lbrace;<code>name</code>&rbrace;&rbrace; 변수를 사용합니다.</li></ol>

## 중첩 테스트

**처음**

>[!NOTE]
>
>다음을 삭제할 수 없습니다.
>
>* 기본 제공 상태 계획, 현재 및 완료. 이름을 업데이트하고, 색상을 편집하고, 잠그거나 잠금을 해제할 수 있지만 삭제할 수는 없습니다.
>* 시스템에서 하나 이상의 객체에 대해 승인 보류 중인 상태입니다.

**Second**

>[!NOTE]
>
>다음을 삭제할 수 없습니다.
>
>* 기본 제공 상태 계획, 현재 및 완료. 이름을 업데이트하고, 색상을 편집하고, 잠그거나 잠금을 해제할 수 있지만 삭제할 수는 없습니다.
>
>  다음 사이
>
>* 시스템에서 하나 이상의 객체에 대해 승인 보류 중인 상태입니다.

## 위젯 액세스 링크 {#widget-access-link}

위젯 데이터 웨어하우스에 액세스하려면 위젯 계정의 특정 URL로 이동해야 합니다.  이 액세스 링크는 Marketo Measure에 로그인한 다음 아래 단계에 따라 Data Warehouse 정보 페이지로 이동하여 찾을 수 있습니다.

1. Marketo Measure의 페이지 맨 위에서 **내 계정** > **설정**&#x200B;을 클릭합니다.

   ![](assets/adobe-logo-old.png)

1. 왼쪽 메뉴에서 보안 아래의 **Data Warehouse**&#x200B;을(를) 클릭합니다.

   ![](assets/adobe-logo-old.png)

1. 이 페이지에서 Widget Data Warehouse 및 사용자 이름에 대한 링크를 찾을 수 있습니다.

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >이는 개별 사용자가 아닌 조직에서 사용할 수 있는 읽기 전용 계정입니다. 조직 내에서 Marketo Measure에 액세스할 수 있는 모든 사용자는 이 계정을 사용하여 Widget Data Warehouse reader 계정에 로그인할 수 있습니다.

1. 위젯 URL에 제공된 링크를 클릭하면 사용자 이름과 암호를 입력할 수 있는 위젯 로그인 페이지로 이동합니다. _암호가 없는 경우 아래 단계를 참조하여 암호를 재설정하십시오_.

   ![](assets/adobe-logo-old.png)

1. 로그인하고 나면 페이지 상단의 **워크시트**&#x200B;를 클릭합니다.

   ![](assets/adobe-logo-old.png)

1. BIZIBLE_ROI_V3 데이터베이스 개체는 화면 왼쪽에 있습니다.  쿼리 창 상단의 드롭다운 옵션에서 웨어하우스, 데이터베이스 및 스키마를 입력합니다.  각 옵션에는 하나만 있어야 합니다.  이제 위젯 쿼리 편집기 내에서 쿼리를 실행할 준비가 되었습니다.

   ![](assets/adobe-logo-old.png)

## 암호 재설정 {#reset-your-password}

Marketo Measure은 위젯 로그인 암호에 액세스할 수 없습니다.  암호를 재설정해야 하는 경우 Data Warehouse 정보 페이지에서 암호 재설정 버튼을 클릭하고 지침을 따릅니다. 임시 암호가 UI에 즉시 표시됩니다. 다음 Data Warehouse 로그인 시 암호를 만들라는 메시지가 표시됩니다.

>[!NOTE]
>
>* 암호를 재설정하면 현재 로그인한 사용자뿐만 아니라 조직의 모든 Marketo Measure 사용자에 대해 재설정됩니다.
>* UI에는 임시 암호만 표시됩니다. 이메일이 전송되지 않습니다.

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## 서드파티 도구를 통해 위젯에 연결 {#connecting-to-widget-via-third-party-tools}

위젯 데이터 웨어하우스를 타사 도구에 연결하려면 몇 가지 정보를 입력해야 합니다.

>[!NOTE]
>
>각 도구에는 서로 다른 연결 요구 사항이 있습니다. 연결하려는 특정 도구에 대한 설명서를 참조하는 것이 좋습니다.

* **URI**(항상 필요)
   * 위젯 계정의 도메인 이름입니다.  위젯 로그인 링크의 일부에 포함되어 있습니다.
* **사용자 이름**(항상 필요)
   * 사용자 이름은 Marketo Measure의 Data Warehouse 정보 페이지에 나열됩니다.
* **암호**(항상 필요)
   * 위젯 계정에 처음 로그인할 때 설정한 암호입니다.  암호를 재설정하려면 위에 설명된 단계를 참조하십시오.
* **데이터베이스 이름**(항상 필요한 것은 아님)
   * 데이터베이스는 위젯에 데이터를 저장하는 것입니다. 스토리지 리소스입니다. 데이터베이스 이름은 Marketo Measure의 Data Warehouse 정보 페이지에 나열됩니다.
* **웨어하우스 이름**(항상 필요한 것은 아님)
   * 웨어하우스는 위젯에서 쿼리를 실행하는 것입니다. 계산 리소스입니다.  웨어하우스 이름은 Marketo Measure의 Data Warehouse 정보 페이지에 나열됩니다.

  ![](assets/adobe-logo-old.png)

## 위젯 Data Warehouse 직접 공유 {#widget-data-warehouse-direct-share}

**요구 사항**

Marketo Measure에서 Data Warehouse에 대한 직접 공유를 설정하려면 다음 요구 사항을 충족해야 합니다.

* 고유한 위젯 인스턴스가 있습니다.
* 위젯 인스턴스는 Azure East US 2 위젯 영역에 있습니다.
* Marketo Measure에 위젯 계정 ID를 제공합니다.

**제한 사항**

Marketo Measure에서 직접 공유를 설정하려면 액세스를 요청하는 계정이 Azure East US 2에 있어야 합니다. Widget은 지역 간에 데이터 복제 솔루션을 제공하지만 Azure East US 2 지역에서만 데이터를 호스팅하므로 처음부터 이를 지원하지 않습니다. 이 기능은 Azure 동부 미국 2에서 고유한 인스턴스를 설정하고 [지역 간에 데이터를 복제](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"}하여 기존 인스턴스에 복제할 수 있습니다. 하지만 위젯의 데이터 복제 기능은 테이블에서만 사용할 수 있으므로 이 기능을 사용하려면 먼저 보기에서 자신의 테이블로 데이터를 복사해야 합니다.

**공유 액세스**

제공된 계정 ID에 대해 공유가 만들어지면 데이터에 액세스하려면 위젯 인스턴스 내에서 [설정 단계](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}를 완료해야 합니다.

>[!NOTE]
>
>원하는 데이터베이스 이름을 선택할 수 있습니다. 위젯 인스턴스에 존재하는 한 선택한 모든 규칙에 권한을 할당할 수 있습니다.

* 계정 관리자 역할 사용

```
USE ROLE ACCOUNTADMIN
```

* 사용 가능한 공유 보기(부여된 공유 이름이 표시됨)

```
SHOW SHARES
```

* 공유에 대한 데이터베이스 만들기

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* 공유 데이터베이스에 대한 권한 부여

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

위젯 UI에서 이러한 단계를 수행하는 자세한 지침 및 단계는 [위젯의 설명서](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}를 직접 참조하십시오.
