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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328896"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Status und den Typ der Tabelle zurück.
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>Parameter

 _lpulTableStatus_
  
> Out Zeiger auf einen Wert, der den Status der Tabelle angibt. Einer der folgenden Werte kann zurückgegeben werden:
    
TBLSTAT_COMPLETE 
  
> Es werden keine Vorgänge ausgeführt.
    
TBLSTAT_QCHANGED 
  
> Der Inhalt der Tabelle wurde erwartungsvoll geändert. Dieser Statuswert wird nicht für Änderungen zurückgegeben, die aus Sortier-oder Einschränkungs Vorgängen resultieren.
    
TBLSTAT_RESTRICT_ERROR 
  
> Während eines [IMAPITable:: Restrict](imapitable-restrict.md) -Vorgangs ist ein Fehler aufgetreten. 
    
TBLSTAT_RESTRICTING 
  
> Ein **IMAPITable:: Restrict** -Vorgang wird ausgeführt. 
    
TBLSTAT_SETCOL_ERROR 
  
> Während eines [IMAPITable::](imapitable-setcolumns.md) SetColumns-Vorgangs ist ein Fehler aufgetreten. 
    
TBLSTAT_SETTING_COLS 
  
> Ein **IMAPITable::** SetColumns-Vorgang wird ausgeführt. 
    
TBLSTAT_SORT_ERROR 
  
> Während eines [IMAPITable:: sortable](imapitable-sorttable.md) -Vorgangs ist ein Fehler aufgetreten. 
    
TBLSTAT_SORTING 
  
> Ein **IMAPITable:: sortable** -Vorgang wird ausgeführt. 
    
 _lpulTableType_
  
> Out Zeiger auf einen Wert, der den Typ der Tabelle angibt. Einer der folgenden drei Tabellentypen kann zurückgegeben werden:
    
TBLTYPE_DYNAMIC 
  
> Der Inhalt der Tabelle ist dynamisch; die Zeilen-und Spaltenwerte können sich ändern, wenn die zugrunde liegenden Daten geändert werden.
    
TBLTYPE_KEYSET 
  
> Die Zeilen in der Tabelle sind festgelegt, aber die Werte der Spalten innerhalb dieser Zeilen sind dynamisch und können geändert werden, wenn die zugrunde liegenden Daten geändert werden.
    
TBLTYPE_SNAPSHOT 
  
> Die Tabelle ist statisch, und ihr Inhalt ändert sich nicht, wenn sich die zugrunde liegenden Daten ändern.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status der Tabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **imapable:: GetStatus** -Methode ruft Informationen über den Typ einer Tabelle und den aktuellen Status ab. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **GetStatus** in Verbindung mit drei anderen **IMAPITable** -Methoden verwenden, um den Status dieser Vorgänge zu überwachen und die Auswirkungen auf die Tabelle zu bestimmen. Rufen **** Sie GetStatus auf, nachdem Sie einen der folgenden **IMAPITable** -Aufrufe durchführen: 
  
- [IMAPITable:: einschränken](imapitable-restrict.md) , um eine Einschränkung festzulegen. 
    
- [IMAPITable:: sortable](imapitable-sorttable.md) , um eine Sortierreihenfolge einzurichten. 
    
- [IMAPITable::](imapitable-setcolumns.md) SetColumns zum Definieren eines Spaltensatzes. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl:: GetStatus  <br/> |MFCMAPI verwendet die **IMAPITable:: GetStatus** -Methode, um den Status einer Tabelle zu melden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

