---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407137"
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
  
> [in] Eine Bitmaske mit Flags, die das Format für Spalten bestimmt, die Zeichenzeichenfolgen sind. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgenspalten im ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Statustabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Tabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::GetStatusTable-Methode** bietet Zugriff auf die Statustabelle, die Informationen zu allen MAPI-Ressourcen in der Sitzung enthält. Die Tabelle enthält eine Zeile mit Informationen zum MAPI-Subsystem, eine Zeile für den MAPI-Spooler, eine Zeile für das integrierte Adressbuch und eine Zeile für jeden Dienstanbieter im Profil. 
  
Eine vollständige Liste der erforderlichen und optionalen Spalten in der Statustabelle finden Sie unter [Status Tables](status-tables.md). 
  
Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den [Methoden IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden. Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode zurückgegeben](imapitable-querysortorder.md) wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnStatusTable  <br/> |MFCMAPI verwendet die **IMAPISession::GetStatusTable-Methode,** um die Statustabelle zu erhalten, die gerendert werden soll.  <br/> |
   
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

