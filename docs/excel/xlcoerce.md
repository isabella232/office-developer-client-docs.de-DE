---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- Xlcoerce-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e02020b6afe67e9c1035e63866c2dd9bff0b24c6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621346"
---
# <a name="xlcoerce"></a>xlCoerce

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Konvertiert einen **XLOPER** /  **XLOPER12-Typ** in einen anderen oder sucht zellwerte auf einem Blatt nach. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Parameter

 _pxSource_
  
Die **XLOPER** /  **XLOPER12-Quelldatei,** die konvertiert werden muss. 
  
 _pxDestType_ (**xltypeInt**)
  
(Optional). Eine Bitmaske der resultierenden Typen, die Sie akzeptieren möchten. Sie sollten den bitweisen **OR-Operator** ( | ) verwenden, um mehrere mögliche Typen anzugeben. Wenn dieses Argument nicht angegeben wird, werden Verweise auf einzelne Zellen in einen der Werttypen **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (wenn die referenzierte Zelle leer ist) konvertiert, und Verweise auf Zellenblöcke werden in **xltypeMulti** konvertiert. Dadurch ist **xlCoerce** die bequemste Methode zum Nachschlagen von Zellwerten. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt den koersierten Wert (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** oder **xltypeMulti**) zurück.
  
## <a name="remarks"></a>Bemerkungen

 **xlCoerce** kann nicht in **xltypeBigData** oder **xltypeFlow** konvertiert werden. Das Übergeben eines **XltypeMissing-** oder **xltypeNil-Typs** als  _pxDestType_ entspricht dem Weglassen des Arguments. Die Konvertierung kann in einigen Fällen fehlschlagen. Beispielsweise können einige Zeichenfolgen nicht in Zahlen konvertiert werden, andere dagegen. 
  
Wenn ein Array oder ein Bezug mit mehreren Zellen in einen einzelnen Werttyp konvertiert wird, ist das Ergebnis der Wert der oberen linken Zelle oder des Arrayelements.
  
## <a name="example"></a>Beispiel

Der folgende Code befindet sich in  `\SAMPLES\EXAMPLE\EXAMPLE.C` . 
  
> [!NOTE]
> Die **xlcAlert-Funktion** versucht implizit, ihr Argument in eine Zeichenfolge zu konvertieren, sodass der hier gezeigte Koersionsschritt tatsächlich entfernt und **xInt** direkt an **xlcAlert** übergeben werden kann. Da **xlcAlert** ein Befehlsmakro ist, funktioniert dieser Code nur ordnungsgemäß, wenn er von einem Makroblatt aufgerufen wird. 
  
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

