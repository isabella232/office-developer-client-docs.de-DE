---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d24f2c0697a3aad951625837fa3e56cf6fb9ccd3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575658"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf einen Nachrichtenspeicheranbieter über ein Nachrichtenspeicheranbieterobjekt. Dieses Nachrichtenspeicheranbieterobjekt wird bei der Anbieteranmeldung von der [MSProviderInit-Einstiegspunktfunktion](msproviderinit.md) des Nachrichtenspeicheranbieters zurückgegeben. Das Nachrichtenspeicheranbieterobjekt wird in erster Linie von Clientanwendungen und dem MAPI-Spooler zum Öffnen von Nachrichtenspeichern verwendet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Nachrichtenspeicheranbieter-Objekte  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicheranbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI und der MAPI-Spooler  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMSProvider  <br/> |
|Zeigertyp:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Shutdown](imsprovider-shutdown.md) <br/> |Schließt einen Nachrichtenspeicheranbieter in geordneter Reihenfolge.  <br/> |
|[Logon](imsprovider-logon.md) <br/> |Protokolliert die MAPI bei einer Instanz eines Nachrichtenspeicheranbieters.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Protokolliert den MAPI-Spooler in einem Nachrichtenspeicher.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Vergleicht zwei Eintragsbezeichner für den Nachrichtenspeicher, um zu bestimmen, ob sie auf dasselbe Speicherobjekt verweisen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die MAPI verwendet ein Nachrichtenspeicheranbieterobjekt pro Sitzung, unabhängig davon, wie viele Nachrichtenspeicher vom Store-Anbieter geöffnet werden. Wenn sich eine zweite MAPI-Sitzung bei geöffneten Speichern anmeldet, ruft MAPI **MSProviderInit** ein zweites Mal auf, um ein neues Nachrichtenspeicheranbieterobjekt für diese Sitzung zu erstellen. 
  
Ein Nachrichtenspeicheranbieterobjekt muss Folgendes enthalten, damit es ordnungsgemäß funktioniert:
  
- Ein  lpMalloc-Speicherzuweisungsroutinezeiger zur Verwendung durch alle Speicher, die mithilfe dieses Anbieterobjekts geöffnet wurden. 
    
- Die _Routinezeiger "lpfAllocateBuffer",_"_ lpfAllocateMore_" und _"lpfFreeBuffer"_ auf die Arbeitsspeicherzuweisungsfunktionen [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer.](mapifreebuffer.md) 
    
- Eine verknüpfte Liste aller Speicher, die mit diesem Anbieterobjekt geöffnet und noch nicht geschlossen wurden.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

