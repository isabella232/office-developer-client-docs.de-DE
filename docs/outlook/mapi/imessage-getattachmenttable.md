---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6eb28f8e69010b138adbf7ec70daecfba149f8a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592284"
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
  
> [in] Bitmaske von Flags, die sich auf die Erstellung der Tabelle beziehen. Das folgende Kennzeichen kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgenspalten das ANSI-Format.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **getAttachmentTable,** erfolgreich zurückzugeben, möglicherweise bevor die Tabelle für den aufrufenden Client vollständig verfügbar ist. Wenn die Tabelle nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler verursachen. 
    
 _lppTable_
  
> [out] Zeiger auf einen Zeiger auf die Anlagentabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anlagentabelle wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMessage::GetAttachmentTable-Methode** gibt einen Zeiger auf die Anlagentabelle der Nachricht zurück, die Informationen zu allen Anlagen in der Nachricht enthält. Clients können nur über die Anlagentabelle Zugriff auf eine Anlage erhalten. Durch abrufen der Nummer einer Anlage seine **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) -Eigenschaft kann ein Client mehrere der **IMessage-Methoden** verwenden, um mit der Anlage zu arbeiten. 
  
Es gibt eine Zeile für jede Anlage. Eine vollständige Liste der Spalten in einer Anlagentabelle finden Sie unter [Anlagentabellen.](attachment-tables.md)
  
Eine Anlage wird in der Regel erst in der Anlagentabelle angezeigt, wenn sowohl die Anlage als auch die Nachricht mit einem Aufruf von [IMAPIProp::SaveChanges](imapiprop-savechanges.md)gespeichert wurden. Anlagentabellen sind dynamisch. Wenn ein Client eine neue Anlage erstellt, eine vorhandene Anlage löscht oder eine oder mehrere Eigenschaften ändert, nachdem die **SaveChanges-Aufrufe** für die Anlage in der Nachricht vorgenommen wurden, wird die Anlagentabelle aktualisiert, um die neuen Informationen widerzuspiegeln. 
  
Einige Anlagentabellen unterstützen eine Vielzahl von Einschränkungen. andere nicht. Die Unterstützung von Einschränkungen hängt von der Implementierung des Nachrichtenspeicheranbieters ab. 
  
Beim anfänglichen Öffnen werden Anlagentabellen nicht unbedingt in einer bestimmten Reihenfolge sortiert. 
  
Das Festlegen des MAPI_UNICODE Flags im  _ulFlags-Parameter_ wirkt sich auf die folgenden Aufrufe der Anlagentabelle aus: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) zum Abrufen des Spaltensatzes. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen von Zeilen. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) zum Abrufen der Sortierreihenfolge. 
    
Das Festlegen des Unicode-Flags fordert an, dass die Informationen für alle von diesen Aufrufen zurückgegebenen Zeichenfolgenspalten im Unicode-Format vorliegen. Da jedoch nicht alle Nachrichtenspeicheranbieter Unicode unterstützen, ist das Festlegen dieses Flags nur eine Anforderung.
  
## <a name="see-also"></a>Siehe auch



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

