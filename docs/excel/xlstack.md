---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- xlstack-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429979"
---
# <a name="xlstack"></a>xlStack

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Überprüft den Speicherplatz, der auf dem Stapel bleibt.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt die Anzahl der Bytes (**xltypeInt**) zurück, die auf dem Stapel bleiben.
  
## <a name="remarks"></a>Hinweise

Die Menge des verfügbaren Stapelspeichers der letzten Versionen überläuft die 16-Bit-signierte ganze Zahl der **XLOPER**. Dies bedeutet, **dass xlStack** einen Wert zwischen -32767 und 32768 zurückgeben kann, wenn er mithilfe von **XLOPER** s und **Excel4** oder **Excel4v** aufgerufen wird. Um in diesem Fall den richtigen Wert zu erhalten, müssen Sie den zurückgegebenen Wert in eine nicht signierte Short umgedumst haben.
  
Ab Excel 2007 sollten Sie diese Funktion mithilfe von **XLOPER12** s und **Excel12** oder **Excel12v** aufrufen, in diesem Fall ist der zurückgegebene Wert der verfügbare Stapelspeicher oder 64 KB, unabhängig davon, welcher Wert kleiner ist.
  
Excel verfügt über einen begrenzten Speicherplatz auf dem Stapel, und Sie sollten darauf achten, diesen Speicherplatz nicht zu überziehen. Legen Sie niemals sehr große Datenstrukturen auf den Stapel, und legen Sie so viele lokale Variablen wie möglich statisch fest. Vermeiden Sie rekursives Aufrufen von Funktionen, da dadurch der Stapel schnell auffüllt wird.
  
Wenn Sie vermuten, dass Sie den Stapel überlaufen, rufen Sie diese Funktion häufig auf, um zu sehen, wie viel Stapelspeicherplatz übrig bleibt.
  
## <a name="example"></a>Beispiel

Im ersten Beispiel wird eine Benachrichtigung angezeigt, die die Menge an Stapelspeicherplatz enthält, die in enthalten  `\SAMPLES\EXAMPLE\EXAMPLE.C` ist. Im zweiten Beispiel wird dasselbe Beispiel verwendet, das **mit XLOPER** s arbeitet und nicht im SDK-Beispielcode enthalten ist.
  
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

