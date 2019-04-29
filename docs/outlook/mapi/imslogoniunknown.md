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
  
Greift auf Ressourcen in einem Nachrichtenspeicher-Anmeldeobjekt zu.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Nachrichtenspeicher-Anmeldeobjekte  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicher Anbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMSLogon  <br/> |
|Zeigertyp:  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterroraufzurufen](imslogon-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum letzten Fehler enthält, der für das Nachrichtenspeicherobjekt aufgetreten ist.  <br/> |
|[Logoff](imslogon-logoff.md) <br/> |Meldet einen Nachrichtenspeicher Anbieter ab.  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |Öffnet ein Folder-oder Message-Objekt und gibt einen Zeiger auf das Objekt zurück, um weiteren Zugriff zu ermöglichen.  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.  <br/> |
|[Beraten](imslogon-advise.md) <br/> |Registriert ein Objekt bei einem Nachrichtenspeicher Anbieter für Benachrichtigungen zu Änderungen im Nachrichtenspeicher.  <br/> |
|[Unadvise](imslogon-unadvise.md) <br/> |Entfernt die Registrierung eines Objekts für die Benachrichtigung über Änderungen am Nachrichtenspeicher, die zuvor mithilfe eines Aufrufs der **IMSLogon:: Advise** -Methode festgelegt wurden.  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Öffnet ein Status-Objekt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Nachrichtenspeicher-Anmeldeobjekt ist der Teil eines geöffneten Nachrichtenspeicher Anbieters, der von MAPI direkt aufgerufen wird. Es gibt eine 1:1-Entsprechung zwischen dem Nachrichtenspeicher-Anmeldeobjekt, das von MAPI aufgerufen wird, und dem Nachrichtenspeicherobjekt, das von Clientanwendungen aufgerufen wird; Sie können sich die Anmelde-und Speicherobjekte als ein Objekt vorstellen, das zwei Schnittstellen verfügbar macht. Die beiden Objekte werden zusammen erstellt und gemeinsam freigegeben.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

