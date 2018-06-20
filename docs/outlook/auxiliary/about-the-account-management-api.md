---
title: Informationen zu der Konto-Management-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'Der Konto-Verwaltungs-API ermöglicht den Zugriff auf Kontoinformationen und Benachrichtigungen von kontoänderungen unterstützt. E-Mail-Anbieter Sie als dieser API-Clients wie folgt:'
ms.openlocfilehash: 678143def25395c47f1c17cc99dcdcd1fb145e1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790920"
---
# <a name="about-the-account-management-api"></a>Informationen zu der Konto-Management-API

Der Konto-Verwaltungs-API ermöglicht den Zugriff auf Kontoinformationen und Benachrichtigungen von kontoänderungen unterstützt. E-Mail-Anbieter Sie als dieser API-Clients wie folgt:
  
1. Verwenden Sie zum Verwalten des Zugriffs auf Konten und Einrichten von Benachrichtigungen bezüglich kontoänderungen [IOlkAccountManager](iolkaccountmanager.md) . 
    
2. Implementieren und [IOlkAccountNotify](iolkaccountnotify.md) zum Senden von Benachrichtigungen bezüglich kontoänderungen verwenden. 
    
3. Verwenden Sie [IOlkEnum](iolkenum.md) zum Aufzählen von Konten. 
    
4. Verwenden Sie [IOlkAccount](iolkaccount.md) zum Abrufen und Festlegen von Eigenschaften und andere Informationen über ein Konto an. Clients erhalten diese Schnittstelle über [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) oder [IOlkEnum::GetNext](iolkenum-getnext.md) ein individuelles Konto Zugriff auf. 
    
5. Implementieren und [IOlkAccountHelper](iolkaccounthelper.md) zum Bereitstellen der Konto-Manager-Hilfsprogramm-Funktionen, einschließlich erste ein Konto Profilname und der aktuellen MAPI-Sitzung verwenden. 
    
6. Implementieren Sie und verwenden Sie [IOlkErrorUnknown](iolkerrorunknown.md) , um zusätzliche Informationen zu einem Fehler in **IOlkAccountManager**, **IOlkAccountNotify**und **IOlkAccount**bereitzustellen. 

##  <a name="account-management-api-components"></a>Konto-Verwaltungs-API-Komponenten

Die Konto-Management-API bietet die folgenden Definitionen, die Datentypen, die Schnittstellen, die mit dem Namen, und Eigenschaften.
  
### <a name="definitions"></a>Definitionen
  
- [Konstanten (Account Management API)](constants-account-management-api.md)
    
### <a name="data-types"></a>Datentypen
  
- [ACCT_BIN](acct_bin.md)
    
- [ACCT_VARIANT](acct_variant.md)
    
### <a name="interfaces"></a>Schnittstellen
  
- [IOlkAccount](iolkaccount.md)
    
- [IOlkAccountHelper](iolkaccounthelper.md)
    
- [IOlkAccountManager](iolkaccountmanager.md)
    
- [IOlkAccountNotify](iolkaccountnotify.md)
    
- [IOlkEnum](iolkenum.md)
    
- [IOlkErrorUnknown](iolkerrorunknown.md)
    
### <a name="named-properties"></a>Benannte Eigenschaften
  
- [PidLidInternetAccountName](pidlidinternetaccountname.md)
    
- [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a>Eigenschaften
  
- [PidTagNextSendAcct](pidtagnextsendacct.md)
    
- [PidTagPrimarySendAccount](pidtagprimarysendaccount.md)
    
- [PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md)
    
- [PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md)
    
- [PROP_ACCT_ID](prop_acct_id.md)
    
- [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)
    
- [PROP_ACCT_NAME](prop_acct_name.md)
    
- [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md)
    
- [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md)
    
- [PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md)
    
- [PROP_ACCT_STAMP](prop_acct_stamp.md)
    
- [PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)
    
- [PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md)
    
- [PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md)
    
- [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md)
    
- [PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md)
    

