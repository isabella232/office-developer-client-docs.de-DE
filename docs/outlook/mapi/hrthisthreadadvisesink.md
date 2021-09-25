---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f9375bea70521ead0659f51413301be170559ac5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616957"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Empfehlungssenke, die eine vorhandene Empfehlungssenke zur Threadsicherheit umschließt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parameter

 _lpAdviseSink_
  
> [in] Zeiger auf die Empfehlungssenke, die umbrochen werden soll. 
    
 _lppAdviseSink_
  
> [out] Zeiger auf einen Zeiger auf eine neue Empfehlungssenke, die die Rate-Senken umschließt, auf die der  _lpAdviseSink-Parameter_ verweist. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Der Zweck des Wrappers besteht darin, sicherzustellen, dass die Benachrichtigung für denselben Thread aufgerufen wird, der die **HrThisThreadAdviseSink-Funktion** aufgerufen hat. Diese Funktion wird verwendet, um Benachrichtigungsrückrufe zu schützen, die in einem bestimmten Thread ausgeführt werden müssen. 
  
Clientanwendungen sollten **HrThisThreadAdviseSink** verwenden, um einzuschränken, wann Benachrichtigungen generiert werden, d. h., wenn Aufrufe an die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) des Advise-Senkenobjekts erfolgen, das vom Client in einem vorherigen **Advise-Aufruf** übergeben wurde. Wenn Benachrichtigungen willkürlich generiert werden dürfen, kann eine Benachrichtigungsimplementierungen einen Client in einen Multithread-Vorgang erzwingen, wenn dies nicht geeignet wäre. Beispielsweise kann ein Client eine Bibliothek verwenden, z. B. eine der Microsoft Foundation-Klassenbibliotheken, die keine Multithread-Aufrufe unterstützt. Benachrichtigungen in einem anderen Thread würden einen solchen Client schwierig zu testen und fehleranfällig machen. 
  
 **HrThisThreadAdviseSink** stellt sicher, dass **OnNotify-Aufrufe** nur zu den folgenden zeitpunkten erfolgen: 
  
- Während der Verarbeitung eines Aufrufs einer mapi-Methode. 
    
- Während der Verarbeitung von Windows Nachrichten. 
    
Wenn **HrThisThreadAdviseSink** implementiert wird, wird die ursprüngliche Benachrichtigungsmethode bei Aufrufen der **OnNotify-Methode** der neuen Empfehlungssenke in einem Thread in dem Thread ausgeführt, für den **HrThisThreadAdviseSink** aufgerufen wurde. 
  
Weitere Informationen zu Benachrichtigungs- und Empfehlungssenken finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) und [Implementieren eines Advise Sink-Objekts.](implementing-an-advise-sink-object.md) 
  

