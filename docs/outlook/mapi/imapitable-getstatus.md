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
ms.openlocfilehash: 6478f2c6c8196fa332a7b019269e6a6266485d1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792472"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**Betrifft**: Outlook 
  
Status und Typ der Tabelle zurückgegeben.
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>Parameter

 _lpulTableStatus_
  
> [out] Zeiger auf einen Wert, der den Status der Tabelle. Die folgenden Werte kann zurückgegeben werden:
    
TBLSTAT_COMPLETE 
  
> Keine Vorgänge werden durchgeführt.
    
TBLSTAT_QCHANGED 
  
> Der Inhalt der Tabelle haben expectantly geändert. Dieser Statuswert wird nicht für Änderungen zurückgegeben, die aus sortieren oder Einschränkung Vorgänge.
    
TBLSTAT_RESTRICT_ERROR 
  
> Während eines Vorgangs [Methode IMAPITable:: Restrict](imapitable-restrict.md) ist ein Fehler aufgetreten. 
    
TBLSTAT_RESTRICTING 
  
> Ein **Methode IMAPITable:: Restrict** -Vorgang wird gerade durchgeführt. 
    
TBLSTAT_SETCOL_ERROR 
  
> Während eines Vorgangs [IMAPITable::SetColumns](imapitable-setcolumns.md) ist ein Fehler aufgetreten. 
    
TBLSTAT_SETTING_COLS 
  
> Ein **IMAPITable::SetColumns** Vorgang ist in Bearbeitung. 
    
TBLSTAT_SORT_ERROR 
  
> Während eines Vorgangs [SortTable](imapitable-sorttable.md) ist ein Fehler aufgetreten. 
    
TBLSTAT_SORTING 
  
> Ein Vorgang **SortTable** wird gerade durchgeführt. 
    
 _lpulTableType_
  
> [out] Zeiger auf einen Wert vom Typ der Tabelle an. Eine der folgenden drei Tabelle kann zurückgegeben:
    
TBLTYPE_DYNAMIC 
  
> Die Tabelle Inhalt sind dynamisch; die Zeilen und Spaltenwerte können die zugrunde liegenden Daten geändert ändern.
    
TBLTYPE_KEYSET 
  
> Die Zeilen innerhalb der Tabelle behoben werden, aber die Werte der Spalten in diesen Zeilen sind dynamisch und ändern können, als die zugrunde liegenden Daten geändert.
    
TBLTYPE_SNAPSHOT 
  
> Die Tabelle sind statisch, und dessen Inhalt nicht ändern, wenn die zugrunde liegenden Daten geändert.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Tabelle Status wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPTable::GetStatus** -Methode ruft Informationen über den Typ und den aktuellen Status einer Tabelle ab. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **GetStatus** in Verbindung mit drei **IMAPITable** -Methoden verwenden, den Status von Vorgängen überwachen und bestimmen die Auswirkung auf die Tabelle. Rufen Sie nach dem Ändern eines der folgenden **IMAPITable** Aufrufe **GetStatus** : 
  
- [Methode IMAPITable:: Restrict](imapitable-restrict.md) eine Einschränkung festlegen. 
    
- [SortTable](imapitable-sorttable.md) keine Sortierreihenfolge herstellen. 
    
- Legen Sie [IMAPITable::SetColumns](imapitable-setcolumns.md) für eine Spalte definieren. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |MFCMAPI (engl.) wird die **IMAPITable::GetStatus** -Methode verwendet, um den Status einer Tabelle Berichten.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

