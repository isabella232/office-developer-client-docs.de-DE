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
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66d2ac05b9603d6bb587a3898bde2545c1bb844a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407795"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird von Microsoft Excel aufgerufen, wenn der Add-In-Manager zum ersten Mal in einer Excel wird. Diese Funktion wird verwendet, um dem Add-In-Manager Informationen zu Ihrem Add-In zur Verfügung zu stellen.
  
Excel 2007 und höher wird **xlAddInManagerInfo12** vor **xlAddInManagerInfo** angezeigt, wenn sie von der XLL exportiert werden. Die **xlAddInManagerInfo12-Funktion** sollte auf die gleiche Weise wie **xlAddInManagerInfo** funktionieren, um versionsspezifische Unterschiede im Verhalten der XLL zu vermeiden. Excel erwartet, **dass xlAddInManagerInfo12** einen **XLOPER12-Datentyp** zurück gibt, **während xlAddInManagerInfo** einen **XLOPER zurückgeben sollte.**
  
Die **xlAddInManagerInfo12-Funktion** wird nicht von Versionen von Excel vor Excel 2007 aufgerufen, da diese **xlOPER12** nicht unterstützen.
  
Excel erfordert keine XLL zum Implementieren und Exportieren einer dieser Funktionen.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Parameter

 _pxAction:_ Ein Zeiger auf eine numerische **XLOPER/XLOPER12** (**xltypeInt** oder **xltypeNum**).
  
Die Von Excel verlangten Informationen.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn  _pxAction_ die Zahl 1 ist oder zu ihr gecced werden kann, sollte Ihre Implementierung dieser Funktion eine Zeichenfolge zurückgeben, die einige Informationen zum Add-In enthält, in der Regel seinen Namen und möglicherweise eine Versionsnummer. Andernfalls sollte #VALUE!. 
  
Wenn Sie keine Zeichenfolge zurückgeben, versucht Excel, den zurückgegebenen Wert in eine Zeichenfolge zu konvertieren.
  
## <a name="remarks"></a>Hinweise

Wenn die zurückgegebene Zeichenfolge auf dynamisch zugewiesenen Puffer verweist, müssen Sie sicherstellen, dass dieser Puffer schließlich frei wird. Wenn die Zeichenfolge von der Excel zugewiesen wurde, verwenden Sie dazu **xlbitXLFree**. Wenn die Zeichenfolge von der DLL zugewiesen wurde, verwenden Sie dazu **xlbitDLLFree** und müssen auch in [xlAutoFree](xlautofree-xlautofree12.md) (wenn Sie einen **XLOPER** zurückgeben) oder **xlAutoFree12** implementieren (wenn Sie einen **XLOPER12** zurückgeben).
  
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

