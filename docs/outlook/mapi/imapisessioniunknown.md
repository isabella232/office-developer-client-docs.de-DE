---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 163bce38d665a8566fd703420ff1f7b2f44f7c63
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571808"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Verwaltet von Objekten einer MAPI-Sitzung zugeordnet.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Verfügbar gemacht von:  <br/> |Session-Objekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPISession  <br/> |
|Zeigertyp:  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Sitzungsfehler enthält.  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Bietet Zugriff auf die Nachricht Store Tabelle mit Informationen zu allen Nachrichtenspeichern im Profil der Sitzung.  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Öffnet einen Nachrichtenspeicher und gibt einen Zeiger [IMsgStore](imsgstoreimapiprop.md) für den weiteren Zugriff.  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Öffnet das MAPI-integrierte Adressbuch, einen [IAddrBook](iaddrbookimapiprop.md) Zeiger für den weiteren Zugriff zurückgibt.  <br/> |
|["OpenProfileSection"](imapisession-openprofilesection.md) <br/> |Öffnet einen Abschnitt des aktuellen Profils und gibt einen Zeiger [IProfSect](iprofsectimapiprop.md) für den weiteren Zugriff.  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Bietet Zugriff auf die Statustabelle, einer Tabelle, Informationen zu allen MAPI-Ressourcen in der Sitzung enthält.  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |Öffnet ein Objekt und gibt einen Schnittstellenzeiger für den weiteren Zugriff.  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.  <br/> |
|[Beraten](imapisession-advise.md) <br/> |Um die Benachrichtigung der angegebenen Ereignisse, die Einfluss auf die Sitzung registriert.  <br/> |
|[Heben Sie diesen Vorgang](imapisession-unadvise.md) <br/> |Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der **Advise** -Methode eingerichtet.  <br/> |
|**MessageOptions** <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |Veraltet. Gibt die behandelt werden können Adresstypen aller Anbieter für den Transport in der Sitzung zurück.  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Gibt die Eintrags-ID des Objekts, das die primäre Identität für die Sitzung bereitstellt.  <br/> |
|[Logoff](imapisession-logoff.md) <br/> |MAPI-Sitzung beendet.  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Stellt einen Nachrichtenspeicher als Standard-Informationsspeicher für die Sitzung her.  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |Gibt einen Zeiger [IMsgServiceAdmin](imsgserviceadminiunknown.md) für die Änderung Message-Dienste.  <br/> |
|[ShowForm aus](imapisession-showform.md) <br/> |Zeigt ein Formular an.  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |Erstellt eine numerische Token, das die **ShowForm aus** -Methode verwendet, um auf eine Nachricht zuzugreifen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

