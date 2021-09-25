---
title: Informationen zur Kontoverwaltungs-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'Die Kontoverwaltungs-API bietet Zugriff auf Kontoinformationen und unterstützt Benachrichtigungen über Kontoänderungen. Als Clients dieser API führen E-Mail-Anbieter Folgendes aus:'
ms.openlocfilehash: 6711fc3297c803c0af3115e31a36255dafe3d028
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596708"
---
# <a name="about-the-account-management-api"></a>Informationen zur Kontoverwaltungs-API

Die Kontoverwaltungs-API bietet Zugriff auf Kontoinformationen und unterstützt Benachrichtigungen über Kontoänderungen. Als Clients dieser API führen E-Mail-Anbieter Folgendes aus:
  
1. Verwenden Sie [IOlkAccountManager,](iolkaccountmanager.md) um den Zugriff auf Konten zu verwalten und Benachrichtigungen zu Kontoänderungen einzurichten. 
    
2. Implementieren und verwenden [Sie IOlkAccountNotify,](iolkaccountnotify.md) um Benachrichtigungen über Kontoänderungen zu senden. 
    
3. Verwenden Sie [IOlkEnum](iolkenum.md) zum Aufzählen von Konten. 
    
4. Verwenden Sie [IOlkAccount,](iolkaccount.md) um Eigenschaften und andere Informationen zu einem Konto abzurufen und festzulegen. Clients erhalten diese Schnittstelle über [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) oder [IOlkEnum::GetNext,](iolkenum-getnext.md) um auf ein einzelnes Konto zuzugreifen. 
    
5. Implementieren und verwenden Sie [IOlkAccountHelper,](iolkaccounthelper.md) um die Hilfsfunktionen des Konto-Managers bereitzustellen, einschließlich des Abrufens des Profilnamens eines Kontos und der aktuellen MAPI-Sitzung. 
    
6. Implementieren und verwenden [Sie IOlkErrorUnknown,](iolkerrorunknown.md) um zusätzliche Informationen zu einem Fehler in **IOlkAccountManager**, **IOlkAccountNotify** und **IOlkAccount** bereitzustellen. 

##  <a name="account-management-api-components"></a>Kontoverwaltungs-API-Komponenten

Die Kontoverwaltungs-API stellt die folgenden Definitionen, Datentypen, Schnittstellen, benannten Eigenschaften und Eigenschaften bereit.
  
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
    

