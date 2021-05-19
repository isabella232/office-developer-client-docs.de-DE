---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: 007a44d13565889b4775f2d3fe9979685e1878b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425064"
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
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
| *Platzhaltermitglied*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhaltermitglied*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhaltermitglied*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhaltermitglied*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhaltermitglied*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhaltermitglied*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[GetAccountInfo](iolkaccount-getaccountinfo.md) <br/> |Ruft den Typ und die Kategorien des angegebenen Kontos ab.  <br/> |
|[GetProp](iolkaccount-getprop.md) <br/> |Ruft den Wert der angegebenen Account-Eigenschaft ab. Weitere Informationen finden Sie in der Tabelle Eigenschaften unten.  <br/> |
|[SetProp](iolkaccount-setprop.md) <br/> |Legt den Wert der angegebenen Account-Eigenschaft fest. Weitere Informationen finden Sie in der Tabelle Eigenschaften unten.  <br/> |
| *Platzhaltermitglied*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhaltermitglied*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhaltermitglied*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[FreeMemory](iolkaccount-freememory.md) <br/> |Gibt den von der **IOlkAccount-Schnittstelle zugewiesenen Arbeitsspeicher** frei.  <br/> |
| *Platzhaltermitglied*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |Übergeht Änderungen am Kontoobjekt, indem in den Registrierungsspeicher geschrieben wird.  <br/> |
   
## <a name="properties"></a>Eigenschaften

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Stellt die Eintrags-ID des Standardzustellungsordners für das Konto dar.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Stellt die Eintrags-ID des Standardzustellungsspeichers für das Konto dar.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Gibt den Kontobezeichner in Outlook 2000 und früheren Versionen von Outlook.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |True, wenn es sich bei dem Konto um ein Microsoft-Exchange handelt.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Gibt den Kontobezeichner in Versionen von Outlook seit Outlook 2002 zurück.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Gibt den Kontonamen zurück.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Ruft den eindeutigen Bezeichner (Unique Identifier, UID) für den Profilabschnitt ab, in dem die Kontoeinstellungen gespeichert sind.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Gibt den Kontostempel "Senden" zurück.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto dar.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Gibt den Kontostempel zurück.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Gibt den Anzeigenamen des Benutzers zurück.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Gibt die E-Mail-Adresse für das Konto an.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Stellt eine [ACCT_BIN](acct_bin.md) dar, die die UID eines Exchange enthält.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Ruft die Adressbucheintrags-ID für das Konto ab oder legt sie fest.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Stellt Transporteinstellungen dar, die Microsoft Outlook verwendet, um die erforderlichen Synchronisierungsaufgaben zu ermitteln und die benutzeroberflächenelemente zu deaktivieren, die vom Konto nicht unterstützt werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Schnittstelle wird von **IOlkAccountManager::FindAccount** zurückgegeben, wenn nach einem Konto gesucht wird, das **IOlkAccount** und **IOlkEnum::GetNext** unterstützt, wenn das nächste Konto in einem Enumerationsmodul angezeigt wird. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

