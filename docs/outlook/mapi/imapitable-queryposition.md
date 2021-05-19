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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415663"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die aktuelle Tabellenzeile des Cursors basierend auf einem Bruchwert ab.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Parameter

 _lpulRow_
  
> [out] Zeiger auf die Nummer der aktuellen Zeile. Die Zeilennummer ist nullbasierter Wert. Die erste Zeile in der Tabelle ist Null. 
    
 _lpulNumerator_
  
> [out] Zeiger auf den Zähler für den Bruch, der die Tabellenposition identifiziert.
    
 _lpulDenominator_
  
> [out] Zeiger auf den Nenner für den Bruch, der die Tabellenposition identifiziert. Der  _lpulDenominator-Parameter_ darf nicht null sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Methode hat gültige Werte in _lpulRow,_ _lpulNumerator_ und _lpulDenominator zurückgegeben._
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::QueryPosition-Methode** bestimmt die aktuelle Zeilenposition und gibt sowohl die Nummer der aktuellen Zeile als auch einen Bruchwert zurück, der die relative Position am Ende der Tabelle angibt. MAPI definiert die aktuelle Zeile als die nächste zu lesende Zeile. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen nicht die genaue Anzahl der Zeilen in der Tabelle für den  _lpulDenominator-Parameter zurückgeben._ Dies kann eine Näherung sein. 
  
Wenn Sie die aktuelle Zeile nicht ermitteln können, geben Sie den Wert 0xFFFFFFFF in _lpulRow zurück._
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **QueryPosition verwenden,** um ein Bildlauffeld in einer Bildlaufleiste zu positionieren. Wenn **QueryPosition** beispielsweise in einer Tabelle mit 100 Zeilen den Wert 75 im  _lpulNumerator-Parameter,_ 100 im  _lpulDenominator-Parameter_ und 75 im  _lpulRow-Parameter_ zurückgibt, können Sie das Bildlauffeld 3/4 des Wegs über die Bildlaufleiste positionieren. 
  
Verlassen Sie sich nicht darauf, dass der Wert in  _lpulDenominator_ die Anzahl der Zeilen in der Tabelle ist. **QueryPosition** kann nicht immer die genaue Zeile identifizieren, in der der Cursor positioniert ist. 
  
Ein Aufruf von **QueryPosition** kann große Mengen an Arbeitsspeicher umfassen, insbesondere für große kategorisierte Tabellen. Wenn der  _lpulRow-Parameter_ auf 0xFFFFFFFF festgelegt ist, war zu viel Arbeitsspeicher für **QueryPosition** erforderlich, um die aktuelle Zeile zu bestimmen. Rufen Sie [die IMAPITable::SeekRowApprox-Methode](imapitable-seekrowapprox.md) auf, um die Tabelle in der Zeile zu positionieren, die durch die  _Parameter lpulNumerator_ und  _lpulDenominator identifiziert_ wird. Gehen Sie jedoch nicht immer davon aus, dass **SeekRowApprox** als aktuelle Position dieselbe Zeile wie **QueryPosition** festlegen würde, wenn der Arbeitsspeicher kein Faktor gewesen wäre. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

