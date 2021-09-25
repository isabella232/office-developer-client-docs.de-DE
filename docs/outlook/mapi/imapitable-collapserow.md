---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6f8d1319f5655591bdd11188910e2ac458b4dcfc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584353"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Reduziert eine erweiterte Tabellenkategorie, wobei überschriften und Blattzeilen auf niedrigerer Ebene, die zur Kategorie gehören, aus der Tabellenansicht entfernt werden.
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a>Parameter

 _cbInstanceKey_
  
> [in] Die Anzahl der Bytes in der PR_INSTANCE_KEY-Eigenschaft, auf die der  _PbInstanceKey-Parameter_ verweist. 
    
 _pbInstanceKey_
  
> [in] Ein Zeiger auf die **eigenschaft PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), die die Überschriftenzeile für die Kategorie identifiziert. 
    
 _ulFlags_
  
> Reserviert; muss Null sein.
    
 _lpulRowCount_
  
> [out] Ein Zeiger auf die Gesamtzahl der Zeilen, die aus der Tabellenansicht entfernt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Reduzieren-Vorgang wurde erfolgreich ausgeführt.
    
MAPI_E_NOT_FOUND 
  
> Die vom  _PbInstanceKey-Parameter_ identifizierte Zeile ist nicht vorhanden. 
    
MAPI_E_INVALID_ENTRYID 
  
> Die vom  _PbInstanceKey-Parameter_ identifizierte Zeile ist nicht vorhanden. Dieser Fehler ist eine Alternative zu MAPI_E_NOT_FOUND; Dienstanbieter können beide zurückgeben. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPITable::CollapseRow-Methode** reduziert eine Tabellenkategorie und entfernt sie aus der Tabellenansicht. Die Zeilen werden beginnend mit der Zeile reduziert, die durch die **PR_INSTANCE_KEY** Eigenschaft identifiziert wird, auf die durch den  _PbInstanceKey-Parameter_ verwiesen wird. Die Anzahl der Zeilen, die aus der Ansicht entfernt werden, wird im Inhalt des  _lpulRowCount-Parameters_ zurückgegeben. 
  
Benachrichtigungen werden nie für Tabellenzeilen generiert, die aufgrund eines Reduzierens aus einer Ansicht entfernt werden. 
  
Wenn eine Zeile, die durch eine Textmarke definiert ist, aus der Ansicht reduziert wird, wird die Textmarke so verschoben, dass sie auf die nächste sichtbare Zeile zeigt. 
  
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und Kategorisieren.](sorting-and-categorization.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI verwendet die **IMAPITable::CollapseRow-Methode,** um eine Tabellenkategorie zu reduzieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

