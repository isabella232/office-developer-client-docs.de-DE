---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- Xlstack-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 455de097446af6e96e2655cef66fcc84adbbd203
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621297"
---
# <a name="xlstack"></a>xlStack

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Überprüft, wie viel Platz auf dem Stapel bleibt.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt die Anzahl der Bytes (**xltypeInt**) zurück, die im Stapel verbleiben.
  
## <a name="remarks"></a>Bemerkungen

Der verfügbare Stapelspeicher der letzten Versionen überläuft die 16-Bit-Ganzzahl mit Vorzeichen des **XLOPER.** Dies bedeutet, dass **xlStack** einen Wert zwischen -32767 und 32768 zurückgeben kann, wenn er mit **XLOPER** s und **Excel4** oder **Excel4v** aufgerufen wird. Um den richtigen Wert in diesem Fall zu erhalten, müssen Sie den zurückgegebenen Wert in eine unsignierte Abkürzung umwandeln.
  
Ab Excel 2007 sollten Sie diese Funktion mit **XLOPER12** s und **Excel12** oder **Excel12v** aufrufen. In diesem Fall ist der zurückgegebene Wert der verfügbare Stapelspeicher oder 64 KB, je nachdem, welcher der kleinere ist.
  
Excel verfügt über einen begrenzten Speicherplatz auf dem Stapel, und Sie sollten darauf achten, diesen Speicherplatz nicht zu überlaufen. Legen Sie niemals sehr große Datenstrukturen in den Stapel, und erstellen Sie so viele lokale Variablen wie möglich statisch. Vermeiden Sie rekursives Aufrufen von Funktionen, da dadurch der Stapel schnell gefüllt wird.
  
Wenn Sie vermuten, dass Sie den Stapel überlaufen, rufen Sie diese Funktion häufig auf, um zu sehen, wie viel Stapelspeicher übrig bleibt.
  
## <a name="example"></a>Beispiel

Im ersten Beispiel wird eine Warnmeldung angezeigt, die den linken Stapelplatz enthält und in enthalten  `\SAMPLES\EXAMPLE\EXAMPLE.C` ist. Im zweiten Beispiel wird dieselbe Aktion ausgeführt, wobei **XLOPER-Elemente** verwendet werden und nicht im SDK-Beispielcode enthalten sind.
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a>Siehe auch

- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

