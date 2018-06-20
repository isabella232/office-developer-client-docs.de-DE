---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- XlStack-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fcd073f7d2b97e84743d01c498435f186277e345
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790613"
---
# <a name="xlstack"></a>xlStack

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Überprüft die Menge freier Speicherplatz auf dem Stapel.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Gibt die Anzahl von Bytes (**vom Typ XltypeInt**) auf dem Stapel verbleibenden zurück.
  
## <a name="remarks"></a>Hinweise

Die Menge an verfügbaren Stapelspeicher aktueller Versionen überschreitet die 16-Bit-Ganzzahl mit Vorzeichen von der **XLOPER**. Dies bedeutet, dass diese **XlStack** einen Wert zwischen-32767 und 32768 bei einem Aufruf mit **XLOPER**s und **Excel4** oder **Excel4v**zurückgeben kann. Um müssen den richtigen Wert in diesem Fall abzurufen, Sie den zurückgegebenen Wert in eine nicht signierte kurze umgewandelt.
  
Starten in Excel 2007, müssen Sie diese Funktion mithilfe von **XLOPER12**s und **Excel12** aufrufen oder **Excel12v**, in dem Fall den zurückgegebenen Wert Stack verfügbaren Speicherplatz oder 64 KB, ist der kleinere der Werte ist.
  
Excel verfügt über eine begrenzte Menge an Speicherplatz auf dem Stapel und sollte nicht zum Überschreitung dieses Speicherplatz sorgfältig. Sehr große Datenstrukturen nie auf dem Stapel zu platzieren und wie viele lokale Variablen möglichst statische erleichtern. Vermeiden Sie die Funktionen rekursiv aufrufen, da, die den Stapel schnell gefüllt wird.
  
Wenn Sie annehmen, dass Sie den Stapel dieses sind, rufen Sie diese Funktion häufig, um festzustellen, wie viel Speicherplatz bleibt.
  
## <a name="example"></a>Beispiel

Im ersten Beispiel wird eine Meldung mit der Menge an Speicherplatz Stack und in enthalten ist `\SAMPLES\EXAMPLE\EXAMPLE.C`. Im zweite Beispiel werden dieselben, arbeiten mit **XLOPER**s und nicht in der SDK-Beispiel-Code enthalten ist.
  
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

