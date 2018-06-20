---
title: XlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- Xladdinmanagerinfo-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e42cca809c4426ddf9a98b3b275d08490d31c8db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790573"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>XlAddInManagerInfo/xlAddInManagerInfo12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird von Microsoft Excel aufgerufen, wenn der Add-In-Manager zum ersten Mal in einer Excel-Sitzung aufgerufen wird. Diese Funktion wird das Add-In-Manager Informationen über das Add-in bereitzustellen.
  
Excel 2007 und spätere Versionen aufrufen **xlAddInManagerInfo12** anstelle von **XlAddInManagerInfo** , wenn durch die XLL exportiert. Die Funktion **xlAddInManagerInfo12** sollte auf die gleiche Weise als **XlAddInManagerInfo** zur Vermeidung von versionsspezifischen Unterschiede im Verhalten von XLL funktionieren. Excel erwartet **xlAddInManagerInfo12** einen **XLOPER12** -Datentyp zurück, während ein **XLOPER** **XlAddInManagerInfo** zurückgegeben werden soll.
  
Die **xlAddInManagerInfo12** -Funktion wird nicht von früheren Versionen von Excel als Excel 2007 aufgerufen, wie diese **XLOPER12**nicht unterstützen.
  
Excel erforderlich keine XLL zu implementieren und exportieren Sie eine dieser Funktionen.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Parameter

 _PxAction:_ Ein Zeiger auf eine numerische **XLOPER/XLOPER12** (**vom Typ XltypeInt** oder **XltypeNum**).
  
Die Informationen, der für Excel Listenbereich anfordert.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

_PxAction_ umgewandelt werden kann, um die Zahl 1 oder ist, sollte die Implementierung von dieser Funktion eine Zeichenfolge mit einige Informationen über das Add-in, in der Regel seinen Namen und möglicherweise eine Versionsnummer zurückgegeben. Andernfalls sollte es #VALUE zurück!. 
  
Wenn Sie keine Zeichenfolge zurückzugeben, versucht Excel den zurückgegebenen Wert in eine Zeichenfolge zu konvertieren.
  
## <a name="remarks"></a>Hinweise

Wenn die zurückgegebene Zeichenfolge an dynamisch zugewiesenen Puffer verweist, müssen Sie sicherstellen, dass dieser Puffer schließlich freigegeben wird. Wenn die Zeichenfolge von Excel belegt wurde, Sie zu diesem Zweck **XlbitXLFree**festlegen. Wenn die Zeichenfolge von der DLL belegt wurde, zu diesem Zweck Einstellung **XlbitDLLFree**und müssen Sie auch in implementieren [XlAutoFree](xlautofree-xlautofree12.md) (Wenn Sie eine **XLOPER**zurückgeben) oder **xlAutoFree12** (Wenn Sie eine **XLOPER12**zurückgeben).
  
## <a name="example"></a>Beispiel

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a>Siehe auch



[Add-In-Manager und Funktionen von XLL-Schnittstelle](add-in-manager-and-xll-interface-functions.md)

