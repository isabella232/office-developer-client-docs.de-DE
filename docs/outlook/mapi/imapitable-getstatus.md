---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8127a09582c98fc82fb5be92dbf24a4e84911ada
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575785"
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
  
> Der Inhalt der Tabelle hat sich erwartungsmäßig geändert. Dieser Statuswert wird für Änderungen, die sich aus Sortier- oder Einschränkungsvorgängen ergeben, nicht zurückgegeben.
    
TBLSTAT_RESTRICT_ERROR 
  
> Während eines [IMAPITable::Restrict-Vorgangs](imapitable-restrict.md) ist ein Fehler aufgetreten. 
    
TBLSTAT_RESTRICTING 
  
> Ein **IMAPITable::Restrict-Vorgang** wird ausgeführt. 
    
TBLSTAT_SETCOL_ERROR 
  
> Während eines [IMAPITable::SetColumns-Vorgangs](imapitable-setcolumns.md) ist ein Fehler aufgetreten. 
    
TBLSTAT_SETTING_COLS 
  
> Ein **IMAPITable::SetColumns-Vorgang** wird ausgeführt. 
    
TBLSTAT_SORT_ERROR 
  
> Während eines [IMAPITable::SortTable-Vorgangs](imapitable-sorttable.md) ist ein Fehler aufgetreten. 
    
TBLSTAT_SORTING 
  
> Ein **IMAPITable::SortTable-Vorgang** wird ausgeführt. 
    
 _lpulTableType_
  
> [out] Zeiger auf einen Wert, der den Typ der Tabelle angibt. Einer der folgenden drei Tabellentypen kann zurückgegeben werden:
    
TBLTYPE_DYNAMIC 
  
> Der Inhalt der Tabelle ist dynamisch. Die Zeilen- und Spaltenwerte können sich ändern, wenn sich die zugrunde liegenden Daten ändern.
    
TBLTYPE_KEYSET 
  
> Die Zeilen in der Tabelle sind fixiert, aber die Werte der Spalten innerhalb dieser Zeilen sind dynamisch und können sich ändern, wenn sich die zugrunde liegenden Daten ändern.
    
TBLTYPE_SNAPSHOT 
  
> Die Tabelle ist statisch, und ihr Inhalt ändert sich nicht, wenn sich die zugrunde liegenden Daten ändern.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status der Tabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPTable::GetStatus-Methode** ruft Informationen zum Typ einer Tabelle und zum aktuellen Status ab. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **GetStatus** in Verbindung mit drei anderen **IMAPITable-Methoden** verwenden, um den Status dieser Vorgänge zu überwachen und die Auswirkungen auf die Tabelle zu bestimmen. Rufen **Sie GetStatus** nach einem der folgenden **IMAPITable-Aufrufe** auf: 
  
- [IMAPITable::Restrict](imapitable-restrict.md) to set a restriction. 
    
- [IMAPITable::SortTable](imapitable-sorttable.md) zum Einrichten einer Sortierreihenfolge. 
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md) zum Definieren eines Spaltensatzes. 
    
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

