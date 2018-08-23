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
ms.openlocfilehash: 5908069f5fa887fd9d2e3f8c0df75f2e3d69515c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579536"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt die Empfänger der Nachricht-Tabelle zurück.
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Bitmaske aus Flags, die die Rückgabe von der Tabelle steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **GetRecipientTable** erfolgreich, möglicherweise beendet, bevor die Tabelle vollständig an den aufrufenden Client verfügbar ist. Wenn die Tabelle nicht verfügbar ist, kann nachfolgende anrufen darauf verursacht einen Fehler. 
    
PARAMETER MAPI_UNICODE 
  
> Zeichenfolgenspalten sollte im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sollte die Zeichenfolgenspalten im ANSI-Format sein.
    
 _lppTable_
  
> [out] Zeiger auf einen Zeiger auf die Empfänger Tabelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Empfänger Tabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMessage::GetRecipientTable** -Methode gibt einen Zeiger auf Empfänger die Nachricht-Tabelle, die Informationen zu allen der Empfänger der Nachricht enthält. Es wird eine Zeile für jeden Empfänger. 
  
Empfänger Tabellen ist eine andere Spalte festlegen, je nachdem, ob die Nachricht gesendet wurde. Eine vollständige Liste der Spalten in einer Tabelle Empfänger finden Sie unter [Empfänger Tabellen](recipient-tables.md).
  
Einige Empfänger Tabellen unterstützt eine Vielzahl von Einschränkungen. andere nicht. Unterstützung für Einschränkungen hängt von der Nachricht Informationsdienst Implementierung ab. 
  
Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ wirkt sich auf die folgenden Aufrufe an die Empfänger Tabelle aus: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) zum Abrufen der Spalte festlegen. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) abzurufenden Zeilen. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) , um die Sortierreihenfolge abzurufen. 
    
Durch Festlegen der Unicode-Flag-Anforderungen, die die Informationen für alle diese aufrufen zurückgegebenen Zeichenfolgenspalten im Unicode-Format sein. Da nicht alle Nachricht Anbieter Unicode unterstützen, ist jedoch festlegen dieses Flag nur eine Anforderung.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können eine Empfänger Tabelle ändern, während es geöffnet ist, indem Sie die [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode aufrufen. **ModifyRecipients** Fügt Empfänger, löscht Empfänger oder Empfängereigenschaften ändert. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

