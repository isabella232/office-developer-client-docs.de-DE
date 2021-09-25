---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 856b1f1ee17d776f5d1dfab1c87937fbd8f378f6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575771"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die aktuelle Tabellenzeilenposition des Cursors basierend auf einem Bruchwert ab.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Parameter

 _lpulRow_
  
> [out] Zeiger auf die Nummer der aktuellen Zeile. Die Zeilennummer ist nullbasiert; Die erste Zeile in der Tabelle ist Null. 
    
 _lpulNumerator_
  
> [out] Zeiger auf den Zähler für den Bruch, der die Tabellenposition identifiziert.
    
 _lpulDenominator_
  
> [out] Zeiger auf den Nenner für den Bruch, der die Tabellenposition identifiziert. Der  _lpulDenominator-Parameter_ darf nicht Null sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Methode hat gültige Werte in  _lpulRow_,  _lpulNumerator_ und  _lpulDenominator_ zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPITable::QueryPosition-Methode** bestimmt die aktuelle Zeilenposition und gibt sowohl die Nummer der aktuellen Zeile als auch einen Bruchwert zurück, der die relative Position bis zum Ende der Tabelle angibt. MAPI definiert die aktuelle Zeile als nächste zu lesende Zeile. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen nicht die genaue Anzahl der Zeilen in der Tabelle für den  _Parameter lpulDenominator_ zurückgeben. dies kann eine Näherung sein. 
  
Wenn Sie die aktuelle Zeile nicht ermitteln können, geben Sie den Wert 0xFFFFFFFF in  _lpulRow_ zurück.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **QueryPosition** verwenden, um ein Bildlauffeld in einer Bildlaufleiste zu positionieren. Wenn **QueryPosition** beispielsweise in einer Tabelle mit 100 Zeilen den Wert 75 im  _Parameter "lpulNumerator",_ "100" im  _Parameter "lpulDenominator"_ und "75" im  _Parameter "lpulRow"_ zurückgibt, können Sie das Bildlauffeld 3/4 der Strecke über die Bildlaufleiste positionieren. 
  
Verlassen Sie sich nicht darauf, dass der Wert im  _LpulDenominator_ die Anzahl der Zeilen in der Tabelle ist. **QueryPosition** kann nicht immer die genaue Zeile identifizieren, in der sich der Cursor befindet. 
  
Ein Aufruf von **QueryPosition** kann große Mengen an Arbeitsspeicher umfassen, insbesondere für große kategorisierte Tabellen. Wenn der  _lpulRow-Parameter_ auf 0xFFFFFFFF festgelegt ist, war zu viel Arbeitsspeicher erforderlich, damit **QueryPosition** die aktuelle Zeile ermitteln kann. Rufen Sie die [IMAPITable::SeekRowApprox-Methode](imapitable-seekrowapprox.md) auf, um die Tabelle in der Zeile zu positionieren, die durch die Parameter  _lpulNumerator_ und  _lpulDenominator_ identifiziert wird. Gehen Sie jedoch nicht immer davon aus, dass **SeekRowApprox** die aktuelle Position festlegt, die dieselbe Zeile **queryPosition** hätte, wenn der Speicher kein Faktor wäre. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

