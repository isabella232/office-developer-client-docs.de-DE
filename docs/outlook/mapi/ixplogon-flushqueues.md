---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7fde61429307c2adf209b87b325deef69f098c35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584213"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fordert an, dass der Transportanbieter alle ausstehenden eingehenden oder ausgehenden Nachrichten sofort übermittelt.
  
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
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _cbTargetTransport_
  
> [in] Reserviert. NULL muss sein.
    
 _lpTargetTransport_
  
> [in] Reserviert; muss NULL sein.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Leeren der Nachrichtenwarteschlange erfolgt. Die folgenden Flags können festgelegt werden:
    
FLUSH_DOWNLOAD 
  
> Die Warteschlange für eingehende Nachrichten oder Warteschlangen sollte geleert werden.
    
FLUSH_FORCE 
  
> Der Transportanbieter sollte diese Anforderung nach Möglichkeit auch dann verarbeiten, wenn dies zeitaufwändig ist. 
    
FLUSH_NO_UI 
  
> Der Transportanbieter sollte keine Benutzeroberfläche anzeigen.
    
FLUSH_UPLOAD 
  
> Die Warteschlange für ausgehende Nachrichten oder Warteschlangen sollte geleert werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft die **IXPLogon::FlushQueues-Methode** auf, um dem Transportanbieter zu empfehlen, dass der MAPI-Spooler mit der Verarbeitung von Nachrichten beginnen soll. Der Transportanbieter sollte die [IMAPISupport::ModifyStatusRow-Methode aufrufen,](imapisupport-modifystatusrow.md) um ein geeignetes Bit für seinen Status in der **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) -Eigenschaft der Statuszeile festzulegen. Nach dem Aktualisieren der Statuszeile sollte der Transportanbieter S_OK für den **FlushQueues-Aufruf** zurückgeben. Der MAPI-Spooler beginnt dann mit dem Senden von Nachrichten, wobei der Vorgang synchron mit dem MAPI-Spooler ist. 
  
Zur Unterstützung der Implementierung der [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) ruft der MAPI-Spooler **IXPLogon::FlushQueues** für alle Anmeldeobjekte für aktive Transportanbieter auf, die in einer Profilsitzung ausgeführt werden. Wenn die **FlushQueues-Methode** eines Transportanbieters als Ergebnis eines Clientanwendungsaufrufs an **IMAPIStatus::FlushQueues** aufgerufen wird, erfolgt die Nachrichtenverarbeitung asynchron für den Client.
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

