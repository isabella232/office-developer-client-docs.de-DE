---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 116e3cfaace9c0965001021575b76ec371667877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792877"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**Betrifft**: Outlook 
  
Fordert, dass der Adressbuchhierarchie sofort alle ausstehende eingehende oder ausgehende Nachrichten übermitteln.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.
    
 _cbTargetTransport_
  
> [in] Reserviert. NULL muss sein.
    
 _lpTargetTransport_
  
> [in] Reserviert. NULL muss sein.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie Nachrichten die Warteschlange das leeren erfolgt. Die folgenden Kennzeichen können festgelegt werden:
    
FLUSH_DOWNLOAD 
  
> Die Warteschlange für eingehende Nachrichten oder Warteschlangen geleert werden sollte.
    
FLUSH_FORCE 
  
> Der Adressbuchhierarchie sollte Verarbeiten dieser Anforderung, wenn möglich, auch wenn dies also Zeit in Anspruch nehmen ist. 
    
FLUSH_NO_UI 
  
> Der Transportdienst keine Benutzeroberfläche angezeigt werden sollen.
    
FLUSH_UPLOAD 
  
> Die Warteschlange für ausgehende Nachrichten oder Warteschlangen geleert werden sollte.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die MAPI-Warteschlange Ruft die **IXPLogon::FlushQueues** -Methode, um der Adressbuchhierarchie darauf hinzuweisen, dass die MAPI-Warteschlange ist dabei, die Verarbeitung von Nachrichten zu beginnen. Der Transportdienst sollte die [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode zum Festlegen einer entsprechenden Bit für den Zustand in die **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))-Eigenschaft des seine Statuszeile aufrufen. Nach dem Aktualisieren der Statuszeile, sollte der Adressbuchhierarchie für den Anruf **FlushQueues** S_OK zurückgegeben. Die MAPI-Warteschlange startet das Senden von Nachrichten, mit dem Vorgang synchron an die Warteschlange MAPI. 
  
Unterstützung der Implementierung der [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) -Methode ruft die MAPI-Warteschlange **IXPLogon::FlushQueues** für alle Objekte, Anmeldung für aktiven Transport-Anbieter, die in einer Sitzung Profil ausgeführt werden. Wenn als Ergebnis einer Client-Anwendung **IMAPIStatus::FlushQueues**Aufruf eines Transportdienstes **FlushQueues** -Methode aufgerufen wird, tritt die Verarbeitung von Nachrichten asynchron an den Client.
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon: IUnknown](ixplogoniunknown.md)

