---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- funktion [excel 2007],TempErr12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4b74bfaceab52cb1526ed8abba13e0476f73f0bf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572368"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Frameworkbibliotheksfunktion, die einen temporären **XLOPER** /  **XLOPER12** erstellt, der einen Microsoft Excel Arbeitsblattfehler enthält. 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>Parameter

 _err_
  
Der gewünschte Fehlercode oder dessen literale numerische Entsprechung, wie in der folgenden Tabelle dargestellt.
  
|**Error**|**In XLCALL definierter Fehlercode. H**|**Dezimalentsprechung**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |0  <br/> |
|#DIV/0!  <br/> |**xlerrDiv0** <br/> |7   <br/> |
|#VALUE!  <br/> |**xlerrValue** <br/> |15   <br/> |
|#REF!  <br/> |**xlerrRef** <br/> |23  <br/> |
|#NAME?  <br/> |**xlerrName** <br/> |29  <br/> |
|#NUM!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#N/A  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>Rückgabewert

Gibt einen **xltypeBool-Wert** zurück, der den übergebenen Fehlercode enthält. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempErr12-Funktion** verwendet, um einen #VALUE zurückzugeben. Excel. 
  
> [!NOTE]
> Die Framework-Bibliotheksfunktion **TempErr12** weist Speicher aus einem internen Puffer zu, der normalerweise freigegeben wird, wenn die Framework-Funktion **Excel12f** aufgerufen wird. Wenn diese Beispielfunktion wiederholt aufgerufen wird, ohne **Dass Excel12f** aufgerufen wird, tritt ein Speicherverlust auf. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

