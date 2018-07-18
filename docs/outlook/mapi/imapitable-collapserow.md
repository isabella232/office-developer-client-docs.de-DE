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
ms.openlocfilehash: 1fd711683ff476ef5d381bca2f9db6bc25b07c68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792456"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**Betrifft**: Outlook 
  
Blendet eine Tabellenkategorie für erweiterte, entfernen Sie die untergeordnete Überschriften und Endknoten Zeilen aus der Tabellenansicht für die Kategorie gehören.
  
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
  
> [in] Die Anzahl der Bytes in der PR_INSTANCE_KEY-Eigenschaft auf den durch den Parameter _PbInstanceKey_ verwiesen. 
    
 _pbInstanceKey_
  
> [in] Ein Zeiger auf die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaft, die Zeile mit der Spaltenüberschrift für die Kategorie identifiziert. 
    
 _ulFlags_
  
> Reserviert. NULL muss sein.
    
 _lpulRowCount_
  
> [out] Ein Zeiger auf die Gesamtzahl der Zeilen, die aus der Tabellenansicht entfernt werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Collapse-Vorgang wurde erfolgreich abgeschlossen.
    
MAPI_E_NOT_FOUND 
  
> Die Zeile, die vom _PbInstanceKey_ -Parameter ist nicht vorhanden. 
    
MAPI_E_INVALID_ENTRYID 
  
> Die Zeile, die vom _PbInstanceKey_ -Parameter ist nicht vorhanden. Dieser Fehler ist eine Alternative zur MAPI_E_NOT_FOUND. Dienstanbieter können entweder 1 zurück. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::CollapseRow** -Methode wird eine Tabellenkategorie reduziert und entfernt ihn aus der Tabellenansicht. Die Zeilen werden regelmäßig beginnend in der Zeile, die von der **PR_INSTANCE_KEY** -Eigenschaft auf das durch den Parameter _PbInstanceKey_ identifiziert. Die Anzahl der Zeilen, die aus der Ansicht entfernt wurden, wird in den Inhalt des Parameters _LpulRowCount_ zurückgegeben. 
  
Benachrichtigungen werden nie für Tabellenzeilen generiert, die als Ergebnis eines Vorgangs reduzieren aus einer Ansicht entfernt werden. 
  
Wenn eine Zeile, die durch eine Textmarke definiert wird aus der Ansicht reduziert ist, wird die Textmarke So zeigen Sie auf die nächste sichtbare Zeile verschoben. 
  
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoExpandCollapse  <br/> |MFCMAPI (engl.) verwendet die **IMAPITable::CollapseRow** -Methode, um eine Tabellenkategorie reduzieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

