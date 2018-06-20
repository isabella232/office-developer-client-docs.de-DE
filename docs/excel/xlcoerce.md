---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- XlCoerce-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0474b81a6d24663fe85303efc8fe2fd62cfdd82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790599"
---
# <a name="xlcoerce"></a>xlCoerce

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Konvertiert einen Typ von **XLOPER**/ **XLOPER12** in eine andere oder sucht Werte von Zellen in einem Blatt. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Parameter

 _pxSource_
  
Die Quelle **XLOPER**/ **XLOPER12** , die konvertiert werden muss. 
  
 _pxDestType_ (**vom Typ XltypeInt**)
  
(Optional). Eine Bitmaske der resultierenden Typen sind Sie bereit, akzeptieren. Sie sollten den bitweisen **OR** -Operator (|) verwenden, um mehrere möglichen Typen anzugeben. Wenn dieses Argument ausgelassen wird, werden Verweise auf einzelne Zellen konvertiert auf eine der der Wert Typen **XltypeStr**, **XltypeNum**, **XltypeBool**, **XltypeErr**, **XltypeNil** (wenn die genannten Zelle leer ist) und Verweise auf blockiert Zellen werden in **XltypeMulti**konvertiert. Auf diese Weise **XlCoerce** Weise Zellwerten nachzuschlagen. 
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Gibt den umgewandelten Wert (**XltypeStr**, **XltypeNum**, **XltypeBool**, **XltypeErr**, **XltypeNil**oder **XltypeMulti**) zurück.
  
## <a name="remarks"></a>Hinweise

 **XlCoerce** kann nicht zu oder von **XltypeBigData** oder **XltypeFlow**konvertiert. Übergeben einen Typ **XltypeMissing** oder **XltypeNil** als _PxDestType_ entspricht das Argument auslassen. In einigen Fällen kann Konvertierung fehl. Beispielsweise können einige Zeichenfolgen in Zahlen, konvertiert werden, während andere Benutzer können. 
  
Wenn ein Array oder ein mit mehreren Zellbezug zu einem einzelnen Wert umgewandelt wird, ist das Ergebnis der Wert des oberen linken Zelle oder Array-Elements an.
  
## <a name="example"></a>Beispiel

Der folgende Code finden Sie unter `\SAMPLES\EXAMPLE\EXAMPLE.C`. 
  
> [!NOTE]
> Die Funktion **XlcAlert** versucht implizit Argument in eine Zeichenfolge zu konvertieren, damit der hier gezeigte Koersion Schritt tatsächlich entfernt konnte und **xInt** direkt an **XlcAlert**übergeben werden konnte. Wie **XlcAlert** ein Makro mit Befehlen ist, funktioniert diesen Code nur ordnungsgemäß Wenn von einem Makroblatt aufgerufen. 
  
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



[gleich xlSet](xlset.md)


[C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

