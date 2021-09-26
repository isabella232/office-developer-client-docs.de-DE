---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e7c00cc8fa6f651ded26b23522eb4943195c27f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620933"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf die Nachrichtenspeichertabelle, die Informationen zu allen Nachrichtenspeichern im Sitzungsprofil enthält.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Format für Spalten bestimmt, bei denen es sich um Zeichenfolgen handelt. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgenspalten das ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Nachrichtenspeichertabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Tabelle wurde erfolgreich zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Das MAPI_UNICODE Flag wurde festgelegt, und die Sitzung unterstützt unicode nicht.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession::GetMsgStoresTable-Methode** ruft einen Zeiger auf die Nachrichtenspeichertabelle ab, eine von mapi verwaltete Tabelle, die Informationen zu jedem geöffneten Nachrichtenspeicher im Profil enthält. 
  
Eine vollständige Liste der erforderlichen und optionalen Spalten in der Nachrichtenspeichertabelle finden Sie unter [Message Store Tables](message-store-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da die MAPI die Nachrichtenspeichertabelle während der Sitzung aktualisiert, wenn Änderungen auftreten, rufen Sie die **Advise-Methode** der Nachrichtenspeichertabelle auf, um sich zu registrieren, um über diese Änderungen benachrichtigt zu werden. Mögliche Änderungen sind das Hinzufügen neuer Nachrichtenspeicher, das Entfernen vorhandener Speicher und Änderungen am Standardspeicher. 
  
Das Festlegen des MAPI_UNICODE Flags im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden. Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode](imapitable-querysortorder.md) zurückgegeben wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI verwendet die **IMAPISession::GetMsgStoresTable-Methode,** um die Nachrichtenspeichertabelle abzurufen, damit sie im Hauptdialogfeld von MFCMAPI gerendert werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Nachrichten Store Tabellen](message-store-tables.md)

