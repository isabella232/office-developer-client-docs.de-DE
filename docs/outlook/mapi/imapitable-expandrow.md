---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415166"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erweitert eine reduzierte Tabellenkategorie und fügt der Tabellenansicht die Überschriftenzeilen auf Blatt- oder Unterebene hinzu, die der Kategorie zugeordnet sind.
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a>Parameter

 _cbInstanceKey_
  
> [in] Die Anzahl der Bytes in der PR_INSTANCE_KEY, auf die der  _pbInstanceKey-Parameter_ verweist. 
    
 _pbInstanceKey_
  
> [in] Ein Zeiger auf die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaft, die die Überschriftenzeile für die Kategorie identifiziert. 
    
 _ulRowCount_
  
> [in] Die maximale Anzahl von Zeilen, die im  _lppRows-Parameter zurückgegeben werden_ sollen. 
    
 _ulFlags_
  
> Reserviert; muss null sein.
    
 _lppRows_
  
> [out] Ein Zeiger auf eine [SRowSet-Struktur,](srowset.md) die die ersten Zeilen (bis  _ulRowCount)_ empfängt, die als Ergebnis der Erweiterung in die Tabellenansicht eingefügt wurden. Diese Zeilen werden nach der überschriftenzeile eingefügt, die durch den  _pbInstanceKey-Parameter identifiziert_ wurde. Der  _lppRows-Parameter_ kann NULL sein, wenn  _der ulRowCount-Parameter_ null ist. 
    
 _lpulMoreRows_
  
> [out] Ein Zeiger auf die Gesamtanzahl der Zeilen, die der Tabellenansicht hinzugefügt wurden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Kategorie wurde erfolgreich erweitert.
    
MAPI_E_NOT_FOUND 
  
> Die vom  _pbInstanceKey-Parameter_ identifizierte Zeile ist nicht vorhanden. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::ExpandRow-Methode** erweitert eine reduzierte Tabellenkategorie und fügt der Tabellenansicht die Überschriftenzeilen auf Blatt- oder unterer Ebene hinzu, die zur Kategorie gehören. Ein Grenzwert für die Anzahl der Zeilen, die im  _lppRows-Parameter_ zurückgegeben werden sollen, kann im  _ulRowCount-Parameter angegeben_ werden. Wenn  _ulRowCount_ auf einen Wert festgelegt ist, der größer als Null ist und eine oder mehrere Zeilen in dem Zeilensatz zurückgegeben werden, auf den  _lppRows_ verweist, wird die Position der Textmarke BOOKMARK_CURRENT in die Zeile unmittelbar nach der letzten Zeile im Zeilensatz verschoben.
  
Wenn  _ulRowCount_ auf Null festgelegt ist und fordert, dass der Kategorie Keine Blattzeilen oder Zeilen auf unterer Ebene hinzugefügt werden, oder null Zeilen zurückgegeben werden, da keine Zeilen auf Blatt- oder unterer Ebene in der Kategorie vorhanden sind, wird die Position von BOOKMARK_CURRENT auf die Zeile festgelegt, die der zeile folgt, die durch  _pbInstanceKey_ identifiziert wurde. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Generieren Sie keine Benachrichtigungen für Zeilen, die aufgrund der Kategorieerweiterung einer Tabellenansicht hinzugefügt werden.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die Anzahl der Zeilen im Zeilensatz, auf die der  _lppRows-Parameter_ verweist, entspricht möglicherweise nicht der Anzahl der Zeilen, die der Tabelle hinzugefügt wurden, dem gesamten Satz von Blatt- oder Unterzeilen für die Kategorie. Fehler können auftreten, z. B. unzureichender Arbeitsspeicher oder die Anzahl der Zeilen in der Kategorie, die die im  _ulRowCount-Parameter_ angegebene Anzahl überschreitet. In beiden Fällen wird BOOKMARK_CURRENT an der letzten zurückgegebenen Zeile positioniert. Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md)auf, um die restlichen Zeilen in der Kategorie sofort abzurufen.
  
Erwarten Sie keine Tabellenbenachrichtigung, wenn eine Kategorie ihren Status ändert. Sie können einen lokalen Cache von Zeilen verwalten, der mit jedem **ExpandRow-** oder **CollapseRow-Aufruf aktualisiert werden** kann. 
  
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sorting and Categorization](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI verwendet die **IMAPITable::ExpandRow-Methode,** um eine reduzierte Tabellenkategorie zu erweitern.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

