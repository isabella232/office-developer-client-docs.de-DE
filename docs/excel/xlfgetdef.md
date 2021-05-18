---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 014db553156849d84bd07e0e416f8cb3fefb4e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421998"
---
# <a name="xlfgetdef"></a>xlfGetDef

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt den Namen als Text zurück, der für einen bestimmten Bereich, Wert oder eine Formel in einer Arbeitsmappe definiert ist. In Excel wird dieser Wert in der Spalte **Name** des **Dialogfelds** **Name Manager** angezeigt, das angezeigt  wird, wenn Sie im Abschnitt Definierte Namen auf der Registerkarte Formeln auf **Name Manager** klicken. Verwenden **Sie xlfGetDef,** um den Namen zu erhalten, der einer Definition entspricht. Verwenden Sie [xlfGetName,](xlfgetname.md)um die Definition eines Namens zu erhalten.
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Parameter

_pxDefText_ (**xltypeStr**)
  
Dies kann alles sein, auf das Sie einen Namen definieren können, einschließlich eines Verweises, eines Werts, eines Objekts oder einer Formel.
  
Verweise müssen in der R1C1-Formatvorlage angegeben werden, z.  `"R3C5"` B. . Wenn  _pxDefText_ ein Wert oder eine Formel ist, muss das Gleichheitszeichen, das in der Spalte **Verweist** auf im Dialogfeld **Name Manager** angezeigt wird, nicht hinzugefügt werden. Wenn mehr als ein Name für  _pxDefText_ vorkommt, gibt **xlfGetDef** den Vornamen zurück. Wenn kein Name  _mit pxDefText entspricht,_ **gibt xlfGetDef den**  `#NAME?` Fehlerwert zurück. 
  
_pxDocumentText_ (**xltypeStr**)
  
Gibt das Blatt an, auf  _dem sich pxDefText_ befindet. Wenn  _pxDocumentText_ nicht angegeben wird, wird davon ausgegangen, dass es sich um das aktive Blatt handelt. 
  
_pxTypeNum_ (**xltypeNum**)
  
Eine Zahl von 1 bis 3, mit der angegeben wird, welche Namentypen zurückgegeben werden.
  
|**_pxTypeNum_**|**gibt zurück**|
|:-----|:-----|
|1 (oder Auslassung)  <br/> |Nur normale Namen.  <br/> |
|2  <br/> |Nur ausgeblendete Namen.  <br/> |
|3  <br/> |Alle Namen.  <br/> |
   
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

 _pxRes_ (**xltypeStr** oder **xltypeErr**)
  
Gibt den Namen zurück, der der angegebenen Definition zugeordnet ist.
  
## <a name="remarks"></a>Hinweise

In der folgenden Tabelle sind vier Beispiele für die Werte aufgeführt, die von einem Aufruf von **xlfGetDef** mit den angegebenen Argumenten zurückgegeben werden. 
  
|**Name, der in Excel**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|:-----|:-----|
|Der angegebene Bereich in Sheet4 heißt Sales.  <br/> |"R2C2:R9C6"  <br/> |"Sheet4"  <br/> |\<ausgelassen\>  <br/> |"Sales"  <br/> |
|Der Wert 100 in Sheet4 ist als Konstante definiert.  <br/> |"100"  <br/> |"Sheet4"  <br/> |\<ausgelassen\>  <br/> |"Constant"  <br/> |
|Die angegebene Formel in Sheet4 heißt SumTotal.  <br/> |"SUM(R1C1:R10C1)"  <br/> |"Sheet4"  <br/> |\<ausgelassen\>  <br/> |"SumTotal"  <br/> |
|3 ist als ausgeblendeter Namenszähler auf dem aktiven Blatt definiert.  <br/> |"3"  <br/> |\<ausgelassen\>  <br/> |2  <br/> |"Counter"  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [xlfGetName](xlfgetname.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

