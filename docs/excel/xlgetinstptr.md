---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fd4b4ad5bf52f29384ef7e0ba738c350189f471e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310052"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt den Instanz-Handle der Instanz von Microsoft Excel zurück, die derzeit eine DLL aufruft.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Der Instanzen Handler (**xltypeBigData**) befindet sich im Feld **Val. hdata. h.** . 
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion kann verwendet werden, um zwischen mehreren laufenden Instanzen von Excel zu unterscheiden, die die DLL aufrufen.
  
Diese Funktion gibt einen korrekten Wert mit sowohl 32-Bit-als auch 64-Bit-Versionen von Excel zurück. Es wurde in Excel 2010 als Erweiterung der [xlGetInst](xlgetinst.md) -Funktion eingeführt, die nur mit 32-Bit-Versionen von Excel ordnungsgemäß funktioniert. 
  
Diese Funktion funktioniert ordnungsgemäß, wenn Sie aufgerufen wird, indem sowohl die [Excel4-als auch die Excel12](excel4-excel12.md) -Vielzahl der API-Rückruffunktionen verwendet wird, da sowohl **XLOPER** als auch **XLOPER12** die gleiche Struktur aufweisen, die den **xltypeBigData** -Wert unterstützt. Typ. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die Instanz der letzten Excel-Kopie, die Sie aufgerufen hat, mit der aktuellen Excel-Kopie verglichen, die Sie aufgerufen hat. Wenn Sie identisch sind, wird 1 zurückgegeben; Wenn dies nicht der Fall ist, wird 0 zurückgegeben; Wenn die Funktion fehlschlägt, gibt Sie-1 zurück. Dieses Beispiel funktioniert sowohl mit 32-als auch 64-Bit-Versionen von Excel.
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
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

- [xlGetHwnd](xlgethwnd.md)
- [xlGetInst](xlgetinst.md)
- [C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

