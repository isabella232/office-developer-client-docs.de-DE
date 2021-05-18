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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fb26c7f366ce6a262362001773e825c60d0e4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421970"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fordert an, dass der Transportanbieter sofort alle ausstehenden eingehenden oder ausgehenden Nachrichten zuliefert.
  
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
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _cbTargetTransport_
  
> [in] Reserviert. NULL muss sein.
    
 _lpTargetTransport_
  
> [in] Reserviert; muss NULL sein.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichtenwarteschlange geleert wird. Die folgenden Kennzeichen können festgelegt werden:
    
FLUSH_DOWNLOAD 
  
> Die Eingehende Nachrichtenwarteschlange oder Warteschlangen sollten geleert werden.
    
FLUSH_FORCE 
  
> Der Transportanbieter sollte diese Anforderung nach Möglichkeit verarbeiten, auch wenn dies zeitaufwändig ist. 
    
FLUSH_NO_UI 
  
> Der Transportanbieter sollte keine Benutzeroberfläche anzeigen.
    
FLUSH_UPLOAD 
  
> Die Warteschlange für ausgehende Nachrichten oder Warteschlangen sollte geleert werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft die **IXPLogon::FlushQueues-Methode** auf, um den Transportanbieter zu informieren, dass der MAPI-Spooler mit der Verarbeitung von Nachrichten beginnt. Der Transportanbieter sollte die [IMAPISupport::ModifyStatusRow-Methode](imapisupport-modifystatusrow.md) aufrufen, um ein geeignetes Bit für den Status in der **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))-Eigenschaft der Statuszeile festlegen. Nach dem Aktualisieren der Statuszeile sollte der Transportanbieter S_OK **FlushQueues-Aufruf zurückgeben.** Der MAPI-Spooler beginnt dann mit dem Senden von Nachrichten, und der Vorgang ist synchron mit dem MAPI-Spooler. 
  
Zur Unterstützung der Implementierung der [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) ruft der MAPI-Spooler **IXPLogon::FlushQueues** für alle Anmeldeobjekte für aktive Transportanbieter auf, die in einer Profilsitzung ausgeführt werden. Wenn die **FlushQueues-Methode** eines Transportanbieters als Ergebnis eines Clientanwendungsaufrufs von **IMAPIStatus::FlushQueues** aufgerufen wird, erfolgt die Nachrichtenverarbeitung asynchron für den Client.
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

