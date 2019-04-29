---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- xlgetinst-Funktion [Excel 2007]
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
  
Gibt den Instanz-Handle der Instanz von Microsoft Excel zurück, die derzeit eine DLL aufruft.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Der Instanz-handle (**xltypeInt**) befindet sich im **Val. w** -Feld. 
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion kann verwendet werden, um zwischen mehreren laufenden Instanzen von Excel zu unterscheiden, die die DLL aufrufen.
  
Wenn Sie diese Funktion mithilfe von [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, handelt es sich bei der zurückgegebenen XLOPER-ganzzahligen Variablen um einen signierten 16-Bit-short-int-Wert. Dies kann nur die niedrigen 16 Bits des Windows-Handles von 32-Bit enthalten. Beginnend mit Excel 2007 ist die ganzzahlige Variable des **XLOPER12** ein signiertes 32-Bit int und enthält daher das gesamte handle, sodass nicht alle geöffneten Fenster durchlaufen werden müssen. 
  
> [!IMPORTANT]
> Wenn die **xlGetInst** -Funktion mit der 64-Bit-Version von Microsoft Excel verwendet wird, schlägt die Funktion fehl. Der Grund ist, dass der **xltypeInt** -Werttyp nicht breit genug ist, um das von Excel zurückgegebene 64-Bit Long-Handle in diesem Fall zu speichern. Zu diesem Zweck hat Excel 2010 eine neue Funktion namens [xlGetInstPtr](xlgetinstptr.md)eingeführt, die sowohl mit der 32-Bit-als auch der 64-Bit-Version von Excel ordnungsgemäß ausgeführt wird. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die Instanz der letzten Excel-Kopie, die Sie aufgerufen hat, mit der aktuellen Excel-Kopie verglichen, die Sie aufgerufen hat. Wenn Sie identisch sind, wird 1 zurückgegeben; Wenn dies nicht der Fall ist, wird 0 zurückgegeben; Wenn die Funktion fehlschlägt, gibt Sie-1 zurück.
  
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

