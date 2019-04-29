---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 97575a65cd6825e07d6f11c813beec539f99f53a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436076"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Daten zurück, die erforderlich sind, um den aktuellen reduzierten oder erweiterten Status einer kategorisierten Tabelle neu zu erstellen.
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert muss NULL sein.
    
 _cbInstanceKey_
  
> in Die Anzahl der Bytes im Instanzschlüssel, auf die durch den _lpbInstanceKey_ -Parameter verwiesen wird. 
    
 _lpbInstanceKey_
  
> in Ein Zeiger auf die **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md))-Eigenschaft der Zeile, in der der aktuelle reduzierte oder erweiterte Zustand neu erstellt werden soll. Der _lpbInstanceKey_ -Parameter darf nicht NULL sein. 
    
 _lpcbCollapseState_
  
> Out Ein Zeiger auf die Anzahl der Strukturen, auf die durch den _lppbCollapseState_ -Parameter verwiesen wird. 
    
 _lppbCollapseState_
  
> Out Ein Zeiger auf einen Zeiger auf Strukturen, die Daten enthalten, die die aktuelle Tabellenansicht beschreiben.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status der kategorisierten Tabelle wurde erfolgreich gespeichert.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Vorgang gestartet wird. Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle unterstützt keine Kategorisierung und erweiterte und reduzierte Ansichten.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: GetCollapseState** -Methode kann mit der [IMAPITable:: SetCollapseState](imapitable-setcollapsestate.md) -Methode verwendet werden, um die Benutzeransicht einer kategorisierten Tabelle zu ändern. **GetCollapseState** speichert die Daten, die **SetCollapseState** benötigen, um die entsprechenden Ansichten der Kategorien einer kategorisierten Tabelle neu zu erstellen. Dienstanbieter bestimmen die zu speichernden Daten. Die meisten Dienstanbieter, die **GetCollapseState** implementieren, speichern jedoch Folgendes: 
  
- Die Sortierschlüssel (Standardspalten und Kategorien Spalten).
    
- Informationen zu der Zeile, die der Instanzschlüssel darstellt.
    
- Informationen zum Wiederherstellen der reduzierten und erweiterten Kategorien der Tabelle.
    
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und kategorisieren](sorting-and-categorization.md).
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Speichert den aktuellen Status aller Knoten einer Tabelle im _lppbCollapseState_ -Parameter. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **GetCollapseState** immer auf, bevor Sie **SetCollapseState**aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

