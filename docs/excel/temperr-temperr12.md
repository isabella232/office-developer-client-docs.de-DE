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
- Temperr-Funktion [excel 2007], TempErr12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790566"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliothek-Funktion, die eine temporäre **XLOPER**erstellt/ **XLOPER12** mit einer Microsoft Excel-Arbeitsblatt-Fehler. 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>Parameter

 _Err_
  
Die gewünschte Fehlercode oder deren Literale numerische Entsprechung, wie in der folgenden Tabelle dargestellt.
  
|**Fehler**|**Fehlercode in XLCALL definiert. H**|**Dezimalzahl**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |0  <br/> |
|#DIV/0!  <br/> |**xlerrDiv0** <br/> |7  <br/> |
|#VALUE!  <br/> |**xlerrValue** <br/> |15  <br/> |
|#REF!  <br/> |**xlerrRef** <br/> |23  <br/> |
|#NAME?  <br/> |**xlerrName** <br/> |29  <br/> |
|#NUM!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#N/A  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>R�ckgabewert

Gibt ein **XltypeBool** mit den Fehlercode übergeben wird. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempErr12** -Funktion verwendet, um eine #VALUE zurück! Fehler in Excel. 
  
> [!NOTE]
> Die Bibliothek Framework-Funktion **TempErr12** reserviert Speicher aus einem internen Puffer, die normalerweise freigegeben wird, wenn die Framework-Funktion **Excel12f** aufgerufen wird. Wenn diese Beispielfunktion ohne **Excel12f** aufgerufen wird wiederholt aufgerufen wird, tritt ein, Speicherverluste. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

