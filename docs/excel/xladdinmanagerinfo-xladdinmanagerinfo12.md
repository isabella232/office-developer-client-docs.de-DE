---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- xladdinmanagerinfo-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ebd7c4f8cd7e93ea9c3b838cc89d48ffdd60d503
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572354"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird von Microsoft Excel aufgerufen, wenn der Add-In-Manager zum ersten Mal in einer Excel Sitzung aufgerufen wird. Diese Funktion wird verwendet, um dem Add-In-Manager Informationen zu Ihrem Add-In bereitzustellen.
  
Excel 2007 und neuere Versionen rufen **xlAddInManagerInfo12** vor **xlAddInManagerInfo** auf, wenn sie von der XLL exportiert werden. Die **XlAddInManagerInfo12-Funktion** sollte auf die gleiche Weise wie **xlAddInManagerInfo funktionieren,** um versionsspezifische Unterschiede im Verhalten der XLL zu vermeiden. Excel erwartet, **dass xlAddInManagerInfo12** einen **XLOPER12-Datentyp** zurückgibt, während **xlAddInManagerInfo** einen **XLOPER** zurückgeben sollte.
  
Die **XlAddInManagerInfo12-Funktion** wird nicht von Versionen von Excel vor Excel 2007 aufgerufen, da diese **xlOPER12** nicht unterstützen.
  
Excel erfordert keine XLL, um eine dieser Funktionen zu implementieren und zu exportieren.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Parameter

 _pxAction:_ Ein Zeiger auf eine numerische **XLOPER/XLOPER12** (**xltypeInt** oder **xltypeNum**).
  
Die Informationen, die Excel anfragt.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn  _pxAction_ die Zahl 1 ist oder in diese konvertiert werden kann, sollte Die Implementierung dieser Funktion eine Zeichenfolge mit einigen Informationen über das Add-In zurückgeben, in der Regel den Namen und möglicherweise eine Versionsnummer. Andernfalls sollte #VALUE! zurückgegeben werden. 
  
Wenn Sie keine Zeichenfolge zurückgeben, versucht Excel, den zurückgegebenen Wert in eine Zeichenfolge zu konvertieren.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die zurückgegebene Zeichenfolge auf den dynamisch zugeordneten Puffer zeigt, müssen Sie sicherstellen, dass dieser Puffer schließlich freigegeben wird. Wenn die Zeichenfolge von Excel zugewiesen wurde, legen Sie **xlbitXLFree** fest. Wenn die Zeichenfolge von der DLL zugewiesen wurde, legen Sie **xlbitDLLFree** fest, und Sie müssen auch [xlAutoFree](xlautofree-xlautofree12.md) implementieren (wenn Sie ein **XLOPER** zurückgeben) oder **xlAutoFree12** (wenn Sie eine **XLOPER12** zurückgeben).
  
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



[Add-In-Manager und XLL-Benutzeroberflächenfunktionen](add-in-manager-and-xll-interface-functions.md)

