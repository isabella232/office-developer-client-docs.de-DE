---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: 07b2669a88010ccb8d76d077f40d61ffdbe50d99
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625693"
---
# <a name="iolkaccount"></a>IOlkAccount

Unterstützt das Abrufen und Festlegen von Eigenschaften und anderen Informationen zu einem Konto.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt von:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Bereitgestellt von:  <br/> |[IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) und [IOlkEnum::GetNext](iolkenum-getnext.md) <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkAccount  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[GetAccountInfo](iolkaccount-getaccountinfo.md) <br/> |Ruft den Typ und die Kategorien des angegebenen Kontos ab.  <br/> |
|[GetProp](iolkaccount-getprop.md) <br/> |Ruft den Wert der angegebenen Kontoeigenschaft ab. Weitere Informationen finden Sie unten in der Tabelle "Eigenschaften".  <br/> |
|[SetProp](iolkaccount-setprop.md) <br/> |Legt den Wert der angegebenen Kontoeigenschaft fest. Weitere Informationen finden Sie unten in der Tabelle "Eigenschaften".  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[FreeMemory](iolkaccount-freememory.md) <br/> |Gibt von der **IOlkAccount-Schnittstelle** zugewiesenen Speicher frei.  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |Führt einen Commit für Änderungen am Kontoobjekt durch Schreiben in den Registrierungsspeicher aus.  <br/> |
   
## <a name="properties"></a>Eigenschaften

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Stellt die Eintrags-ID des Standardzustellungsordners für das Konto dar.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Stellt die Eintrags-ID des Standardzustellungsspeichers für das Konto dar.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Gibt den Kontobezeichner in Outlook 2000 und früheren Versionen von Outlook zurück.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |True, wenn es sich bei dem Konto um ein Microsoft Exchange-Konto handelt.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Gibt den Kontobezeichner in Versionen von Outlook seit Outlook 2002 zurück.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Gibt den Kontonamen zurück.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Ruft den eindeutigen Bezeichner (UID) für den Profilabschnitt ab, in dem die Kontoeinstellungen gespeichert sind.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Gibt den Stempel "Senden" des Kontos zurück.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto dar.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Gibt den Kontostempel zurück.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Gibt den Anzeigenamen des Benutzers zurück.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Gibt die E-Mail-Adresse für das Konto an.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Stellt eine [ACCT_BIN](acct_bin.md) Struktur dar, die die UID eines Exchange Kontos enthält.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Ruft die Adressbucheintrags-ID für das Konto ab oder legt sie fest.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Stellt Transporteinstellungen dar, die Microsoft Outlook verwendet, um die erforderlichen Synchronisierungsaufgaben zu ermitteln und die Benutzeroberflächenelemente zu deaktivieren, die das Konto nicht unterstützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wird von **IOlkAccountManager::FindAccount** zurückgegeben, wenn nach einem Konto gesucht wird, das **IOlkAccount** und **IOlkEnum::GetNext** unterstützt, wenn das nächste Konto in einem Enumerator abgerufen wird. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

