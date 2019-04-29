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
  
Erweitert eine reduzierte Tabellen Kategorie und fügt der Tabellenansicht die Überschriftenzeilen des Blatts oder der unteren Ebene hinzu, die der Kategorie angehören.
  
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
  
> in Die Anzahl der Bytes in der PR_INSTANCE_KEY-Eigenschaft, auf die durch den _pbInstanceKey_ -Parameter verwiesen wird. 
    
 _pbInstanceKey_
  
> in Ein Zeiger auf die **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md))-Eigenschaft, die die Überschriftenzeile für die Kategorie identifiziert. 
    
 _ulRowCount_
  
> in Die maximale Anzahl von Zeilen, die im _lppRows_ -Parameter zurückgegeben werden. 
    
 _ulFlags_
  
> Reserviert muss NULL sein.
    
 _lppRows_
  
> Out Ein Zeiger auf eine [SRowSet](srowset.md) -Struktur, die die ersten Zeilen (bis zu _ulRowCount_) empfängt, die als Ergebnis der Erweiterung in die Tabellenansicht eingefügt wurden. Diese Zeilen werden nach der Überschriftenzeile eingefügt, die durch den _pbInstanceKey_ -Parameter identifiziert wird. Der _lppRows_ -Parameter kann NULL sein, wenn der _ulRowCount_ -Parameter NULL ist. 
    
 _lpulMoreRows_
  
> Out Ein Zeiger auf die Gesamtanzahl der Zeilen, die der Tabellenansicht hinzugefügt wurden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Kategorie wurde erfolgreich erweitert.
    
MAPI_E_NOT_FOUND 
  
> Die durch den _pbInstanceKey_ -Parameter angegebene Zeile ist nicht vorhanden. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: ExpandRow** -Methode erweitert eine reduzierte Tabellen Kategorie, indem Sie die Überschriftenzeilen Blatt oder auf niedrigerer Ebene, die der Kategorie angehören, der Tabellenansicht hinzugefügt wird. Ein Grenzwert für die Anzahl der Zeilen, die im _lppRows_ -Parameter zurückgegeben werden können, kann im Parameter _ulRowCount_ angegeben werden. Wenn _ulRowCount_ auf einen Wert größer als 0 (null) festgelegt ist und mindestens eine Zeile in der Zeilengruppe zurückgegeben wird, auf die von _lppRows_verwiesen wird, wird die Position der Textmarke BOOKMARK_CURRENT in die Zeile verschoben, die unmittelbar auf die letzte Zeile im Zeilensatz folgt.
  
Wenn _ulRowCount_ auf 0 (null) festgelegt ist, die die Kategorie mit NULL-oder untergeordneten Überschriftenzeilen hinzugefügt werden, oder null Zeilen zurückgegeben werden, da keine Überschriftenzeilen Blatt oder unterer Ebene in der Kategorie vorhanden sind, wird die Position von BOOKMARK_CURRENT auf die Zeile festgelegt. nach der durch _pbInstanceKey_identifizierten Zeile. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Generieren Sie keine Benachrichtigungen für Zeilen, die aufgrund der Kategorien Erweiterung zu einer Tabellenansicht hinzugefügt werden.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die Anzahl der Zeilen im Zeilensatz, auf die durch den _lppRows_ -Parameter verwiesen wird, entspricht möglicherweise nicht der Anzahl der Zeilen, die der Tabelle tatsächlich hinzugefügt wurden, dem gesamten Satz von Überschriftenzeilen der Blatt-oder unteren Ebene für die Kategorie. Fehler können auftreten, beispielsweise unzureichender Arbeitsspeicher, oder die Anzahl der Zeilen in der Kategorie, die die im _ulRowCount_ -Parameter angegebene Anzahl überschreitet. In beiden Fällen wird BOOKMARK_CURRENT in der letzten zurückgegebenen Zeile positioniert. Wenn Sie die restlichen Zeilen in der Kategorie sofort abrufen möchten, rufen Sie [IMAPITable:: QueryRows](imapitable-queryrows.md)auf.
  
Erwarten Sie nicht, eine Tabellenbenachrichtigung zu erhalten, wenn eine Kategorie ihren Status ändert. Sie können einen lokalen Cache mit Zeilen verwalten, die mit jedem **ExpandRow** -oder **CollapseRow** -Aufruf aktualisiert werden können. 
  
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und kategorisieren](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI verwendet die **IMAPITable:: ExpandRow** -Methode, um eine reduzierte Tabellen Kategorie zu erweitern.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

