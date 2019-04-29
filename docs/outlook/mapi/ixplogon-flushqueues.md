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
  
Fordert, dass der Transportanbieter alle ausstehenden eingehenden oder ausgehenden Nachrichten sofort bereitstellt.
  
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
  
> in Ein Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster.
    
 _cbTargetTransport_
  
> [in] Reserviert. NULL muss sein.
    
 _lpTargetTransport_
  
> in Reserviert muss NULL sein.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie die Nachrichten Warteschlangen Spülung durchgeführt wird. Die folgenden Flags können festgelegt werden:
    
FLUSH_DOWNLOAD 
  
> Die Warteschlange für eingehende Nachrichten oder Warteschlangen sollte geleert werden.
    
FLUSH_FORCE 
  
> Der Transportanbieter sollte diese Anforderung, wenn möglich, verarbeiten, auch wenn dies zeitaufwändig ist. 
    
FLUSH_NO_UI 
  
> Der Transportanbieter sollte keine Benutzeroberfläche anzeigen.
    
FLUSH_UPLOAD 
  
> Die Warteschlange für ausgehende Nachrichten oder Warteschlangen sollte geleert werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Der MAPI-Spooler Ruft die **IXPLogon:: FlushQueues** -Methode auf, um dem Transportanbieter zu raten, dass der MAPI-Spooler mit der Verarbeitung von Nachrichten beginnen soll. Der Transportanbieter sollte die [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode aufrufen, um ein entsprechendes Bit für seinen Status in der **PR_STATUS_CODE** ([pidtagstatuscode (](pidtagstatuscode-canonical-property.md))-Eigenschaft der Status Zeile festzulegen. Nach dem Aktualisieren der Statuszeile sollte der Transportanbieter S_OK für den **FlushQueues** -Aufruf zurückgeben. Der MAPI-Spooler startet dann das Senden von Nachrichten, wobei der Vorgang synchron mit dem MAPI-Spooler ausgeführt wird. 
  
Zur Unterstützung der Implementierung der [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) -Methode ruft der MAPI-Spooler **IXPLogon:: FlushQueues** für alle Anmeldeobjekte für aktive Transportanbieter auf, die in einer Profil Sitzung laufen. Wenn die **FlushQueues** -Methode eines Transportanbieters als Ergebnis eines Client Anwendungsaufrufs an **IMAPIStatus:: FlushQueues**aufgerufen wird, wird die Nachrichtenverarbeitung asynchron für den Client ausgeführt.
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

