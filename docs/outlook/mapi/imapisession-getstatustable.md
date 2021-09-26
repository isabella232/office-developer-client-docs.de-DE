---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8c76d4fb1654b55a15d2c86db7ede25d1fc26da9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620898"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf die Statustabelle, eine Tabelle, die Informationen zu allen MAPI-Ressourcen in der Sitzung enthält.
  
```cpp
HRESULT GetStatusTable(
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
  
> [out] Ein Zeiger auf einen Zeiger auf die Statustabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Tabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession::GetStatusTable-Methode** ermöglicht den Zugriff auf die Statustabelle, die Informationen zu allen MAPI-Ressourcen in der Sitzung enthält. Die Tabelle enthält eine Zeile mit Informationen zum MAPI-Subsystem, eine Zeile für den MAPI-Spooler, eine Zeile für das integrierte Adressbuch und eine Zeile für jeden Dienstanbieter im Profil. 
  
Eine vollständige Liste der erforderlichen und optionalen Spalten in der Statustabelle finden Sie unter [Statustabellen.](status-tables.md) 
  
Das Festlegen des MAPI_UNICODE Flags im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden. Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode](imapitable-querysortorder.md) zurückgegeben wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnStatusTable  <br/> |MFCMAPI verwendet die **IMAPISession::GetStatusTable-Methode,** um die statustabelle abzurufen, die gerendert werden soll.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Statustabellen](status-tables.md)

