---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790617"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt die Instanzzugriffsnummer der Instanz von Microsoft Excel, die derzeit eine DLL aufruft.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Die Instanzzugriffsnummer (**XltypeBigData**) werden im Feld **val.bigdata.h.hdata** . 
  
## <a name="remarks"></a>Hinweise

Diese Funktion kann mehrere ausgeführten Instanzen von Excel unterscheiden, die die DLL aufruft, sind verwendet werden.
  
Diese Funktion gibt den richtigen Wert mit 32-Bit- und 64-Bit-Versionen von Excel. Es wurde in Excel 2010 als Erweiterung der Funktion [XlGetInst](xlgetinst.md) eingeführt die ordnungsgemäß nur mit 32-Bit-Versionen von Excel funktioniert. 
  
Diese Funktion funktioniert ordnungsgemäß, wenn sie mithilfe der [Excel4 und Excel12](excel4-excel12.md) Varianten Rückruffunktionen API aufgerufen wird, da **XLOPER** und **XLOPER12** dieselbe Struktur aufweisen, die den Wert **XltypeBigData** unterstützt Geben Sie ein. 
  
## <a name="example"></a>Beispiel

Das folgende Beispiel vergleicht die Instanz der letzten Kopie von Excel, die sie an der aktuellen Version von Excel aufgerufen, die diese aufgerufen. Wenn sie identisch sind, gibt 1 zurück. Wenn dies nicht der Fall ist, sie gibt 0 zurück; Wenn die Funktion fehlschlägt, gibt-1 zurück. Dieses Beispiel funktioniert mit 32-Bit- und 64-Bit-Versionen von Excel.
  
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

