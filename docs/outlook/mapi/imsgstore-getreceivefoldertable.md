---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421354"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf die Tabelle Receive Folder, eine Tabelle mit Informationen zu allen Empfangs Ordnern für den Nachrichtenspeicher.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Tabellenzugriff steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht es **GetReceiveFolderTable** , erfolgreich zurückzugeben, möglicherweise bevor die Tabelle vollständig für den Aufrufer verfügbar ist. Wenn die Tabelle nicht vollständig verfügbar ist, kann durch einen nachfolgenden Tabellen Aufruf ein Fehler ausgelöst werden. 
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 _lppTable_
  
> Out Ein Zeiger auf einen Zeiger auf die Tabelle des Empfangs Ordners.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Tabelle des Empfangs Ordners wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore:: GetReceiveFolderTable** -Methode ermöglicht den Zugriff auf eine Tabelle, in der die Eigenschafteneinstellungen für alle Empfangsordner des Nachrichtenspeichers angezeigt werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Eine Liste der erforderlichen Spalten in einer Tabelle mit einem Receive-Ordner finden Sie unter [Receive Folder Tables](receive-folder-tables.md). 
  
Implementieren Sie die Tabellen des Empfangs Ordners, um Einstellungs Einschränkungen für die **PR_RECORD_KEY** ([pidtagrecordkey (](pidtagrecordkey-canonical-property.md))-Eigenschaft zu unterstützen. Dies ermöglicht den einfachen Zugriff auf bestimmte Empfangsordner.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Das Festlegen des MAPI_UNICODE-Flags im _ulFlags_ -Parameter wirkt sich auf das Format der Spalten aus, die von den Methoden [IMAPITable:: QueryColumns](imapitable-querycolumns.md) und [IMAPITable:: QueryRows](imapitable-queryrows.md) zurückgegeben werden. Dieses Flag steuert auch die Eigenschaftentypen in der von der [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegebenen Sortierreihenfolge. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnDisplayReceiveFolderTable  <br/> |MFCMAPI verwendet die **IMsgStore:: GetReceiveFolderTable** -Methode, um die anzuzeigende Ordnertabelle abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

