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
  
> in Bitmaske von Flags, die die Rückgabe der Tabelle steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **** getrecipientable, um erfolgreich zurückzugeben, möglicherweise bevor die Tabelle vollständig für den aufrufenden Client verfügbar ist. Wenn die Tabelle nicht verfügbar ist, kann der nachfolgende Aufruf einen Fehler verursachen. 
    
MAPI_UNICODE 
  
> Zeichenfolgenspalten sollten im Unicode-Format vorliegen. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sollten die Zeichenfolgenspalten im ANSI-Format sein.
    
 _lppTable_
  
> Out Zeiger auf einen Zeiger auf die Empfängertabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfängertabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMessage::** getrecipientable-Methode gibt einen Zeiger auf die Empfängertabelle der Nachricht zurück, die Informationen zu allen Empfängern der Nachricht enthält. Es gibt eine Zeile für jeden Empfänger. 
  
Empfänger Tabellen haben unterschiedliche Spaltensätze, je nachdem, ob die Nachricht übermittelt wurde. Eine vollständige Liste der Spalten in einer Empfängertabelle finden Sie unter [Recipient Tables](recipient-tables.md).
  
Einige Empfänger Tabellen unterstützen eine Vielzahl von Einschränkungen; andere nicht. Die Unterstützung von Einschränkungen hängt von der Implementierung des Nachrichtenspeicher Anbieters ab. 
  
Das Festlegen des MAPI_UNICODE-Flags im _ulFlags_ -Parameter wirkt sich auf die folgenden Aufrufe der Recipient-Tabelle aus: 
  
- [IMAPITable:: QueryColumns](imapitable-querycolumns.md) zum Abrufen des Spaltensatzes. 
    
- [IMAPITable:: QueryRows](imapitable-queryrows.md) zum Abrufen von Zeilen. 
    
- [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) , um die Sortierreihenfolge abzurufen. 
    
Durch Festlegen des Unicode-Kennzeichens wird angefordert, dass die Informationen für Zeichenfolgenspalten, die von diesen Aufrufen zurückgegeben werden, im Unicode-Format vorliegen. Da jedoch nicht alle Nachrichtenspeicher Anbieter Unicode unterstützen, ist das Festlegen dieses Kennzeichens nur eine Anforderung.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können eine Empfängertabelle ändern, während Sie geöffnet ist, indem Sie die [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode aufrufen. **ModifyRecipients** fügt Empfänger hinzu, löscht Empfänger oder ändert Empfänger Eigenschaften. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

