---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- convertxlref12toxlref-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 15f4576bd988668b2f9e06ca7790afa27dd97aad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576730"
---
# <a name="convertxlref12toxlref"></a>ConvertXLRef12ToXLRef

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Versucht, ein **XLREF12** in ein **XLREF** zu konvertieren.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a>Parameter

 _pxRef12_ (**LPXLREF12**)
  
Zeiger auf die Quellverweisstruktur.
  
 _pxRef_ (**LPXLREF**)
  
Zeiger auf die Zielverweisstruktur, in der der konvertierte Wert platziert werden soll.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

 **TRUE,** wenn die Konvertierung erfolgreich war, **andernfalls FALSE.** 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Konvertierung von **XLREF12** in **XLREF** schlägt fehl, wenn sich der angegebene Verweis auf einen Teil eines Arbeitsblatts Excel 2007 bezieht, der in früheren Versionen nicht unterstützt wird. 
  
## <a name="example"></a>Beispiel

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRef12ToXLRef(LPXLREF12 pxref12, LPXLREF pxref)
{
   if (pxref12->rwLast >= pxref12->rwFirst && pxref12->colLast >= pxref12->colFirst)
   {
      if (pxref12->rwFirst >=0 && pxref12->colFirst >= 0)
      {
         if (pxref12->rwLast < rwMaxO8 && pxref12->colLast < colMaxO8)
         {
            pxref->rwFirst = (WORD)pxref12->rwFirst;
            pxref->rwLast = (WORD)pxref12->rwLast;
            pxref->colFirst = (BYTE)pxref12->colFirst;
            pxref->colLast = (BYTE)pxref12->colLast;
            return TRUE;
         }
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

