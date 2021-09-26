---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e9f8eb5e8c5bb21e7c1a9a61d6dfd85630d2f553
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620688"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf die Empfangsordnertabelle, eine Tabelle, die Informationen zu allen Empfangsordnern für den Nachrichtenspeicher enthält.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Tabellenzugriff steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **getReceiveFolderTable** die erfolgreiche Rückgabe, möglicherweise bevor die Tabelle für den Aufrufer vollständig verfügbar ist. Wenn die Tabelle nicht vollständig verfügbar ist, kann durch einen nachfolgenden Tabellenaufruf ein Fehler ausgelöst werden. 
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Empfangsordnertabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfangsordnertabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore::GetReceiveFolderTable-Methode** ermöglicht den Zugriff auf eine Tabelle, in der die Eigenschafteneinstellungen für alle Empfangsordner des Nachrichtenspeichers angezeigt werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Eine Liste der erforderlichen Spalten in einer Empfangsordnertabelle finden Sie unter ["Ordnertabellen empfangen".](receive-folder-tables.md) 
  
Implementieren Sie Ihre Empfangsordnertabellen, um das Festlegen von Eigenschaftseinschränkungen für die **PR_RECORD_KEY** -[PidTagRecordKey](pidtagrecordkey-canonical-property.md)) -Eigenschaft zu unterstützen. Dies ermöglicht den einfachen Zugriff auf bestimmte Empfangsordner.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Das Festlegen des MAPI_UNICODE Flags im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden. Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode](imapitable-querysortorder.md) zurückgegeben wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDisplayReceiveFolderTable  <br/> |MFCMAPI verwendet die **IMsgStore::GetReceiveFolderTable-Methode,** um die anzuzeigende Empfangsordnertabelle abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

