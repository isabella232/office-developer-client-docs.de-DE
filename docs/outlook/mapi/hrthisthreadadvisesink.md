---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427728"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Ratensenke, die eine vorhandene Ratensenke zur Threadsicherheit umschließt. 
  
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
  
> [in] Zeiger auf die umbrochene Ratensenke. 
    
 _lppAdviseSink_
  
> [out] Zeiger auf einen Zeiger auf eine neue Hinweissenke, die die durch den  _lpAdviseSink-Parameter angezeigte_ Ratensenke umschließt. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Der Zweck des Wrappers besteht im Sicherstellen, dass die Benachrichtigung für denselben Thread aufgerufen wird, der die **HrThisThreadAdviseSink-Funktion** aufgerufen hat. Diese Funktion wird verwendet, um Benachrichtigungsrückrufe zu schützen, die in einem bestimmten Thread ausgeführt werden müssen. 
  
Clientanwendungen sollten **HrThisThreadAdviseSink** verwenden, um einzuschränken, wann Benachrichtigungen generiert werden, d. h. wenn Aufrufe an die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) des vom Client in einem vorherigen Advise-Aufruf übergebenen **Advise-Objekts** ausgeführt werden. Wenn Benachrichtigungen willkürlich generiert werden dürfen, kann eine Benachrichtigungsimplementierung einen Client zu einem Multithreadvorgang zwingen, wenn dies nicht angemessen wäre. Ein Client kann z. B. eine Bibliothek verwenden, z. B. eine der Microsoft Foundation-Klassenbibliotheken, die keine Multithreadaufrufe unterstützt. Eine Benachrichtigung in einem anderen Thread würde einen solchen Client schwer testen und fehleranfällig machen. 
  
 **HrThisThreadAdviseSink** stellt sicher, dass **OnNotify-Aufrufe** nur zu den folgenden geeigneten Zeiten auftreten: 
  
- Während der Verarbeitung eines Aufrufs einer beliebigen MAPI-Methode. 
    
- Während der Verarbeitung Windows Nachrichten. 
    
Wenn **HrThisThreadAdviseSink** implementiert ist, werden alle Aufrufe der **OnNotify-Methode** der neuen Ratensenke für jeden Thread dazu führen, dass die ursprüngliche Benachrichtigungsmethode für den Thread ausgeführt wird, in dem **HrThisThreadAdviseSink** aufgerufen wurde. 
  
Weitere Informationen zu Benachrichtigungs- und Hinweissenken finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) und [Implementieren eines Advise Sink-Objekts](implementing-an-advise-sink-object.md). 
  

