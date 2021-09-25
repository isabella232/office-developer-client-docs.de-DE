---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 91cd01e3160ac0f02cf17248c25290480b3e9107
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556406"
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
  
> [out] Ein Zeiger auf einen Zeiger auf die Tabelle der ausgehenden Warteschlange.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Tabelle der ausgehenden Warteschlange wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgStore::GetOutgoingQueue-Methode** bietet dem MAPI-Spooler Zugriff auf die Tabelle, die die Warteschlange des Nachrichtenspeichers für ausgehende Nachrichten anzeigt. In der Regel werden Nachrichten in der Tabelle der ausgehenden Warteschlange platziert, nachdem ihre [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufgerufen wurde. Da sich die Reihenfolge der Übermittlung jedoch auf die Reihenfolge der Vorverarbeitung und Übermittlung an den Transportanbieter auswirkt, werden einige Nachrichten, die für das Senden markiert wurden, möglicherweise nicht sofort in der Tabelle der ausgehenden Warteschlange angezeigt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Eine Liste der Eigenschaften, die als Spalten in die Tabelle der ausgehenden Warteschlange eingeschlossen werden müssen, finden Sie unter ["Outgoing Queue Tables".](outgoing-queue-tables.md) 
  
Da der MAPI-Spooler darauf ausgelegt ist, Nachrichten aus einem Nachrichtenspeicher in aufsteigender Reihenfolge der Übermittlungszeit zu akzeptieren, können Sie entweder zulassen, dass der MAPI-Spooler die Tabelle der ausgehenden Warteschlange so sortiert, dass sie dieser Reihenfolge entspricht, oder sie als Standardsortierreihenfolge einrichten.
  
Sie müssen Benachrichtigungen für die Tabelle der Warteschlange für ausgehende Nachrichten unterstützen, um sicherzustellen, dass der MAPI-Spooler benachrichtigt wird, wenn sich der Inhalt der Warteschlange ändert. 
  
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

