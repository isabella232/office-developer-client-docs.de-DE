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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328963"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Reduziert eine erweiterte Tabellen Kategorie, wobei alle untergeordneten Überschriften und Blattzeilen, die der Kategorie angehören, aus der Tabellenansicht entfernt werden.
  
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
  
> in Die Anzahl der Bytes in der PR_INSTANCE_KEY-Eigenschaft, auf die durch den _pbInstanceKey_ -Parameter verwiesen wird. 
    
 _pbInstanceKey_
  
> in Ein Zeiger auf die **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md))-Eigenschaft, die die Überschriftenzeile für die Kategorie identifiziert. 
    
 _ulFlags_
  
> Reserviert muss NULL sein.
    
 _lpulRowCount_
  
> Out Ein Zeiger auf die Gesamtanzahl der Zeilen, die aus der Tabellenansicht entfernt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Collapse-Vorgang wurde erfolgreich ausgeführt.
    
MAPI_E_NOT_FOUND 
  
> Die durch den _pbInstanceKey_ -Parameter angegebene Zeile ist nicht vorhanden. 
    
MAPI_E_INVALID_ENTRYID 
  
> Die durch den _pbInstanceKey_ -Parameter angegebene Zeile ist nicht vorhanden. Dieser Fehler ist eine Alternative zu MAPI_E_NOT_FOUND; Dienstanbieter können eine der beiden zurückgeben. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: CollapseRow** -Methode reduziert eine Tabellen Kategorie und entfernt Sie aus der Tabellenansicht. Die Zeilen werden beginnend bei der Zeile reduziert, die von der **PR_INSTANCE_KEY** -Eigenschaft identifiziert wird, auf die durch den _pbInstanceKey_ -Parameter verwiesen wird. Die Anzahl der Zeilen, die aus der Ansicht entfernt werden, wird im Inhalt des _lpulRowCount_ -Parameters zurückgegeben. 
  
Benachrichtigungen werden nie für Tabellenzeilen generiert, die aus einer Ansicht als Ergebnis eines Collapse-Vorgangs entfernt werden. 
  
Wenn eine Zeile, die durch eine Textmarke definiert ist, ausgeblendet ist, wird die Textmarke so verschoben, dass Sie auf die nächste sichtbare Zeile zeigt. 
  
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und kategorisieren](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI verwendet die **IMAPITable:: CollapseRow** -Methode, um eine Tabellen Kategorie zu reduzieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

