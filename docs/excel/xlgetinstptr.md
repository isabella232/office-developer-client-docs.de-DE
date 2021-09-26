---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6ac86bce80520c924fcc3d50ffd04f186a3d29e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631412"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt das Instanzhandle der Instanz von Microsoft Excel zurück, die derzeit eine DLL aufruft.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Das Instanzhandle (**xltypeDigData**) befindet sich im **Feld "val.bigdata.h.hdata".** 
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion kann verwendet werden, um zwischen mehreren ausgeführten Instanzen von Excel zu unterscheiden, die die DLL aufrufen.
  
Diese Funktion gibt einen korrekten Wert mit 32-Bit- und 64-Bit-Versionen von Excel zurück. Sie wurde in Excel 2010 als Erweiterung der [xlGetInst-Funktion](xlgetinst.md) eingeführt, die nur mit 32-Bit-Versionen von Excel ordnungsgemäß funktioniert. 
  
Diese Funktion funktioniert ordnungsgemäß, wenn sie mithilfe der [Excel4- und Excel12-Varianten](excel4-excel12.md) der API-Rückruffunktionen aufgerufen wird, da **XLOPER** und **XLOPER12** dieselbe Struktur aufweisen, die den **XltypeBigData-Werttyp** unterstützt. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die Instanz der letzten Kopie von Excel, die sie aufgerufen hat, mit der aktuellen Kopie von Excel verglichen, die sie aufgerufen hat. Wenn sie identisch sind, wird 1 zurückgegeben. ist dies nicht der Fehler, wird 0 zurückgegeben. wenn die Funktion fehlschlägt, wird -1 zurückgegeben. Dieses Beispiel funktioniert sowohl mit 32-Bit- als auch mit 64-Bit-Versionen von Excel.
  
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

