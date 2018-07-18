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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 744d9a7588bff89e9d306e516a24da2db3038d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791967"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**Betrifft**: Outlook 
  
Erstellt eine Advise-Empfänger, der eine vorhandene Advise-Empfänger für Threadsicherheit umbrochen wird. 
  
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
  
> [in] Zeiger auf die Advise-Empfänger umgebrochen werden. 
    
 _lppAdviseSink_
  
> [out] Zeiger auf einen Zeiger auf eine neue Advise-Empfänger, der auf das durch den Parameter _LpAdviseSink_ Advise-Empfänger umbrochen wird. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>Bemerkungen

Der Zweck des Wrappers ist dafür sorgen, dass die Benachrichtigung auf dem gleichen Thread aufgerufen wird, die die **HrThisThreadAdviseSink** -Funktion aufgerufen. Diese Funktion wird verwendet, um Benachrichtigung Rückrufe zu schützen, die für einen bestimmten Thread ausgeführt werden muss. 
  
Clientanwendungen sollten **HrThisThreadAdviseSink** verwenden, um einzuschränken, wenn Benachrichtigungen generiert werden, d. h., wenn Anrufe an die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode von der Advise-Empfängerobjekt vom Client in einem vorherigen **Advise übergeben werden **aufrufen. Wenn Benachrichtigungen an willkürlich generiert werden dürfen, möglicherweise eine Benachrichtigung Implementierung ein Clients in Multithread-Vorgang erzwingen, wenn, die nicht geeignet ist. Beispielsweise kann ein Client eine Bibliothek beispielsweise eine der Microsoft Foundation Class Libraries, verwenden, die keine Multithread-Anrufe unterstützt. Benachrichtigung für einen anderen Thread würde solcher Client schwierig zu testen und fehleranfällig, stellen. 
  
 **HrThisThreadAdviseSink** stellt sicher, dass nur diese geeigneten Zeitpunkt **OnNotify** -Aufrufe erfolgen: 
  
- Während der Verarbeitung eines Anrufs an eine beliebige MAPI-Methode. 
    
- Während der Verarbeitung von Windows-Nachrichten. 
    
Wenn **HrThisThreadAdviseSink** implementiert wird, führen dazu, dass alle Anrufe an die neue Advise-Empfänger **OnNotify** -Methode auf einem beliebigen Thread die ursprünglichen Benachrichtigungsmethode für den Thread ausgeführt werden, auf dem **HrThisThreadAdviseSink** aufgerufen wurde. 
  
Weitere Informationen zur Benachrichtigung und advise-Empfänger, finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md) und [Implementieren eines Objekts beraten Auffangen verwenden](implementing-an-advise-sink-object.md). 
  

