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
  
Ermöglicht den Zugriff auf einen Nachrichtenspeicher Anbieter über ein Objekt des Nachrichtenspeicher Anbieters. Dieses Objekt des Nachrichtenspeicher Anbieters wird bei der Anbieter Anmeldung von der [MSProviderInit](msproviderinit.md) -Einstiegspunktfunktion des Nachrichtenspeicher Anbieters zurückgegeben. Das Nachrichtenspeicher-Anbieterobjekt wird hauptsächlich von Clientanwendungen und dem MAPI-Spooler zum Öffnen von Nachrichten speichern verwendet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Nachrichtenspeicheranbieter-Objekte  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicher Anbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI und der MAPI-Spooler  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMSProvider  <br/> |
|Zeigertyp:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Herunterfahren](imsprovider-shutdown.md) <br/> |Schließt einen Nachrichtenspeicher Anbieter ordnungsgemäß.  <br/> |
|[Logon](imsprovider-logon.md) <br/> |Protokolliert MAPI für eine Instanz eines Nachrichtenspeicher Anbieters.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Protokolliert den MAPI-Spooler in einem Nachrichtenspeicher.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Vergleicht zwei Nachrichtenspeicher Eintrags-IDs, um zu bestimmen, ob Sie auf dasselbe Store-Objekt verweisen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

MAPI verwendet ein Nachrichtenspeicher-Anbieterobjekt pro Sitzung, unabhängig davon, wie viele Nachrichtenspeicher vom Informationsspeicher Anbieter geöffnet werden. Wenn sich eine zweite MAPI-Sitzung bei einem geöffneten Speicher anmeldet, ruft MAPI **MSProviderInit** ein zweites Mal auf, um ein neues Nachrichtenspeicher-Anbieterobjekt für die zu verwendende Sitzung zu erstellen. 
  
Ein Nachrichtenspeicher-Anbieterobjekt muss Folgendes enthalten, damit es ordnungsgemäß funktioniert:
  
- Ein _lpMalloc_ -Routine Zeiger zur Speicherzuweisung für die Verwendung durch alle Speicher, die mithilfe dieses Anbieterobjekts geöffnet werden. 
    
- Die _lpfAllocateBuffer_-, _ lpfAllocateMore _-und _lpfFreeBuffer_ -Routine Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md)-, [MAPIAllocateMore](mapiallocatemore.md)-und [mapifreebufferfreigegeben](mapifreebuffer.md) -Speicher Zuordnungsfunktionen. 
    
- Eine verknüpfte Liste aller Speicher, die mithilfe dieses Anbieterobjekts geöffnet und noch nicht geschlossen wurden.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

