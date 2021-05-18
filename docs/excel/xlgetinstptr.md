---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fd4b4ad5bf52f29384ef7e0ba738c350189f471e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405282"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt das Instanzhandle der Instanz des Microsoft Excel, die derzeit eine DLL aufruft.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Das Instanzhandle (**xltypeBigData**) wird im **Feld val.bigdata.h.hdata** angezeigt. 
  
## <a name="remarks"></a>Hinweise

Diese Funktion kann verwendet werden, um zwischen mehreren ausgeführten Instanzen von Excel, die die DLL aufrufen, zu unterscheiden.
  
Diese Funktion gibt einen korrekten Wert mit 32-Bit- und 64-Bit-Versionen von Excel. Sie wurde in Excel 2010 als Erweiterung der [xlGetInst-Funktion](xlgetinst.md) eingeführt, die nur mit 32-Bit-Versionen von Excel. 
  
Diese Funktion funktioniert ordnungsgemäß, wenn sie mit den [Excel4- und Excel12-Varianten](excel4-excel12.md) der API-Rückruffunktionen aufgerufen wird, da **sowohl XLOPER** als auch **XLOPER12** dieselbe Struktur haben, die den **xltypeBigData-Werttyp** unterstützt. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die Instanz der letzten Kopie von Excel, die sie aufgerufen hat, mit der aktuellen Kopie von Excel, die sie aufgerufen hat, verglichen. Wenn sie identisch sind, wird 1 zurückgegeben. Andern falls nicht, wird 0 zurückgegeben. Wenn die Funktion fehlschlägt, gibt sie -1 zurück. Dieses Beispiel funktioniert sowohl mit 32-Bit- als auch mit 64-Bit-Excel.
  
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
- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

