---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cdee8a33ad6f9528eed43482aacabf5916b40799
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625511"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet Objekte, die einer MAPI-Anmeldesitzung zugeordnet sind.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Session-Objekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPISession  <br/> |
|Zeigertyp:  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterror](imapisession-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Sitzungsfehler enthält.  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Ermöglicht den Zugriff auf die Nachrichtenspeichertabelle, die Informationen zu allen Nachrichtenspeichern im Sitzungsprofil enthält.  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Öffnet einen Nachrichtenspeicher und gibt einen [IMsgStore-Zeiger](imsgstoreimapiprop.md) für den weiteren Zugriff zurück.  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Öffnet das integrierte MAPI-Adressbuch und gibt einen [IAddrBook-Zeiger](iaddrbookimapiprop.md) für den weiteren Zugriff zurück.  <br/> |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück.  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Bietet Zugriff auf die Statustabelle, eine Tabelle, die Informationen zu allen MAPI-Ressourcen in der Sitzung enthält.  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |Öffnet ein Objekt und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück.  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.  <br/> |
|[Beraten](imapisession-advise.md) <br/> |Registriert sich, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Sitzung auswirken.  <br/> |
|[Unadvise](imapisession-unadvise.md) <br/> |Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **Advise-Methode** eingerichtet wurden.  <br/> |
|**MessageOptions** <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |Veraltet. Gibt die Adresstypen zurück, die von allen Transportanbietern in der Sitzung verarbeitet werden können.  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Gibt den Eintragsbezeichner des Objekts zurück, das die primäre Identität für die Sitzung bereitstellt.  <br/> |
|[Logoff](imapisession-logoff.md) <br/> |Beendet eine MAPI-Sitzung.  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Richtet einen Nachrichtenspeicher als Standardnachrichtenspeicher für die Sitzung ein.  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |Gibt einen [IMsgServiceAdmin-Zeiger](imsgserviceadminiunknown.md) zum Vornehmen von Änderungen an Nachrichtendiensten zurück.  <br/> |
|[Showform](imapisession-showform.md) <br/> |Zeigt ein Formular an.  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |Erstellt ein numerisches Token, das von der **ShowForm-Methode** für den Zugriff auf eine Nachricht verwendet wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

