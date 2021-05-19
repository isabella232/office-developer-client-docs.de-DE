---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434333"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Status und Typ der Tabelle zurück.
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>Parameter

 _lpulTableStatus_
  
> [out] Zeiger auf einen Wert, der den Status der Tabelle angibt. Einer der folgenden Werte kann zurückgegeben werden:
    
TBLSTAT_COMPLETE 
  
> Es werden keine Vorgänge ausgeführt.
    
TBLSTAT_QCHANGED 
  
> Der Inhalt der Tabelle hat sich erwartungslich geändert. Dieser Statuswert wird nicht für Änderungen zurückgegeben, die aus Sortier- oder Einschränkungsvorgängen resulten.
    
TBLSTAT_RESTRICT_ERROR 
  
> Bei einem [IMAPITable::Restrict-Vorgang](imapitable-restrict.md) ist ein Fehler aufgetreten. 
    
TBLSTAT_RESTRICTING 
  
> Ein **IMAPITable::Restrict-Vorgang** wird ausgeführt. 
    
TBLSTAT_SETCOL_ERROR 
  
> Bei einem [IMAPITable::SetColumns-Vorgang](imapitable-setcolumns.md) ist ein Fehler aufgetreten. 
    
TBLSTAT_SETTING_COLS 
  
> Ein **IMAPITable::SetColumns-Vorgang** wird ausgeführt. 
    
TBLSTAT_SORT_ERROR 
  
> Bei einem [IMAPITable::SortTable-Vorgang](imapitable-sorttable.md) ist ein Fehler aufgetreten. 
    
TBLSTAT_SORTING 
  
> Ein **IMAPITable::SortTable-Vorgang** wird ausgeführt. 
    
 _lpulTableType_
  
> [out] Zeiger auf einen Wert, der den Typ der Tabelle angibt. Einer der folgenden drei Tabellentypen kann zurückgegeben werden:
    
TBLTYPE_DYNAMIC 
  
> Der Inhalt der Tabelle ist dynamisch. Die Zeilen- und Spaltenwerte können sich ändern, wenn sich die zugrunde liegenden Daten ändern.
    
TBLTYPE_KEYSET 
  
> Die Zeilen in der Tabelle sind fest, aber die Werte der Spalten in diesen Zeilen sind dynamisch und können sich ändern, wenn sich die zugrunde liegenden Daten ändern.
    
TBLTYPE_SNAPSHOT 
  
> Die Tabelle ist statisch, und ihr Inhalt ändert sich nicht, wenn sich die zugrunde liegenden Daten ändern.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status der Tabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IMAPTable::GetStatus-Methode** ruft Informationen zum Typ und aktuellen Status einer Tabelle ab. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **GetStatus** zusammen mit drei anderen **IMAPITable-Methoden** verwenden, um den Status dieser Vorgänge zu überwachen und die Auswirkungen auf die Tabelle zu bestimmen. Rufen **Sie GetStatus** nach einem der folgenden **IMAPITable-Aufrufe** auf: 
  
- [IMAPITable::Restrict,](imapitable-restrict.md) um eine Einschränkung festlegen. 
    
- [IMAPITable::SortTable](imapitable-sorttable.md) zum Einrichten einer Sortierreihenfolge. 
    
- [IMAPITable::SetColumns,](imapitable-setcolumns.md) um einen Spaltensatz zu definieren. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |MFCMAPI verwendet die **IMAPITable::GetStatus-Methode,** um den Status einer Tabelle zu melden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

