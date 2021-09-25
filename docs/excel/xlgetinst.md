---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- Xlgetinst-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1346eb97fb70912c5acfb49bebffa016e05a17ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572340"
---
# <a name="xlgetinst"></a>xlGetInst

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt das Instanzenhandle der Instanz von Microsoft Excel zurück, die derzeit eine DLL aufruft.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Das Instanzhandle (**xltypeInt**) wird im **Feld val.w** angezeigt. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion kann verwendet werden, um zwischen mehreren ausgeführten Instanzen von Excel zu unterscheiden, die die DLL aufrufen.
  
Wenn Sie diese Funktion mit [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, ist die zurückgegebene XLOPER-Ganzzahlvariable eine signierte 16-Bit-Kurzformatierung. Dies kann nur die niedrigen 16 Bits des 32-Bit-Windows-Handles enthalten. Ab Excel 2007 ist die Ganzzahlvariable von **XLOPER12** ein signiertes 32-Bit-Int und enthält daher das gesamte Handle, sodass alle geöffneten Fenster nicht durchlaufen werden müssen. 
  
> [!IMPORTANT]
> Wenn die **xlGetInst-Funktion** mit der 64-Bit-Version von Microsoft Excel verwendet wird, schlägt die Funktion fehl. Dies liegt daran, dass der **XltypeInt-Werttyp** nicht breit genug ist, um den 64-Bit-Long-Handle zu speichern, der von Excel in diesem Fall zurückgegeben wird. Zu diesem Zweck wurde Excel 2010 eine neue Funktion namens [xlGetInstPtr](xlgetinstptr.md)eingeführt, die sowohl mit der 32-Bit- als auch der 64-Bit-Version von Excel ordnungsgemäß ausgeführt wird. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die Instanz der letzten Kopie von Excel, die sie aufgerufen hat, mit der aktuellen Kopie von Excel verglichen, die sie aufgerufen hat. Wenn sie identisch sind, wird 1 zurückgegeben. ist dies nicht der Fehler, wird 0 zurückgegeben. wenn die Funktion fehlschlägt, wird -1 zurückgegeben.
  
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

