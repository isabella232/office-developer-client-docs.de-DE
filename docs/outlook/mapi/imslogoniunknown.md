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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 42e2633ac6d534be2c75c47b24c1da5ed9771e18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792679"
---
# <a name="imslogon--iunknown"></a>IMSLogon: IUnknown

  
  
**Betrifft**: Outlook 
  
Greift auf Ressourcen in einer Nachricht speichern Anmeldeobjekt.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Nachricht Store Logon-Objekten  <br/> |
|Implementiert von:  <br/> |Nachricht-Anbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMSLogon  <br/> |
|Zeigertyp:  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](imslogon-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den letzten Fehler enthält, die für das Store-Nachrichtenspeicherobjekt aufgetreten sind.  <br/> |
|[Logoff](imslogon-logoff.md) <br/> |Eine Nachricht Abmeldung Speicheranbieter.  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |Öffnet einen Ordner oder Message-Objekt und gibt einen Zeiger auf das Objekt, das Zugriff zu ermöglichen.  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.  <br/> |
|[Beraten](imslogon-advise.md) <br/> |Registriert ein Objekt mit einem Anbieter für Benachrichtigungen zu Änderungen im Nachrichtenspeicher Nachricht.  <br/> |
|[Heben Sie diesen Vorgang](imslogon-unadvise.md) <br/> |Entfernt ein Objekt Anmeldungsseite für Benachrichtigung über Message Store Änderungen, die zuvor durch einen Aufruf an die **IMSLogon::Advise** -Methode festgelegt.  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Öffnet ein Statusobjekt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Message Store Anmeldung-Objekts ist der Teil einer geöffneten Nachricht Speicheranbieter, die MAPI direkt aufruft. Es gibt eine 1: 1-Beziehung zwischen Message Store Anmeldung-Objekts, die MAPI-Aufrufe und die Nachricht Objekt speichern, die Clientanwendungen aufrufen. Sie können vorstellen der Anmeldung und Speichern von Objekten als ein Objekt, das zwei Schnittstellen verfügbar macht. Die zwei Objekte werden zusammen und freigegebenen zusammen erstellt.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

