---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: dc802d8fef0d90672428c8bfa3662a2734637d05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791068"
---
# <a name="iolkaccount"></a>IOlkAccount

Unterstützt das Abrufen und Festlegen von Eigenschaften und andere Informationen über ein Konto.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Bereitgestellt von:  <br/> |[IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) und [IOlkEnum::GetNext](iolkenum-getnext.md) <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkAccount  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|[GetAccountInfo](iolkaccount-getaccountinfo.md) <br/> |Ruft den Typ und die Kategorien für das angegebene Konto.  <br/> |
|[GetProp](iolkaccount-getprop.md) <br/> |Ruft den Wert der Eigenschaft angegebene Konto. Finden Sie unter Eigenschaften in der folgenden Tabelle.  <br/> |
|[SetProp](iolkaccount-setprop.md) <br/> |Legt den Wert der Eigenschaft angegebene Konto. Finden Sie unter Eigenschaften in der folgenden Tabelle.  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|[Freier Speicher](iolkaccount-freememory.md) <br/> |Durch die Schnittstelle **IOlkAccount** Arbeitsspeicher frei.  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |Führt ein Commit für Änderungen an das Account-Objekt durch Schreiben der Registrierung gespeichert.  <br/> |
   
## <a name="properties"></a>Eigenschaften

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Stellt die Eintrags-ID des Standardordners Übermittlung für das Konto an.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Stellt die Eintrags-ID der standardmäßiger übermittlungsspeicher für das Konto an.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Gibt die Konto-ID in Outlook 2000 und früheren Versionen von Outlook zurück.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |True, wenn das Konto ein Microsoft Exchange-Konto handelt.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Gibt die Konto-ID in Versionen von Outlook seit Outlook 2002 zurück.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Gibt den Kontonamen an.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Ruft den eindeutigen Bezeichner (UID) für den Benutzerprofildienst-Abschnitt, in dem die Vorgaben Konto gespeichert.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Gibt den Konto-Stempel "Senden" zurück.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto an.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Gibt den Stempel Konto zurück.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Gibt den Anzeigenamen des Benutzers zurück.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Gibt die e-Mail-Adresse für das Konto an.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Stellt eine [ACCT_BIN](acct_bin.md) -Struktur, die UID des ein Exchange-Konto enthält.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Ruft ab oder legt die Address Book Eintrags-ID für das Konto.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Stellt transporteinstellungen, die Microsoft Outlook verwendet, um die erforderlichen Aufgaben zu ermitteln und die Elemente der Benutzeroberfläche (UI) zu deaktivieren, die das Konto nicht unterstützt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Schnittstelle wird von **IOlkAccountManager::FindAccount** zurückgegeben, bei der Suche nach einem Konto an, die **IOlkAccount** und **IOlkEnum::GetNext** unterstützt, wenn das nächste Konto in ein Enumerator abrufen. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

