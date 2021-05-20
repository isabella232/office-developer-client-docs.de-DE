---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428879"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Accesses resources in a message store logon object.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Anmeldeobjekte des Nachrichtenspeichers  <br/> |
|Implementiert von:  <br/> |Anbieter von Nachrichtenspeichern  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMSLogon  <br/> |
|Zeigertyp:  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](imslogon-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum letzten Fehler enthält, der für das Nachrichtenspeicherobjekt aufgetreten ist.  <br/> |
|[Logoff](imslogon-logoff.md) <br/> |Protokolliert einen Nachrichtenspeicheranbieter.  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |Öffnet einen Ordner oder ein Nachrichtenobjekt und gibt einen Zeiger auf das Objekt zurück, um weiteren Zugriff zu ermöglichen.  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.  <br/> |
|[Raten](imslogon-advise.md) <br/> |Registriert ein Objekt bei einem Nachrichtenspeicheranbieter für Benachrichtigungen über Änderungen im Nachrichtenspeicher.  <br/> |
|[Unadvise](imslogon-unadvise.md) <br/> |Entfernt die Registrierung eines Objekts zur Benachrichtigung über Nachrichtenspeicheränderungen, die zuvor mithilfe eines Aufrufs der **IMSLogon::Advise-Methode erstellt** wurden.  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Öffnet ein Statusobjekt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Anmeldeobjekt des Nachrichtenspeichers ist Teil eines geöffneten Nachrichtenspeicheranbieters, den MAPI direkt aufruft. Es besteht eine 1:1-Entsprechung zwischen dem von MAPI aufruften Anmeldeobjekt des Nachrichtenspeichers und dem Nachrichtenspeicherobjekt, das Clientanwendungen aufrufen. Sie können sich die Anmeldung und das Speichern von Objekten als ein Objekt ausbilden, das zwei Schnittstellen verfügbar macht. Die beiden Objekte werden zusammen erstellt und gemeinsam frei.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

