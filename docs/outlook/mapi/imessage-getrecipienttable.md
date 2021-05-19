---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ca42e91528cdb7e61ae3620989c4a89966db1061
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424609"
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
  
> [in] Bitmaske von Flags, die die Rückgabe der Tabelle steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **getRecipientTable,** erfolgreich zurückzukehren, möglicherweise bevor die Tabelle vollständig für den aufrufenden Client verfügbar ist. Wenn die Tabelle nicht verfügbar ist, kann ein nachfolgender Aufruf der Tabelle zu einem Fehler führen. 
    
MAPI_UNICODE 
  
> Zeichenfolgenspalten sollten im Unicode-Format vorliegen. Wenn das MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgenspalten im ANSI-Format vorliegen.
    
 _lppTable_
  
> [out] Zeiger auf einen Zeiger auf die Empfängertabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfängertabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IMessage::GetRecipientTable-Methode** gibt einen Zeiger auf die Empfängertabelle der Nachricht zurück, die Informationen zu allen Empfängern für die Nachricht enthält. Es gibt eine Zeile für jeden Empfänger. 
  
Empfängertabellen haben einen anderen Spaltensatz, je nachdem, ob die Nachricht übermittelt wurde. Eine vollständige Liste der Spalten in einer Empfängertabelle finden Sie unter [Recipient Tables](recipient-tables.md).
  
Einige Empfängertabellen unterstützen eine Vielzahl von Einschränkungen. Andere tun dies nicht. Die Unterstützung für Einschränkungen hängt von der Implementierung des Nachrichtenspeicheranbieters ab. 
  
Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ wirkt sich auf die folgenden Aufrufe an die Empfängertabelle aus: 
  
- [IMAPITable::QueryColumns,](imapitable-querycolumns.md) um den Spaltensatz abzurufen. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen von Zeilen. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) zum Abrufen der Sortierreihenfolge. 
    
Das Festlegen des Unicode-Kennzeichens fordert, dass die Informationen für alle von diesen Aufrufen zurückgegebenen Zeichenfolgenspalten im Unicode-Format vorliegen. Da jedoch nicht alle Nachrichtenspeicheranbieter Unicode unterstützen, ist das Festlegen dieses Kennzeichens nur eine Anforderung.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können eine Empfängertabelle ändern, während sie geöffnet ist, indem Sie die [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) aufrufen. **ModifyRecipients** fügt Empfänger hinzu, löscht Empfänger oder ändert Empfängereigenschaften. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

