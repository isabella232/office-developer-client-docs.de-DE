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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349273"
---
# <a name="imessagegetattachmenttable"></a>IMessage::GetAttachmentTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Anlage Tabelle der Nachricht zurück.
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Bitmaske von Flags, die sich auf die Erstellung der Tabelle beziehen. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind die Zeichenfolgenspalten im ANSI-Format.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **** getattachmentable, um erfolgreich zurückzugeben, möglicherweise bevor die Tabelle vollständig für den aufrufenden Client verfügbar ist. Wenn die Tabelle nicht verfügbar ist, kann der nachfolgende Aufruf einen Fehler verursachen. 
    
 _lppTable_
  
> Out Zeiger auf einen Zeiger auf die Anlagentabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Attachment-Tabelle wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMessage::** getattachmentable-Methode gibt einen Zeiger auf die Attachment-Tabelle der Nachricht zurück, die Informationen zu allen Anlagen in der Nachricht enthält. Clients können Zugriff auf eine Anlage nur über die Attachment-Tabelle erhalten. Durch das Abrufen der Nummer einer Anlage die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft kann ein Client mehrere der **IMessage** -Methoden verwenden, um mit der Anlage zu arbeiten. 
  
Für jede Anlage gibt es eine Zeile. Eine vollständige Liste der Spalten in einer Attachment-Tabelle finden Sie unter [Attachment Tables](attachment-tables.md).
  
Eine Anlage wird in der Regel erst dann in der Anlage Tabelle angezeigt, wenn die Anlage und die Nachricht mit einem Aufruf von [IMAPIProp:: SaveChanges](imapiprop-savechanges.md)gespeichert wurden. Anlagen Tabellen sind dynamisch. Wenn ein Client eine neue Anlage erstellt, eine vorhandene Anlage löscht oder eine oder mehrere Eigenschaften ändert, nachdem die **SaveChanges** -Aufrufe für die Anlage in der Nachricht vorgenommen wurden, wird die Anlage Tabelle aktualisiert, um die neuen Informationen widerzuspiegeln. 
  
Einige Anlagen Tabellen unterstützen eine Vielzahl von Einschränkungen; andere nicht. Die Unterstützung von Einschränkungen hängt von der Implementierung des Nachrichtenspeicher Anbieters ab. 
  
Beim anfänglichen öffnen werden Anlagen Tabellen nicht unbedingt in einer bestimmten Reihenfolge sortiert. 
  
Das Festlegen des MAPI_UNICODE-Flags im _ulFlags_ -Parameter wirkt sich auf die folgenden Aufrufe der Attachment-Tabelle aus: 
  
- [IMAPITable:: QueryColumns](imapitable-querycolumns.md) zum Abrufen des Spaltensatzes. 
    
- [IMAPITable:: QueryRows](imapitable-queryrows.md) zum Abrufen von Zeilen. 
    
- [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) , um die Sortierreihenfolge abzurufen. 
    
Durch Festlegen des Unicode-Kennzeichens wird angefordert, dass die Informationen für Zeichenfolgenspalten, die von diesen Aufrufen zurückgegeben werden, im Unicode-Format vorliegen. Da jedoch nicht alle Nachrichtenspeicher Anbieter Unicode unterstützen, ist das Festlegen dieses Kennzeichens nur eine Anforderung.
  
## <a name="see-also"></a>Siehe auch



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

