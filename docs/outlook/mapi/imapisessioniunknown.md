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
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413381"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet Objekte, die einer MAPI-Anmeldesitzung zugeordnet sind.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Sitzungsobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPISession  <br/> |
|Zeigertyp:  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Sitzungsfehler enthält.  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Bietet Zugriff auf die Nachrichtenspeichertabelle, die Informationen zu allen Nachrichtenspeichern im Sitzungsprofil enthält.  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Öffnet einen Nachrichtenspeicher und gibt einen [IMsgStore-Zeiger](imsgstoreimapiprop.md) für weiteren Zugriff zurück.  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Öffnet das integrierte MAPI-Adressbuch und gibt einen [IAddrBook-Zeiger für](iaddrbookimapiprop.md) weiteren Zugriff zurück.  <br/> |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück.  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Bietet Zugriff auf die Statustabelle, eine Tabelle, die Informationen zu allen MAPI-Ressourcen in der Sitzung enthält.  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |Öffnet ein Objekt und gibt einen Schnittstellenzeiger für weiteren Zugriff zurück.  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.  <br/> |
|[Raten](imapisession-advise.md) <br/> |Registriert, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Sitzung auswirken.  <br/> |
|[Unadvise](imapisession-unadvise.md) <br/> |Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **Advise-Methode eingerichtet** wurden.  <br/> |
|**MessageOptions** <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |Veraltet. Gibt die Adresstypen zurück, die von allen Transportanbietern in der Sitzung verarbeitet werden können.  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Gibt den Eintragsbezeichner des Objekts zurück, das die primäre Identität für die Sitzung enthält.  <br/> |
|[Logoff](imapisession-logoff.md) <br/> |Beendet eine MAPI-Sitzung.  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Richtet einen Nachrichtenspeicher als Standardnachrichtenspeicher für die Sitzung ein.  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |Gibt einen [IMsgServiceAdmin-Zeiger zum](imsgserviceadminiunknown.md) Vornehmen von Änderungen an Nachrichtendiensten zurück.  <br/> |
|[ShowForm](imapisession-showform.md) <br/> |Zeigt ein Formular an.  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |Erstellt ein numerisches Token, das von der **ShowForm-Methode** für den Zugriff auf eine Nachricht verwendet wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

