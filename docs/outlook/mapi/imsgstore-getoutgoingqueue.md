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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1b59071758aad9c71939eb9efc029005806b2a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792632"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**Betrifft**: Outlook 
  
Bietet Zugriff auf ausgehende Warteschlangentabelle eine Tabelle mit Informationen über alle Nachrichten in der Nachrichtenspeicher ausgehenden Warteschlange. Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.
  
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
  
> [out] Ein Zeiger auf einen Zeiger auf die ausgehende Warteschlangentabelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die ausgehende Warteschlangentabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::GetOutgoingQueue** -Methode enthält die MAPI-Warteschlange mit Zugriff auf die Tabelle, die die Nachrichtenspeicher-Warteschlange von ausgehenden Nachrichten anzeigt. Nachrichten werden in der Regel in der ausgehenden Warteschlangentabelle platziert, nach deren [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode aufgerufen wird. Allerdings, da die Reihenfolge der Übermittlung die Reihenfolge der vorverarbeitung und Übermittlung an der Adressbuchhierarchie betroffen sind, möglicherweise einige Nachrichten, die für das Senden von gekennzeichnet wurden nicht in der ausgehenden Warteschlangentabelle sofort angezeigt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Eine Liste der Eigenschaften, die als Spalten in der ausgehenden Warteschlangentabelle enthalten sein müssen, finden Sie unter [Ausgehende Warteschlange Tabellen](outgoing-queue-tables.md). 
  
Da die MAPI-Warteschlange zum Akzeptieren von Nachrichten von einem Nachrichtenspeicher in aufsteigender Reihenfolge der Zeitpunkt der Übermittlung ausgelegt ist, entweder zulassen Sie die MAPI-Warteschlange zum Sortieren der ausgehenden Warteschlangentabelle, um diesen Auftrag übereinstimmen oder diese als die standardmäßige Sortierreihenfolge einzurichten.
  
Sie müssen Unterstützung Benachrichtigungen für ausgehende Nachrichten Warteschlange-Tabelle, um sicherzustellen, dass die MAPI-Warteschlange benachrichtigt wird, wenn der Inhalt der Warteschlange ändern. 
  
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

