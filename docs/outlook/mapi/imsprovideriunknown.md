---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c5305ddd20b690f5c2e5807fb7ce2410549f7124
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412863"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf einen Nachrichtenspeicheranbieter über ein Objekt des Nachrichtenspeicheranbieters. Dieses Objekt des Nachrichtenspeicheranbieters wird bei der Anbieteranmeldung von der [MSProviderInit-Einstiegspunktfunktion](msproviderinit.md) des Nachrichtenspeicheranbieters zurückgegeben. Das Objekt des Nachrichtenspeicheranbieters wird hauptsächlich von Clientanwendungen und dem MAPI-Spooler zum Öffnen von Nachrichtenspeichern verwendet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Nachrichtenspeicheranbieter-Objekte  <br/> |
|Implementiert von:  <br/> |Anbieter von Nachrichtenspeichern  <br/> |
|Aufgerufen von:  <br/> |MAPI und der MAPI-Spooler  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMSProvider  <br/> |
|Zeigertyp:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Shutdown](imsprovider-shutdown.md) <br/> |Schließt einen Nachrichtenspeicheranbieter in geordneter Weise.  <br/> |
|[Logon](imsprovider-logon.md) <br/> |Protokolliert MAPI an einer Instanz eines Nachrichtenspeicheranbieters.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Protokolliert den MAPI-Spooler bei einem Nachrichtenspeicher.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Vergleicht zwei Nachrichtenspeichereintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Speicherobjekt verweisen.  <br/> |
   
## <a name="remarks"></a>Hinweise

MAPI verwendet ein Nachrichtenspeicheranbieterobjekt pro Sitzung, unabhängig davon, wie viele Nachrichtenspeicher vom Speicheranbieter geöffnet werden. Wenn sich eine zweite MAPI-Sitzung bei geöffneten Speichern anmeldet, ruft MAPI **MSProviderInit** ein zweites Mal auf, um ein neues Objekt des Nachrichtenspeicheranbieters zu erstellen, das für diese Sitzung verwendet werden soll. 
  
Ein Objekt des Nachrichtenspeicheranbieters muss Folgendes enthalten, damit es ordnungsgemäß funktioniert:
  
- Ein  lpMalloc-Speicherzuweisungsroutinenzeiger zur Verwendung durch alle Speicher, die mithilfe dieses Anbieterobjekts geöffnet werden. 
    
- Die _Routinezeiger lpfAllocateBuffer_, _ lpfAllocateMore _, und _lpfFreeBuffer_ zeigen auf die [Speicherzuweisungsfunktionen MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer.](mapifreebuffer.md) 
    
- Eine verknüpfte Liste aller Mit diesem Anbieterobjekt geöffneten und noch nicht geschlossenen Speicher.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

