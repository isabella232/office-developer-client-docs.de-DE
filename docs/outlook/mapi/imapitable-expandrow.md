---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ca03023d7edd81db214c080b8d4a744c1bf661cc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620828"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erweitert eine reduzierte Tabellenkategorie und fügt der Tabellenansicht die untergeordneten Überschriftenzeilen hinzu, die zur Kategorie gehören.
  
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
  
> [in] Die Anzahl der Bytes in der PR_INSTANCE_KEY-Eigenschaft, auf die der  _PbInstanceKey-Parameter_ verweist. 
    
 _pbInstanceKey_
  
> [in] Ein Zeiger auf die **eigenschaft PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), die die Überschriftenzeile für die Kategorie identifiziert. 
    
 _ulRowCount_
  
> [in] Die maximale Anzahl von Zeilen, die im  _lppRows-Parameter_ zurückgegeben werden sollen. 
    
 _ulFlags_
  
> Reserviert; muss Null sein.
    
 _lppRows_
  
> [out] Ein Zeiger auf eine [SRowSet-Struktur,](srowset.md) die die ersten (bis zu  _ulRowCount)_ Zeilen empfängt, die aufgrund der Erweiterung in die Tabellenansicht eingefügt wurden. Diese Zeilen werden nach der Überschriftenzeile eingefügt, die durch den  _PbInstanceKey-Parameter_ identifiziert wird. Der  _lppRows-Parameter_ kann NULL sein, wenn der  _ulRowCount-Parameter_ Null ist. 
    
 _lpulMoreRows_
  
> [out] Ein Zeiger auf die Gesamtzahl der Zeilen, die der Tabellenansicht hinzugefügt wurden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Kategorie wurde erfolgreich erweitert.
    
MAPI_E_NOT_FOUND 
  
> Die vom  _PbInstanceKey-Parameter_ identifizierte Zeile ist nicht vorhanden. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::ExpandRow-Methode** erweitert eine reduzierte Tabellenkategorie und fügt der Tabellenansicht die Untergeordneten oder Überschriftenzeilen auf unterer Ebene hinzu, die zur Kategorie gehören. Ein Grenzwert für die Anzahl der Zeilen, die im  _lppRows-Parameter_ zurückgegeben werden sollen, kann im  _ulRowCount-Parameter_ angegeben werden. Wenn  _ulRowCount_ auf einen Wert größer als Null festgelegt ist und eine oder mehrere Zeilen in dem Zeilensatz zurückgegeben werden, auf den durch  _lppRows_ verwiesen wird, wird die Position der Textmarke BOOKMARK_CURRENT unmittelbar nach der letzten Zeile im Zeilensatz in die Zeile verschoben.
  
Wenn  _ulRowCount_ auf Null festgelegt ist und die Anforderung, dass Zeilen mit der Überschrift null oder der unteren Ebene zur Kategorie hinzugefügt werden sollen, oder null Zeilen zurückgegeben werden, da keine Zeilen mit der Überschrift auf der unteren Ebene oder auf der unteren Ebene in der Kategorie vorhanden sind, wird die Position von BOOKMARK_CURRENT auf die Zeile festgelegt, die auf die zeile folgt, die durch  _pbInstanceKey_ identifiziert wurde. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Generieren Sie keine Benachrichtigungen für Zeilen, die einer Tabellenansicht aufgrund der Kategorieerweiterung hinzugefügt werden.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die Anzahl der Zeilen in der Zeile, auf die durch den  _Parameter "lppRows"_ verwiesen wird, entspricht möglicherweise nicht der Anzahl der Zeilen, die der Tabelle tatsächlich hinzugefügt wurden, der gesamten Gruppe von Zeilen mit untergeordneten Zeilen oder Überschriften auf unterer Ebene für die Kategorie. Fehler können auftreten, z. B. unzureichender Arbeitsspeicher oder die Anzahl der Zeilen in der Kategorie, die die im  _ulRowCount-Parameter_ angegebene Anzahl überschreitet. In beiden Fällen wird BOOKMARK_CURRENT an der letzten zurückgegebenen Zeile positioniert. Um die restlichen Zeilen in der Kategorie sofort abzurufen, rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md)auf.
  
Erwarten Sie keine Tabellenbenachrichtigung, wenn sich der Status einer Kategorie ändert. Sie können einen lokalen Cache von Zeilen verwalten, der mit jedem **ExpandRow-** oder **CollapseRow-Aufruf** aktualisiert werden kann. 
  
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und Kategorisieren.](sorting-and-categorization.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI verwendet die **IMAPITable::ExpandRow-Methode,** um eine reduzierte Tabellenkategorie zu erweitern.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

