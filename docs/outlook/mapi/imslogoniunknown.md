---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 732832ffba273f174cb107d8b749d7f5c3eb8187
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579789"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Greift auf Ressourcen in einem Anmeldeobjekt für den Nachrichtenspeicher zu.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Anmeldeobjekte des Nachrichtenspeichers  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicheranbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMSLogon  <br/> |
|Zeigertyp:  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterror](imslogon-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum letzten Fehler enthält, der für das Nachrichtenspeicherobjekt aufgetreten ist.  <br/> |
|[Logoff](imslogon-logoff.md) <br/> |Meldet sich von einem Nachrichtenspeicheranbieter ab.  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |Öffnet einen Ordner oder ein Nachrichtenobjekt und gibt einen Zeiger auf das Objekt zurück, um weiteren Zugriff zu ermöglichen.  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.  <br/> |
|[Beraten](imslogon-advise.md) <br/> |Registriert ein Objekt bei einem Nachrichtenspeicheranbieter für Benachrichtigungen zu Änderungen im Nachrichtenspeicher.  <br/> |
|[Unadvise](imslogon-unadvise.md) <br/> |Entfernt die Registrierung eines Objekts für die Benachrichtigung über Änderungen am Nachrichtenspeicher, die zuvor mithilfe eines Aufrufs der **IMSLogon::Advise-Methode** eingerichtet wurden.  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Öffnet ein Statusobjekt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Anmeldeobjekt des Nachrichtenspeichers ist Teil eines geöffneten Nachrichtenspeicheranbieters, den MAPI direkt aufruft. Es besteht eine 1:1-Entsprechung zwischen dem Anmeldeobjekt für den Nachrichtenspeicher, das mapi aufruft, und dem Nachrichtenspeicherobjekt, das von Clientanwendungen aufgerufen wird. Sie können sich die Anmelde- und Speicherobjekte als ein Objekt vorstellen, das zwei Schnittstellen verfügbar macht. Die beiden Objekte werden zusammen erstellt und freigegeben.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

