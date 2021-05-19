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
  
Bietet Zugriff auf die Tabelle "Empfangsordner", eine Tabelle, die Informationen zu allen Empfangsordnern für den Nachrichtenspeicher enthält.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Tabellenzugriff steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **getReceiveFolderTable,** erfolgreich zurückzukehren, möglicherweise bevor die Tabelle vollständig für den Aufrufer verfügbar ist. Wenn die Tabelle nicht vollständig verfügbar ist, kann ein nachfolgender Tabellenaufruf einen Fehler zur Folge haben. 
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Tabelle des Empfangsordners.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Tabelle "Empfangsordner" wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::GetReceiveFolderTable-Methode** bietet Zugriff auf eine Tabelle, in der die Eigenschafteneinstellungen für alle Empfangsordner des Nachrichtenspeichers angezeigt werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Eine Liste der erforderlichen Spalten in einer Tabelle mit Empfangsordnern finden Sie unter [Receive Folder Tables](receive-folder-tables.md). 
  
Implementieren Sie Ihre Empfangsordnertabellen, um Einstellungseinschränkungen für die **Eigenschaft PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) zu unterstützen. Dies ermöglicht einen einfachen Zugriff auf bestimmte Empfangsordner.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den [Methoden IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden. Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode zurückgegeben](imapitable-querysortorder.md) wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDisplayReceiveFolderTable  <br/> |MFCMAPI verwendet die **IMsgStore::GetReceiveFolderTable-Methode,** um die Empfangsordnertabelle zur Anzeige zu erhalten.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

