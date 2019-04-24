---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- xlCoerce-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303962"
---
# <a name="xlcoerce"></a>xlCoerce

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Konvertiert einen Typ von **XLOPER**/ **XLOPER12** in einen anderen oder sucht Zellenwerte in einem Blatt. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Parameter

 _pxSource_
  
Die Quell- **XLOPER**/ **XLOPER12** , die konvertiert werden muss. 
  
 _pxDestType_ (**xltypeInt**)
  
(Optional). Eine Bitmaske der resultierenden Typen, die Sie akzeptieren möchten. Sie sollten den bitweisen **or** -Operator (|) verwenden, um mehrere mögliche Typen anzugeben. Wenn dieses Argument ausgelassen wird, werden Verweise auf einzelne Zellen in einen der Wertetypen **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (wenn die referenzierte Zelle leer ist) und Verweise auf Blöcke konvertiert. von Zellen werden in **xltypeMulti**konvertiert. Damit ist **xlCoerce** die bequemste Methode zum Nachschlagen von Zellwerten. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt den umgewandelten Wert (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**oder **xltypeMulti**) zurück.
  
## <a name="remarks"></a>Bemerkungen

 **xlCoerce** kann nicht in oder aus **xltypeBigData** oder **xltypeFlow**konvertieren. Das Übergeben eines **xltypeMissing** -oder **xltypeNil** -Typs als _pxDestType_ entspricht dem Weglassen des Arguments. In einigen Fällen kann die Konvertierung fehlschlagen. Einige Zeichenfolgen können beispielsweise nicht in Zahlen konvertiert werden, andere jedoch. 
  
Wenn ein Array oder ein mehr zellenverweis in einen einzelnen Werttyp konvertiert wird, ist das Ergebnis der Wert der oberen linken Zelle oder des Arrayelements.
  
## <a name="example"></a>Beispiel

Den folgenden Code finden Sie unter `\SAMPLES\EXAMPLE\EXAMPLE.C`. 
  
> [!NOTE]
> Die **xlcAlert** -Funktion versucht implizit, das Argument in eine Zeichenfolge umzuwandeln, sodass der hier gezeigte Umwandlungs Schritt tatsächlich entfernt werden kann und **XInt** direkt an **xlcAlert**übergeben werden kann. Da **xlcAlert** ein Befehlsmakro ist, funktioniert dieser Code nur dann ordnungsgemäß, wenn er von einem Makroblatt aufgerufen wird. 
  
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


[C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

