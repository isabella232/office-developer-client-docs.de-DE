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
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9484f7bbc1f5e0fc5b0def17f2ce79ef226dcd17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790605"
---
# <a name="xlgetinst"></a>xlGetInst

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt die Instanzzugriffsnummer der Instanz von Microsoft Excel, die derzeit eine DLL aufruft.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Die Instanzzugriffsnummer (**vom Typ XltypeInt**) werden im Feld **val.w** . 
  
## <a name="remarks"></a>Hinweise

Diese Funktion kann mehrere ausgeführten Instanzen von Excel unterscheiden, die die DLL aufruft, sind verwendet werden.
  
Wenn Sie diese Funktion mit [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, wird die zurückgegebene XLOPER ganzzahlige Variable einer signierten 16-Bit-short int Dies ist nur die unteren 16 Bits der 32-Bit-Windows-Handle enthalten kann. Ab Excel 2007, die ganzzahlige Variable der **XLOPER12** ist eine signierte 32-Bit-Int und aus diesem Grund enthält das gesamte Handle, entfernen alle geöffneten Fenster durchlaufen werden müssen. 
  
> [!IMPORTANT]
> Wenn die **XlGetInst** -Funktion mit der 64-Bit-Version von Microsoft Excel verwendet wird, schlägt die Funktion fehl. Dies ist, da der Werttyp **vom Typ XltypeInt** nicht breit genug für das lange 64-Bit-Handle zurückgegeben von Excel in diesem Fall enthalten ist. Für diesen Zweck eingeführt Excel 2010 eine neue Funktion mit dem Namen [XlGetInstPtr](xlgetinstptr.md), der mit der 32-Bit- und 64-Bit-Versionen von Excel ordnungsgemäß ausgeführt wird. 
  
## <a name="example"></a>Beispiel

Das folgende Beispiel vergleicht die Instanz der letzten Kopie von Excel, die sie an der aktuellen Version von Excel aufgerufen, die diese aufgerufen. Wenn sie identisch sind, gibt 1 zurück. Wenn dies nicht der Fall ist, sie gibt 0 zurück; Wenn die Funktion fehlschlägt, gibt-1 zurück.
  
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


[C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

