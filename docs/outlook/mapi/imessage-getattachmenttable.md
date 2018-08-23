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
ms.openlocfilehash: bf100ed916080a91366062f45b9e3349516bdb98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588517"
---
# <a name="imessagegetattachmenttable"></a>IMessage::GetAttachmentTable

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt die Nachricht Anlagentabelle zurück.
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Bitmaske aus Flags, die zur Erstellung der Tabelle beziehen. Das folgende Flag kann festgelegt werden: 
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgenspalten im ANSI-Format.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **GetAttachmentTable** erfolgreich, möglicherweise beendet, bevor die Tabelle vollständig an den aufrufenden Client verfügbar ist. Wenn die Tabelle nicht verfügbar ist, kann nachfolgende anrufen darauf verursacht einen Fehler. 
    
 _lppTable_
  
> [out] Zeiger auf einen Zeiger auf die Anlagentabelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Anlagentabelle wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMessage::GetAttachmentTable** -Methode gibt einen Zeiger auf die Nachricht Anlagentabelle, die Informationen zu allen Anlagen in der Nachricht enthält. Clients erhalten Zugriff auf eine Anlage nur über die Anlagentabelle. Durch Abrufen einer Anlage Anzahl seiner **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft ein Client verschiedenen **IMessage** -Methoden können Sie die Anlage entwickelt. 
  
Es wird eine Zeile für jede Anlage. Eine vollständige Liste der Spalten in einer Anlagentabelle finden Sie unter [Anhang Tabellen](attachment-tables.md).
  
Eine Anlage wird in der Anlagentabelle in der Regel nicht angezeigt, bis die Anlage und die Nachricht mit einem Aufruf von [IMAPIProp::SaveChanges](imapiprop-savechanges.md)gespeichert wurden. Anlagentabellen sind dynamisch. Wenn ein Client eine neue Anlage erstellt, eine vorhandene Anlage löscht oder eine oder mehrere Eigenschaften geändert, sobald die **SaveChanges** -Ruft die Anlage der Nachricht vorgenommen wurden, wird die Anlagentabelle, um die neuen Informationen aktualisiert. 
  
Einige Anlagentabellen unterstützt eine Vielzahl von Einschränkungen. andere nicht. Unterstützung für Einschränkungen hängt von der Nachricht Informationsdienst Implementierung ab. 
  
Beim ersten Öffnen, werden die Anlagentabellen nicht unbedingt in einer bestimmten Reihenfolge sortiert. 
  
Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ wirkt sich auf die folgenden Aufrufe an die Anlagentabelle aus: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) zum Abrufen der Spalte festlegen. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) abzurufenden Zeilen. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) , um die Sortierreihenfolge abzurufen. 
    
Durch Festlegen der Unicode-Flag-Anforderungen, die die Informationen für alle diese aufrufen zurückgegebenen Zeichenfolgenspalten im Unicode-Format sein. Da nicht alle Nachricht Anbieter Unicode unterstützen, ist jedoch festlegen dieses Flag nur eine Anforderung.
  
## <a name="see-also"></a>Siehe auch



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

