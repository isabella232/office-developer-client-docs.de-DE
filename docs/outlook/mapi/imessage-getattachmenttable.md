---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9a77d335f3c8980de29dab6e14079c83bd711b43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421172"
---
# <a name="imessagegetattachmenttable"></a>IMessage::GetAttachmentTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Anlagentabelle der Nachricht zurück.
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Bitmaske von Flags, die sich auf die Erstellung der Tabelle beziehen. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgenspalten im ANSI-Format.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **getAttachmentTable,** erfolgreich zurückzukehren, möglicherweise bevor die Tabelle vollständig für den aufrufenden Client verfügbar ist. Wenn die Tabelle nicht verfügbar ist, kann ein nachfolgender Aufruf der Tabelle zu einem Fehler führen. 
    
 _lppTable_
  
> [out] Zeiger auf einen Zeiger auf die Anlagentabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anlagentabelle wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Hinweise

Die **IMessage::GetAttachmentTable-Methode** gibt einen Zeiger auf die Anlagentabelle der Nachricht zurück, die Informationen zu allen Anlagen in der Nachricht enthält. Clients können nur über die Anlagentabelle zugriff auf eine Anlage erhalten. Durch Abrufen der Nummer einer Anlage PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) -Eigenschaft kann ein Client mehrere der **IMessage-Methoden** verwenden, um mit der Anlage zu arbeiten. 
  
Es gibt eine Zeile für jede Anlage. Eine vollständige Liste der Spalten in einer Anlagentabelle finden Sie unter [Attachment Tables](attachment-tables.md).
  
Eine Anlage wird in der Regel erst in der Anlagentabelle angezeigt, wenn sowohl die Anlage als auch die Nachricht mit einem Aufruf von [IMAPIProp::SaveChanges gespeichert wurden.](imapiprop-savechanges.md) Anlagentabellen sind dynamisch. Wenn ein Client eine neue Anlage erstellt, eine vorhandene Anlage löscht oder eine oder mehrere Eigenschaften ändert, nachdem die **SaveChanges-Aufrufe** für die Anlage in der Nachricht ausgeführt wurden, wird die Anlagentabelle entsprechend den neuen Informationen aktualisiert. 
  
Einige Anlagentabellen unterstützen eine Vielzahl von Einschränkungen. Andere tun dies nicht. Die Unterstützung für Einschränkungen hängt von der Implementierung des Nachrichtenspeicheranbieters ab. 
  
Beim ersten Öffnen werden Anlagentabellen nicht unbedingt in einer bestimmten Reihenfolge sortiert. 
  
Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ wirkt sich auf die folgenden Aufrufe der Anlagentabelle aus: 
  
- [IMAPITable::QueryColumns,](imapitable-querycolumns.md) um den Spaltensatz abzurufen. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen von Zeilen. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) zum Abrufen der Sortierreihenfolge. 
    
Das Festlegen des Unicode-Kennzeichens fordert, dass die Informationen für alle von diesen Aufrufen zurückgegebenen Zeichenfolgenspalten im Unicode-Format vorliegen. Da jedoch nicht alle Nachrichtenspeicheranbieter Unicode unterstützen, ist das Festlegen dieses Kennzeichens nur eine Anforderung.
  
## <a name="see-also"></a>Siehe auch



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

