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
  
Ruft die aktuelle Tabellenzeilen Position des Cursors basierend auf einem Dezimalwert ab.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Parameter

 _lpulRow_
  
> Out Zeiger auf die Nummer der aktuellen Zeile. Die Zeilennummer ist nullbasiert; die erste Zeile in der Tabelle ist NULL. 
    
 _lpulNumerator_
  
> Out Zeiger auf den Zähler für den Bruch, der die Tabellenposition angibt.
    
 _lpulDenominator_
  
> Out Zeiger auf den Nenner für den Bruch, der die Tabellenposition angibt. Der Parameter _lpulDenominator_ darf nicht NULL sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Methode hat gültige Werte in _lpulRow_, _lpulNumerator_und _lpulDenominator_zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: QueryPosition** -Methode bestimmt die aktuelle Zeilenposition und gibt sowohl die Nummer der aktuellen Zeile als auch einen Bruch Wert zurück, der die relative Position am Ende der Tabelle angibt. MAPI definiert die aktuelle Zeile als die nächste Zeile, die gelesen werden soll. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen nicht die genaue Anzahl der Zeilen in der Tabelle für den _lpulDenominator_ -Parameter zurückgeben. Es kann eine Näherung sein. 
  
Wenn die aktuelle Zeile nicht bestimmt werden kann, geben Sie den Wert 0xFFFFFFFF in _lpulRow_zurück.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **QueryPosition** verwenden, um ein Bildlauffeld in einer Bildlaufleiste zu positionieren. Wenn **QueryPosition** beispielsweise in einer tabelle mit 100 Zeilen einen wert von 75 im _lpulNumerator_ -Parameter, 100 im _lpulDenominator_ -Parameter und 75 im _lpulRow_ -Parameter zurückgibt, können Sie das Bildlauffeld 3/4 von die quer über die Bildlaufleiste. 
  
Verlassen Sie sich nicht auf den Wert in _lpulDenominator_ , der die Anzahl der Zeilen in der Tabelle ist. **QueryPosition** kann nicht immer die genaue Zeile identifizieren, auf der sich der Cursor befindet. 
  
Ein Aufruf von **QueryPosition** kann große Mengen an Arbeitsspeicher erfordern, insbesondere für große kategorisierte Tabellen. Wenn der _lpulRow_ -Parameter auf 0xFFFFFFFF festgelegt ist, wurde zu viel Arbeitsspeicher benötigt, damit **QueryPosition** die aktuelle Zeile ermitteln kann. Rufen Sie die [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) -Methode auf, um die Tabelle in der durch die Parameter _lpulNumerator_ und _lpulDenominator_ angegebenen Zeile zu positionieren. Erwarten Sie jedoch nicht immer, dass **SeekRowApprox** als aktuelle Position die gleiche Zeile **QueryPosition** hätte, wenn der Arbeitsspeicher kein Faktor gewesen wäre. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

