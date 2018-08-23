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
ms.openlocfilehash: 46d993060d03b8c22c2d6c083c05f023648e6642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589665"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt die Daten, die benötigt werden, um die aktuelle neu erstellen erweitert oder reduziert Zustand einer kategorisierten Tabelle.
  
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
  
> Reserviert. NULL muss sein.
    
 _cbInstanceKey_
  
> [in] Durch den Parameter _LpbInstanceKey_ auf zeigt die Anzahl der Bytes im Instanzschlüssel. 
    
 _lpbInstanceKey_
  
> [in] Ein Zeiger auf die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaft der Zeile mit der aktuellen reduziert oder erweitert Zustand sollte neu erstellt werden. Der Parameter _LpbInstanceKey_ darf nicht NULL sein. 
    
 _lpcbCollapseState_
  
> [out] Ein Zeiger auf die Anzahl der Strukturen auf den durch den Parameter _LppbCollapseState_ verwiesen. 
    
 _lppbCollapseState_
  
> [out] Ein Zeiger auf einen Zeiger auf Strukturen, die Daten enthalten, die die aktuelle Tabellenansicht beschreibt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Status für die kategorisierten Tabelle wurde erfolgreich gespeichert.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt, die verhindert, den Vorgang gestartet wird dass. Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle unterstützt keine Kategorisierung und erweiterte und reduzierte Ansichten.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPITable::GetCollapseState** -Methode funktioniert mit der [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) -Methode zum Ändern des Benutzers Ansicht einer kategorisierten Tabelle. **GetCollapseState** speichert die Daten, die für **SetCollapseState** zu verwenden, um die entsprechenden Ansichten der Kategorien von einer kategorisierten Tabelle neu erstellen erforderlich ist. Dienstanbieter bestimmen die Daten gespeichert werden soll. Die meisten Dienstanbieter implementieren **GetCollapseState** speichern jedoch die folgenden: 
  
- Die Sortierschlüssel (standard und Spalten Kategorie).
    
- Informationen über die Zeile, die den Instanzschlüssel darstellt.
    
- Informationen zum Wiederherstellen der reduzierten und erweiterten Kategorien der Tabelle.
    
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md).
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Speichern Sie den aktuellen Status aller Knoten in einer Tabelle in der _LppbCollapseState_ -Parameter. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie immer **GetCollapseState** , bevor Sie **SetCollapseState**aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

