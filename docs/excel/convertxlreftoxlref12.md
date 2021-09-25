---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- convertxlreftoxlref12-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f0f48a473024003628a3d0ec1059b4a4a971b78c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601401"
---
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Funktion, die versucht, ein **XLREF** in ein **XLREF12** zu konvertieren.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>Parameter

 _pxRef_ (**LPXLREF**)
  
Zeiger auf die Quellverweisstruktur.
  
 _pxRef12_ (**LPXLREF12**)
  
Zeiger auf die Zielverweisstruktur, in der der konvertierte Wert platziert werden soll.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

 **TRUE,** wenn die Konvertierung erfolgreich war, **andernfalls FALSE.** 
  
## <a name="remarks"></a>HinwBemerkungeneise

Vorausgesetzt, dass der übergebene **XLREF** gültig ist, sollte dieser Vorgang immer erfolgreich sein. Im Gegensatz dazu schlägt die Von [ConvertXLRef12ToXLRef](convertxlref12toxlref.md)durchgeführte Konvertierung von **XLREF12** in **XLREF** fehl, wenn der angegebene Verweis auf einen Teil eines Excel 2007-Arbeitsblatts verweist, das in früheren Versionen nicht unterstützt wird.
  
## <a name="example"></a>Beispiel

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxref, LPXLREF12 pxref12)
{
   if (pxref->rwLast >= pxref->rwFirst && pxref->colLast >= pxref->colFirst)
   {
      if (pxref->rwFirst >= 0 && pxref->colFirst >= 0)
      {
         pxref12->rwFirst = pxref->rwFirst;
         pxref12->rwLast = pxref->rwLast;
         pxref12->colFirst = pxref->colFirst;
         pxref12->colLast = pxref->colLast;
         return TRUE;
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

