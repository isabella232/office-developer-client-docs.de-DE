---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- xlgetinst-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e113ddbf55e2b4651d578549802c44e2c6413a18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428130"
---
# <a name="xlgetinst"></a>xlGetInst

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt das Instanzhandle der Instanz des Microsoft Excel, die derzeit eine DLL aufruft.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Das Instanzhandle (**xltypeInt**) wird im **Val.w-Feld** angezeigt. 
  
## <a name="remarks"></a>Hinweise

Diese Funktion kann verwendet werden, um zwischen mehreren ausgeführten Instanzen von Excel, die die DLL aufrufen, zu unterscheiden.
  
Wenn Sie diese Funktion mithilfe von [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, ist die zurückgegebene XLOPER-Ganzzahlvariable eine signierte 16-Bit-Short-Int. Dies kann nur die niedrigen 16 Bit des 32-Bit-Windows enthalten. Ab Excel 2007 ist die ganzzahlige Variable des **XLOPER12** ein signiertes 32-Bit-Int und enthält daher das gesamte Handle, ohne dass alle geöffneten Fenster durch iteriert werden müssen. 
  
> [!IMPORTANT]
> Wenn die **xlGetInst-Funktion** mit der 64-Bit-Version von Microsoft Excel verwendet wird, kann die Funktion fehlschlagen. Dies liegt daran, dass der **xltypeInt-Werttyp** nicht breit genug ist, um den 64-Bit-Long-Handle zu halten, der von Excel in diesem Fall zurückgegeben wird. Zu diesem Zweck wurde Excel 2010 eine neue Funktion namens [xlGetInstPtr](xlgetinstptr.md)eingeführt, die sowohl mit der 32-Bit- als auch der 64-Bit-Version von Excel. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die Instanz der letzten Kopie von Excel, die sie aufgerufen hat, mit der aktuellen Kopie von Excel, die sie aufgerufen hat, verglichen. Wenn sie identisch sind, wird 1 zurückgegeben. Andern falls nicht, wird 0 zurückgegeben. Wenn die Funktion fehlschlägt, gibt sie -1 zurück.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a>Siehe auch



[xlGetHwnd](xlgethwnd.md)
  
[xlGetInstPtr](xlgetinstptr.md)


[C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

