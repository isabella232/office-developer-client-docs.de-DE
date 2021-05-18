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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bbb79097d03a8ea09cb4aff374231ee780e15395
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412149"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verschiebt den Cursor an eine ungefähre Bruchposition in der Tabelle. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Parameter

 _ulNumerator_
  
> [in] Zeiger auf den Zähler der Bruchzahl, die die Tabellenposition darstellt. Wenn der  _ulNumerator-Parameter_ null ist, wird der Cursor unabhängig vom Nennwert am Anfang der Tabelle positioniert. Wenn  _ulNumerator_ gleich dem  _ulDenominator-Parameter_ ist, wird der Cursor hinter der letzten Tabellenzeile positioniert. 
    
 _ulDenominator_
  
> [in] Zeiger auf den Nenner der Bruchzahl, die die Tabellenposition darstellt. Der  _ulDenominator-Parameter_ darf nicht null sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Suchvorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Zeilensuchenvorgang gestartet wird. Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.
    
## <a name="remarks"></a>Hinweise

Die Cursorposition in einer Tabelle nach einem Aufruf der **IMAPITable::SeekRowApprox-Methode** ist heuristisch der Bruch und möglicherweise nicht exakt. Beispielsweise können bestimmte Anbieter eine Tabelle über einer binären Struktur implementieren und den Tabellenhalbpunkt aus Leistungsgründen als oberster Punkt der Struktur behandeln. Wenn die Struktur nicht ausgeglichen ist, ist der verwendete Halbzeitpunkt möglicherweise nicht genau in der Mitte der Tabelle. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen **Sie SeekRowApprox** auf, um die Daten für eine Bildlaufleistenimplementierung zur Verfügung zu stellen. Wenn der Benutzer beispielsweise das Bildlauffeld 2/3 unten auf der Bildlaufleiste positioniert, können Sie diese Aktion modellieren, indem Sie **SeekRowApprox** aufrufen und einen entsprechenden Bruchwert mithilfe von _ulNumerator_ und _ulDenominator übergeben._ Die **SeekRowApprox-Suche** ist immer vom Anfang der Tabelle aus absolut. Um an das Ende der Tabelle zu wechseln, müssen die Werte in  _ulNumerator_ und  _ulDenominator_ identisch sein. 
  
Verwenden Sie das entsprechende Nummernschema. Das heißt, sie können 1/2, 10/20 oder 50/100 angeben, um eine Position in der Mitte der Tabelle zu finden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable : IUnknown](imapitableiunknown.md)

