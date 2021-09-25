---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b88e7d71639d880a001a48d60e6089e9358f807a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592312"
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
  
> [in] Zeiger auf den Zähler des Bruchs, der die Tabellenposition darstellt. Wenn der  _UlNumerator-Parameter_ Null ist, wird der Cursor unabhängig vom Nennerwert am Anfang der Tabelle positioniert. Wenn  _ulNumerator_ gleich dem  _ulDenominator-Parameter_ ist, wird der Cursor hinter der letzten Tabellenzeile positioniert. 
    
 _ulDenominator_
  
> [in] Zeiger auf den Nenner der Bruchzahl, die die Tabellenposition darstellt. Der  _ulDenominator-Parameter_ darf nicht null sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Suchvorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Vorgang für die Zeilensuche gestartet wird. Entweder sollte der laufende Vorgang abgeschlossen werden können, oder er sollte beendet werden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Cursorposition in einer Tabelle nach einem Aufruf der **IMAPITable::SeekRowApprox-Methode** ist heuristisch der Bruch und ist möglicherweise nicht genau. Beispielsweise können bestimmte Anbieter eine Tabelle über einer binären Struktur implementieren, wobei der halbe Punkt der Tabelle aus Leistungsgründen als oberer Rand der Struktur behandelt wird. Wenn die Struktur nicht ausgeglichen ist, ist der verwendete Halbe-Punkt möglicherweise nicht genau in der Mitte der Tabelle. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen **Sie SeekRowApprox** auf, um die Daten für eine Implementierung einer Bildlaufleiste bereitzustellen. Wenn der Benutzer beispielsweise das Bildlauffeld 2/3 nach unten auf der Bildlaufleiste positioniert, können Sie diese Aktion modellieren, indem Sie **SeekRowApprox** aufrufen und einen entsprechenden Bruchwert mit  _ulNumerator_ und  _ulDenominator_ übergeben. Die **SeekRowApprox-Suche** ist immer absolut am Anfang der Tabelle. Um an das Ende der Tabelle zu wechseln, müssen die Werte in  _ulNumerator_ und  _ulDenominator_ identisch sein. 
  
Verwenden Sie das richtige Zahlenschema. Um also eine Position in der Mitte der Tabelle zu suchen, können Sie 1/2, 10/20 oder 50/100 angeben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable : IUnknown](imapitableiunknown.md)

