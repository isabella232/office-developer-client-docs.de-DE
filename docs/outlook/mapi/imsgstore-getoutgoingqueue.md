---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8ccb732dd587b2e5107290b2db7c48e85d0145d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434151"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf die Tabelle für ausgehende Warteschlangen, eine Tabelle mit Informationen zu allen Nachrichten in der ausgehenden Warteschlange des Nachrichtenspeichers. Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lppTable_
  
> Out Ein Zeiger auf einen Zeiger auf die Tabelle der ausgehenden Warteschlange.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Tabelle für die ausgehende Warteschlange wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore:: GetOutgoingQueue** -Methode bietet dem MAPI-Spooler Zugriff auf die Tabelle, in der die Warteschlange des Nachrichtenspeichers von ausgehenden Nachrichten angezeigt wird. In der Regel werden Nachrichten in der Tabelle für ausgehende Warteschlangen platziert, nachdem die [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode aufgerufen wird. Da sich die Reihenfolge der Übermittlung jedoch auf die Reihenfolge der Vorverarbeitung und Übermittlung an den Transportanbieter auswirkt, werden einige Nachrichten, die zum Senden markiert wurden, möglicherweise nicht sofort in der Tabelle für ausgehende Warteschlangen angezeigt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Eine Liste der Eigenschaften, die in der Tabelle für ausgehende Warteschlangen als Spalten enthalten sein müssen, finden Sie unter [ausgehende Warteschlangentabellen](outgoing-queue-tables.md). 
  
Da der MAPI-Spooler so konzipiert ist, dass er Nachrichten aus einem Nachrichtenspeicher in aufsteigender Reihenfolge der Übermittlungszeit akzeptiert, können die MAPI-Spooler die Tabelle für die ausgehende Warteschlange so sortieren, dass Sie dieser Reihenfolge entspricht, oder Sie als Standardsortierreihenfolge festlegen.
  
Sie müssen Benachrichtigungen für die Warteschlangentabelle für ausgehende Nachrichten unterstützen, um sicherzustellen, dass der MAPI-Spooler benachrichtigt wird, wenn sich die Inhalte der Warteschlange ändern. 
  
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

