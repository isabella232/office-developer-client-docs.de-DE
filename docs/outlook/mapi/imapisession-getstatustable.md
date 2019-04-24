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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338760"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf die Statustabelle, eine Tabelle, die Informationen zu allen MAPI-Ressourcen in der Sitzung enthält.
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die das Format für Spalten bestimmt, die Zeichen Zeichenfolgen sind. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind die Zeichenfolgenspalten im ANSI-Format.
    
 _lppTable_
  
> Out Ein Zeiger auf einen Zeiger auf die Statustabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Tabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession::** getstatusable-Methode ermöglicht den Zugriff auf die Statustabelle, die Informationen zu allen MAPI-Ressourcen in der Sitzung enthält. Es gibt eine Zeile in der Tabelle für Informationen zum MAPI-Subsystem, eine Zeile für den MAPI-Spooler, eine Zeile für das integrierte Adressbuch und eine Zeile für jeden Dienstanbieter im Profil. 
  
Eine vollständige Liste der erforderlichen und optionalen Spalten in der Statustabelle finden Sie unter [Statustabellen](status-tables.md). 
  
Das Festlegen des MAPI_UNICODE-Flags im _ulFlags_ -Parameter wirkt sich auf das Format der Spalten aus, die von den Methoden [IMAPITable:: QueryColumns](imapitable-querycolumns.md) und [IMAPITable:: QueryRows](imapitable-queryrows.md) zurückgegeben werden. Dieses Flag steuert auch die Eigenschaftentypen in der von der [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegebenen Sortierreihenfolge. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: onStatus-Eigenschaft  <br/> |MFCMAPI verwendet die **IMAPISession::** getstatusable-Methode, um die zu rendernde Statustabelle abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Status Tabellen](status-tables.md)

