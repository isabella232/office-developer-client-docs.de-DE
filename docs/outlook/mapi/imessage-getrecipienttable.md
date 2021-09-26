---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 466e0e8d5adee88b8e6a7d1b70c79bf075310cb0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610510"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Empfängertabelle der Nachricht zurück.
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Bitmaske von Flags, die die Rückgabe der Tabelle steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht die erfolgreiche Rückgabe von **GetRecipientTable,** möglicherweise bevor die Tabelle für den aufrufenden Client vollständig verfügbar ist. Wenn die Tabelle nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler verursachen. 
    
MAPI_UNICODE 
  
> Zeichenfolgenspalten sollten im Unicode-Format vorliegen. Wenn das MAPI_UNICODE Flag nicht festgelegt ist, sollten die Zeichenfolgenspalten im ANSI-Format vorliegen.
    
 _lppTable_
  
> [out] Zeiger auf einen Zeiger auf die Empfängertabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfängertabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMessage::GetRecipientTable-Methode** gibt einen Zeiger auf die Empfängertabelle der Nachricht zurück, die Informationen zu allen Empfängern für die Nachricht enthält. Es gibt eine Zeile für jeden Empfänger. 
  
Für Empfängertabellen wird eine andere Spalte festgelegt, je nachdem, ob die Nachricht übermittelt wurde. Eine vollständige Liste der Spalten in einer Empfängertabelle finden Sie unter [Recipient Tables](recipient-tables.md).
  
Einige Empfängertabellen unterstützen eine Vielzahl von Einschränkungen. andere nicht. Die Unterstützung von Einschränkungen hängt von der Implementierung des Nachrichtenspeicheranbieters ab. 
  
Das Festlegen des MAPI_UNICODE Flags im  _ulFlags-Parameter_ wirkt sich auf die folgenden Aufrufe der Empfängertabelle aus: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) zum Abrufen des Spaltensatzes. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen von Zeilen. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) zum Abrufen der Sortierreihenfolge. 
    
Das Festlegen des Unicode-Flags fordert an, dass die Informationen für alle von diesen Aufrufen zurückgegebenen Zeichenfolgenspalten im Unicode-Format vorliegen. Da jedoch nicht alle Nachrichtenspeicheranbieter Unicode unterstützen, ist das Festlegen dieses Flags nur eine Anforderung.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können eine Empfängertabelle ändern, während sie geöffnet ist, indem Sie die [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) aufrufen. **ModifyRecipients** fügt Empfänger hinzu, löscht Empfänger oder ändert Empfängereigenschaften. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

