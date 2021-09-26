---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 64a63e860f423b7de56bce277f778576c2ed44c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620835"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Daten zurück, die zum Neuerstellen des aktuellen reduzierten oder erweiterten Zustands einer kategorisierten Tabelle erforderlich sind.
  
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
  
> Reserviert; muss Null sein.
    
 _cbInstanceKey_
  
> [in] Die Anzahl der Bytes im Instanzschlüssel, auf die durch den  _Parameter lpbInstanceKey_ verwiesen wird. 
    
 _lpbInstanceKey_
  
> [in] Ein Zeiger auf die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaft der Zeile, in der der aktuelle reduzierte oder erweiterte Zustand neu erstellt werden soll. Der  _parameter lpbInstanceKey_ darf nicht NULL sein. 
    
 _lpcbCollapseState_
  
> [out] Ein Zeiger auf die Anzahl der Strukturen, auf die der  _lppbCollapseState-Parameter_ verweist. 
    
 _lppbCollapseState_
  
> [out] Ein Zeiger auf einen Zeiger auf Strukturen, die Daten enthalten, die die aktuelle Tabellenansicht beschreiben.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status für die kategorisierte Tabelle wurde erfolgreich gespeichert.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Vorgang gestartet wird. Entweder sollte der laufende Vorgang abgeschlossen werden können, oder er sollte beendet werden.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle unterstützt keine Kategorisierung sowie erweiterte und reduzierte Ansichten.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::GetCollapseState-Methode** kann mit der [IMAPITable::SetCollapseState-Methode](imapitable-setcollapsestate.md) verwendet werden, um die Ansicht des Benutzers einer kategorisierten Tabelle zu ändern. **GetCollapseState** speichert die Daten, die für **SetCollapseState** erforderlich sind, um die entsprechenden Ansichten der Kategorien einer kategorisierten Tabelle neu zu erstellen. Dienstanbieter bestimmen die zu speichernden Daten. Die meisten Dienstanbieter, die **GetCollapseState** implementieren, speichern jedoch Folgendes: 
  
- Die Sortierschlüssel (Standardspalten und Rubrikenspalten).
    
- Informationen zu der Zeile, die der Instanzschlüssel darstellt.
    
- Informationen zum Wiederherstellen der reduzierten und erweiterten Kategorien der Tabelle.
    
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und Kategorisieren.](sorting-and-categorization.md)
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Store den aktuellen Status aller Knoten einer Tabelle im _Parameter "lppbCollapseState"_ an. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie immer **GetCollapseState** auf, bevor Sie **SetCollapseState** aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

