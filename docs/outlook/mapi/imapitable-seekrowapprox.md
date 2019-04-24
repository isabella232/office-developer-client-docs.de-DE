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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328840"
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
  
> in Zeiger auf den Zähler des Bruchs, der die Tabellenposition darstellt. Wenn der _ulNumerator_ -Parameter 0 (null) ist, wird der Cursor unabhängig vom Wert des Nenners am Anfang der Tabelle positioniert. Wenn _ulNumerator_ dem Parameter _ulDenominator_ entspricht, wird der Cursor hinter der letzten Tabellenzeile positioniert. 
    
 _ulDenominator_
  
> in Zeiger auf den Nenner des Bruchs, der die Tabellenposition darstellt. Der Parameter _ulDenominator_ darf nicht NULL sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Seek-Vorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Es wird ein weiterer Vorgang ausgeführt, der verhindert, dass der Suchvorgang gestartet wird. Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.
    
## <a name="remarks"></a>Bemerkungen

Die Cursorposition in einer Tabelle nach einem Aufruf der **IMAPITable:: SeekRowApprox** -Methode ist heuristisch der Bruchteil und ist möglicherweise nicht genau. Beispielsweise können bestimmte Anbieter eine Tabelle über eine binäre Struktur implementieren, um aus Leistungsgründen die halbe Stelle der Tabelle als oberste der Struktur zu behandeln. Wenn die Struktur nicht ausgeglichen ist, ist die verwendete Hälfte möglicherweise nicht genau in der Mitte der Tabelle. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Aufrufen von **SeekRowApprox** , um die Daten für eine Bildlaufleisten Implementierung bereitzustellen. Wenn der Benutzer beispielsweise das Bildlauffeld 2/3 auf der Bildlaufleiste positioniert, können Sie diese Aktion modellieren, indem Sie **SeekRowApprox** aufrufen und einen äquivalenten Dezimalwert mit _ulNumerator_ und _ulDenominator_übergeben. Die **SeekRowApprox** -Suche ist immer vom Anfang der Tabelle aus absolut. Um zum Ende der Tabelle zu wechseln, müssen die Werte in _ulNumerator_ und _ulDenominator_ identisch sein. 
  
Verwenden Sie ein beliebiges Zahlen Schema. Das heißt, um nach einer Position in der Mitte der Tabelle zu suchen, können Sie 1/2, 10/20 oder 50/100 angeben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable : IUnknown](imapitableiunknown.md)

