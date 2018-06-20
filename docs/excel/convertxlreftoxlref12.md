---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- convertxlreftoxlref12-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f2830633482e5329d285907b610386b708c406a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790400"
---
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Funktion, die versucht, eine **XLREF** in einer **XLREF12**zu konvertieren.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>Parameter

 _pxRef_ (**LPXLREF**)
  
Zeiger auf die Struktur der Datenquelle Verweis.
  
 _pxRef12_ (**LPXLREF12**)
  
Zeiger auf die Ziel-Referenz-Struktur in den konvertierte Wert platziert werden.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

 **True,** Wenn **die Konvertierung erfolgreich; andernfalls** . 
  
## <a name="remarks"></a>Hinweise

Vorausgesetzt, dass die übergebenen **XLREF** gültig ist, sollte dieser Vorgang immer erfolgreich durchgeführt werden. Im Gegensatz dazu schlägt Konvertierung die andere Möglichkeit von **XLREF12** , **XLREF**, [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), die von der angegebene Verweis auf Bestandteil einer Excel 2007-Arbeitsblatt bezieht, die in früheren Versionen nicht unterstützt wird.
  
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

