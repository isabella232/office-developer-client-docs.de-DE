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
  
Erstellt eine Advise-Senke, die eine vorhandene Advise-Senke für die Threadsicherheit umschließt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parameter

 _lpAdviseSink_
  
> in Zeiger auf die zu umhüllende Advise-Senke. 
    
 _lppAdviseSink_
  
> Out Zeiger auf einen Zeiger auf eine neue Advise-Senke, die die Advise-Senke umschließt, auf die durch den _lpAdviseSink_ -Parameter verwiesen wird. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Der Zweck des Wrappers besteht darin, sicherzustellen, dass die Benachrichtigung für den gleichen Thread aufgerufen wird, der die **HrThisThreadAdviseSink** -Funktion aufgerufen hat. Diese Funktion wird verwendet, um Benachrichtigungsrückrufe zu schützen, die für einen bestimmten Thread ausgeführt werden müssen. 
  
Client Anwendungen sollten **HrThisThreadAdviseSink** verwenden, um zu beschränken, wenn Benachrichtigungen generiert werden, das heißt, wenn Aufrufe an die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode des Advise-Senke-Objekts durchgeführt werden, das vom Client in einer vorherigen Advise übergeben wurde. ** **Anruf. Wenn Benachrichtigungen zulässig sind, willkürlich zu generieren, kann eine Benachrichtigungs Implementierung einen Client in Multithread-Betrieb zwingen, wenn dies nicht angemessen wäre. Beispielsweise kann ein Client eine Bibliothek verwenden, wie etwa eine der Microsoft Foundation Class-Bibliotheken, die Multithread-Aufrufe nicht unterstützt. Die Benachrichtigung in einem anderen Thread würde einen solchen Client schwer testen und fehleranfällig machen. 
  
 **HrThisThreadAdviseSink** stellt sicher, **** dass OnNotify-Aufrufe nur zu diesen geeigneten Zeiten stattfinden: 
  
- Während der Verarbeitung eines Aufrufs an eine beliebige MAPI-Methode. 
    
- Während der Verarbeitung von Windows-Nachrichten. 
    
Wenn **HrThisThreadAdviseSink** implementiert wird, führen Aufrufe der OnNotify-Methode der **** neuen Advise-Senke in einem Thread dazu, dass die ursprüngliche Benachrichtigungsmethode für den Thread ausgeführt wird, in dem **HrThisThreadAdviseSink** aufgerufen wurde. 
  
Weitere Informationen zu Benachrichtigungs-und Advise-Senken finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) und [Implementieren eines Advise](implementing-an-advise-sink-object.md)-Senke-Objekts. 
  

