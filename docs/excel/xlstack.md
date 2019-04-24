---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- xlstack-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310157"
---
# <a name="xlstack"></a>xlStack

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Überprüft den Abstand im Stapel.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt die Anzahl von Bytes (**xltypeInt**) zurück, die auf dem Stapel verbleiben.
  
## <a name="remarks"></a>Bemerkungen

Die Menge des verfügbaren Stapelspeichers der letzten Versionen überschreitet die 16-Bit-Ganzzahl mit Vorzeichen des **XLOPER**. Dies führt dazu, dass **xlStack** einen Wert zwischen-32767 und 32768 zurückgeben kann, wenn Sie mit **XLOPER**s und **Excel4** oder **Excel4v**aufgerufen werden. Wenn Sie in diesem Fall den richtigen Wert abrufen möchten, müssen Sie den zurückgegebenen Wert in einen unsigned Short umwandeln.
  
Ab Excel 2007 sollten Sie diese Funktion mit **XLOPER12**s und **Excel12** oder **Excel12v**aufrufen, in diesem Fall ist der zurückgegebene Wert Menge des verfügbaren Stapelspeichers oder 64 KB, je nachdem, welcher kleiner ist.
  
Excel weist nur begrenzten Speicherplatz auf dem Stapel auf, und Sie sollten diesen Speicherplatz nicht überschreiten. Legen Sie keine sehr großen Datenstrukturen auf den Stapel, und stellen Sie so viele lokale Variablen wie möglich statisch dar. Vermeiden Sie das Aufrufen von Funktionen rekursiv, da dadurch schnell der Stapel aufgefüllt wird.
  
Wenn Sie vermuten, dass Sie den Stapel überlaufen haben, rufen Sie diese Funktion häufig auf, um zu sehen, wie viel Stapelplatz noch übrig ist.
  
## <a name="example"></a>Beispiel

Im ersten Beispiel wird eine Warnmeldung mit der Menge des linken Stapelspeichers angezeigt, die `\SAMPLES\EXAMPLE\EXAMPLE.C`in enthalten ist. Im zweiten Beispiel wird die gleiche Funktion mit **XLOPER**s ausgeführt und ist nicht im SDK-Beispielcode enthalten.
  
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

- [C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

