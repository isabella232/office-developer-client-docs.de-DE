---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c3c66b9e54f0776a8afd6b4638d36dec3393dda8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792464"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**Betrifft**: Outlook 
  
Ruft die aktuelle Tabelle Zeilenposition des Cursors, basierend auf einem Bruch Wert.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Parameter

 _lpulRow_
  
> [out] Zeiger auf die Anzahl der aktuellen Zeile. Die Zeilennummer ist nullbasiert. die erste Zeile in der Tabelle ist 0 (null). 
    
 _lpulNumerator_
  
> [out] Zeiger auf die Zähler für den Bruch, die die Position der Tabelle identifiziert.
    
 _lpulDenominator_
  
> [out] Zeiger auf die als Nenner für den Bruch, die die Position der Tabelle identifiziert. Der Parameter _LpulDenominator_ darf nicht NULL sein. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Methode, die gültige Werte in _LpulRow_, _LpulNumerator_und _LpulDenominator_zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::QueryPosition** -Methode die aktuelle Zeilenposition bestimmt und sowohl die Anzahl der aktuellen Zeile und eine anteilige Wert, der angibt, der der relativen Position am Ende der Tabelle zurückgegeben. MAPI definiert die aktuelle Zeile als die nächste Zeile gelesen werden sollen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen nicht die genaue Anzahl der Zeilen in der Tabelle für den Parameter _LpulDenominator_ zurückgegeben. Es kann eine Annäherung sein. 
  
Wenn Sie die aktuelle Zeile nicht ermitteln können, einen Wert 0xFFFFFFFF in _LpulRow_zurück.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

**QueryPosition** können Sie um das Bildlauffeld in einer Bildlaufleiste zu positionieren. Beispielsweise in einer Tabelle mit 100 Zeilen **QueryPosition** in den _LpulNumerator_ -Parameter im Parameter _LpulDenominator_ 100 und 75 in den _LpulRow_ -Parameter einen Wert von 75 zurück können Sie die Scroll Feld 3/4 der positionieren die Möglichkeit, über die Bildlaufleiste. 
  
Verlassen Sie sich nicht auf dem Wert im _LpulDenominator_ wird die Anzahl der Zeilen in der Tabelle. **QueryPosition** kann nicht immer die genaue Zeile identifizieren, der auf dem sich der Cursor befindet. 
  
Ein Aufruf von **QueryPosition** möglicherweise große Mengen von Arbeitsspeicher, besonders für große kategorisierten Tabellen umfassen. Wenn der Parameter _LpulRow_ auf 0xFFFFFFFF festgelegt ist, wurde zu viel Speicher für **QueryPosition** zum Bestimmen der aktuellen Zeile erforderlich. Rufen Sie die [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) -Methode, um die position der Tabelle auf die Zeile, die durch die Parameter _LpulNumerator_ und _LpulDenominator_ identifiziert. Jedoch immer erwarten Sie keine **SeekRowApprox** , wie die aktuelle Position die gleiche Zeile herzustellen, die Wenn Speicher keinen Faktor hätte **QueryPosition** hätten. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)

