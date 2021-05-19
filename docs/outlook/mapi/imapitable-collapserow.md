---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416174"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Reduziert eine erweiterte Tabellenkategorie, indem alle Überschriften auf niedrigerer Ebene und Blattzeilen, die zu der Kategorie gehören, aus der Tabellenansicht entfernt werden.
  
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
  
> [in] Die Anzahl der Bytes in der PR_INSTANCE_KEY, auf die der  _pbInstanceKey-Parameter_ verweist. 
    
 _pbInstanceKey_
  
> [in] Ein Zeiger auf die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaft, die die Überschriftenzeile für die Kategorie identifiziert. 
    
 _ulFlags_
  
> Reserviert; muss null sein.
    
 _lpulRowCount_
  
> [out] Ein Zeiger auf die Gesamtanzahl der Zeilen, die aus der Tabellenansicht entfernt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Collapse-Vorgang ist erfolgreich.
    
MAPI_E_NOT_FOUND 
  
> Die vom  _pbInstanceKey-Parameter_ identifizierte Zeile ist nicht vorhanden. 
    
MAPI_E_INVALID_ENTRYID 
  
> Die vom  _pbInstanceKey-Parameter_ identifizierte Zeile ist nicht vorhanden. Dieser Fehler ist eine Alternative zu MAPI_E_NOT_FOUND. Dienstanbieter können eine der beiden Zurückgeben. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::CollapseRow-Methode** reduziert eine Tabellenkategorie und entfernt sie aus der Tabellenansicht. Die Zeilen werden beginnend mit der Zeile reduziert, die von der **PR_INSTANCE_KEY-Eigenschaft** identifiziert wird, auf die der  _pbInstanceKey-Parameter_ verweist. Die Anzahl der Zeilen, die aus der Ansicht entfernt werden, wird im Inhalt des  _lpulRowCount-Parameters_ zurückgegeben. 
  
Benachrichtigungen werden niemals für Tabellenzeilen generiert, die als Ergebnis eines Reduzierens aus einer Ansicht entfernt werden. 
  
Wenn eine zeile, die durch eine Textmarke definiert ist, aus der Sicht reduziert wird, wird die Textmarke verschoben, um auf die nächste sichtbare Zeile zu zeigen. 
  
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sorting and Categorization](sorting-and-categorization.md).
  
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

