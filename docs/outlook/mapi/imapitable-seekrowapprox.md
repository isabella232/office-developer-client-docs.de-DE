---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 12b0c9b40c7ff06e9a3cf8e7929489f30434fa12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792486"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**Betrifft**: Outlook 
  
Verschiebt den Cursor an eine ungefähre Bruch Position in der Tabelle an. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Parameter

 _ulNumerator_
  
> [in] Zeiger auf die Zähler des Bruchs, die die Position der Tabelle darstellen. Wenn der Parameter _UlNumerator_ gleich NULL ist, wird der Cursor am Anfang der Tabelle ungeachtet des Werts Nenner positioniert. Wenn _UlNumerator_ gleich dem _UlDenominator_ -Parameter ist, wird der Cursor nach der letzten Tabellenzeile positioniert. 
    
 _ulDenominator_
  
> [in] Zeiger auf die als Nenner des Bruchs, die die Position der Tabelle darstellen. Der Parameter _UlDenominator_ darf nicht NULL sein. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Suchvorgang erfolgreich war.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt, die verhindert, die Zeile Suchvorgänge Vorgang dass gestartet wird. Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.
    
## <a name="remarks"></a>Bemerkungen

Die Cursorposition in einer Tabelle nach dem Aufruf **der SeekRowApprox** ist heuristisch den Bruch und möglicherweise nicht genau. Bestimmte Anbieter können beispielsweise eine Tabelle auf der Basis einer binären Struktur, implementieren, zeigen Sie in der Mitte der Tabelle als im oberen Bereich der Struktur aus Gründen der Systemleistung behandelt. Wenn die Struktur nicht ausgeglichen ist, klicken Sie dann in der Mitte Punkts verwendet genau durch die Tabelle in der Mitte möglicherweise nicht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **SeekRowApprox** , um die Daten für die Implementierung eines Scroll-Leiste bereitzustellen. Wenn der Benutzer die Bildlaufleiste Feld 2/3 nach unten die Bildlaufleiste positioniert, können Sie beispielsweise diese Aktion modellieren, durch Aufrufen von **SeekRowApprox** und einen entsprechenden Bruch Wert mithilfe von _UlNumerator_ und _UlDenominator_übergeben. Die **SeekRowApprox** Suche ist immer absolute vom Beginn der Tabelle. Um am Ende der Tabelle zu verschieben, müssen die Werte in _UlNumerator_ und _UlDenominator_ identisch sein. 
  
Verwenden Sie aufbauen Nummerierungsschema geeignet ist. Um eine Position in der Mitte durch die Tabelle gesucht, können Sie d. h., 1/2, 10/20 oder 50/100 angeben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable : IUnknown](imapitableiunknown.md)

