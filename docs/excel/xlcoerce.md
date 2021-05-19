---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- xlcoerce-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424833"
---
# <a name="xlcoerce"></a>xlCoerce

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wandelt einen **XlOPER** /  **XLOPER12-Typ** in einen anderen um, oder es werden Zellwerte auf einem Blatt nach oben angezeigt. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Parameter

 _pxSource_
  
Die **XlOPER** /  **XLOPER12-Quelle,** die konvertiert werden muss. 
  
 _pxDestType_ (**xltypeInt**)
  
(Optional). Eine Bitmaske der resultierenden Typen, die Sie akzeptieren möchten. Sie sollten den bitweisen **OR-Operator** ( | ) verwenden, um mehrere mögliche Typen anzugeben. Wenn dieses Argument nicht angegeben wird, werden Verweise auf einzelne Zellen in einen der Werttypen **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (wenn die Zelle mit Bezug leer ist) konvertiert, und Verweise auf Zellblöcke werden in **xltypeMulti konvertiert.** Dadurch ist **xlCoerce** die bequemste Methode zum Suchen nach Zellenwerten. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt den koercierten Wert zurück (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** oder **xltypeMulti**).
  
## <a name="remarks"></a>Hinweise

 **xlCoerce kann** nicht in oder von **xltypeBigData oder** **xltypeFlow konvertiert werden.** Das Übergeben **eines xltypeMissing-** oder **xltypeNil-Typs** als  _pxDestType_ entspricht dem Weglassen des Arguments. Die Konvertierung kann in einigen Fällen fehlschlagen. Beispielsweise können einige Zeichenfolgen nicht in Zahlen konvertiert werden, andere dagegen. 
  
Wenn ein Array oder ein Verweis mit mehreren Zellen in einen einzelnen Werttyp konvertiert wird, ist das Ergebnis der Wert der linken oberen Zelle oder des Arrayelements.
  
## <a name="example"></a>Beispiel

Der folgende Code finden Sie unter  `\SAMPLES\EXAMPLE\EXAMPLE.C` . 
  
> [!NOTE]
> Die **xlcAlert-Funktion** versucht implizit, ihr Argument in eine Zeichenfolge zu konvertieren, sodass der hier gezeigte Coercion-Schritt entfernt werden konnte und **xInt** direkt an **xlcAlert** übergeben werden konnte. Da **xlcAlert** ein Befehlsmakro ist, funktioniert dieser Code nur ordnungsgemäß, wenn er von einem Makroblatt aufgerufen wird. 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a>Siehe auch



[xlSet](xlset.md)


[C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

