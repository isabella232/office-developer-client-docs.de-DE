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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1b3d8c74d85696e733b378a4cac2b8e2a3b6a072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792446"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**Betrifft**: Outlook 
  
Erweitert eine reduzierte Tabellenkategorie, Hinzufügen von Endknoten oder auf niedrigerer Ebene Überschriftenzeilen der Kategorie auf die Tabellenansicht.
  
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
  
> [in] Die Anzahl der Bytes in der PR_INSTANCE_KEY-Eigenschaft auf den durch den Parameter _PbInstanceKey_ verwiesen. 
    
 _pbInstanceKey_
  
> [in] Ein Zeiger auf die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaft, die Zeile mit der Spaltenüberschrift für die Kategorie identifiziert. 
    
 _ulRowCount_
  
> [in] Die maximale Anzahl der Zeilen, die im Parameter _LppRows_ zurückzugeben. 
    
 _ulFlags_
  
> Reserviert. NULL muss sein.
    
 _lppRows_
  
> [out] Ein Zeiger auf eine [SRowSet](srowset.md) -Struktur empfangen die ersten (bis zum _UlRowCount_) Zeilen, die in der Tabellenansicht als Ergebnis der Erweiterung eingefügt wurden. Diese Zeilen werden nach der Zeile mit der Spaltenüberschrift identifiziert durch den Parameter _PbInstanceKey_ eingefügt. Wenn der Parameter _UlRowCount_ gleich NULL ist, kann der Parameter _LppRows_ NULL sein. 
    
 _lpulMoreRows_
  
> [out] Ein Zeiger auf die Gesamtzahl der Zeilen, die die Tabellenansicht hinzugefügt wurden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Kategorie wurde erfolgreich erweitert.
    
MAPI_E_NOT_FOUND 
  
> Die Zeile, die vom _PbInstanceKey_ -Parameter ist nicht vorhanden. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::ExpandRow** -Methode erweitert eine reduzierte Tabellenkategorie, Hinzufügen von Endknoten oder auf niedrigerer Ebene Überschriftenzeilen, die die Tabelle-Ansicht der Kategorie angehören. Beschränkt die Anzahl der Zeilen im _LppRows_ -Parameter zurückgegeben werden soll, kann in der _UlRowCount_ -Parameter angegeben werden. Wenn _UlRowCount_ auf einen Wert größer als 0 (null) festgelegt wird, und eine oder mehrere Zeilen in der Zeile auf den _LppRows_zurückgegeben werden, legen Sie die Position der Textmarke, die bookmark_current in die Zeile unmittelbar nach der letzten Zeile in der Zeile verschoben wird.
  
Wenn _UlRowCount_ auf NULL festgelegt ist, für die Kategorie hinzugefügt werden, die Endknoten NULL oder auf niedrigerer Ebene Überschriftenzeilen anfordern oder keine Zeilen zurückgegeben werden, da keine Endknoten oder auf niedrigerer Ebene Überschriftenzeilen in der Kategorie vorhanden sind, wird die Position des BOOKMARK_CURRENT in die Zeile festgelegt. nach der Zeile, die durch _PbInstanceKey_identifiziert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Generieren Sie keine Benachrichtigungen auf Zeilen, die aufgrund der Kategorie die Erweiterung einer Tabellenansicht hinzugefügt werden.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die Anzahl der Zeilen in der Zeile durch den Parameter _LppRows_ auf zeigt möglicherweise nicht gleich der Anzahl der Zeilen, die tatsächlich zur Tabelle hinzugefügt wurden, die gesamte Satz von Endknoten oder auf niedrigerer Ebene Überschriftenzeilen für die Kategorie. Fehler können auftreten, wie nicht genügend Arbeitsspeicher oder die Anzahl der Zeilen in der Kategorie überschreiten im _UlRowCount_ -Parameter angegebene Nummer getestet werden. In beiden Fällen wird in der letzten Zeile zurückgegeben BOOKMARK_CURRENT positioniert. Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md), um den Rest der Zeilen in der Kategorie sofort abzurufen.
  
Davon ausgehen, dass eine Tabelle Benachrichtigung zu erhalten, wenn eine Kategorie den Zustand wechselt. Sie können einen lokalen Cache der Zeilen verwalten, die bei jedem Anruf **ExpandRow** oder **CollapseRow** aktualisiert werden können. 
  
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoExpandCollapse  <br/> |MFCMAPI (engl.) wird die **IMAPITable::ExpandRow** -Methode verwendet, um eine reduzierte Tabellenkategorie zu erweitern.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

