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
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0a12052a93d030088feb548449955129ff5bdc0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432653"
---
# <a name="convertxlref12toxlref"></a>ConvertXLRef12ToXLRef

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Versucht, eine **XLREF12 in** eine **XLREF zu konvertieren.**
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a>Parameter

 _pxRef12_ (**LPXLREF12**)
  
Zeiger auf die Quellreferenzstruktur.
  
 _pxRef_ (**LPXLREF**)
  
Zeiger auf die Zielreferenzstruktur, in die der konvertierte Wert platziert werden soll.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

 **TRUE,** wenn die Konvertierung erfolgreich war, **andernfalls FALSE.** 
  
## <a name="remarks"></a>Hinweise

Die Konvertierung von **XLREF12** in **XLREF** schlägt fehl, wenn sich der angegebene Verweis auf einen Teil eines Arbeitsblatts von Excel 2007 bezieht, das in früheren Versionen nicht unterstützt wird. 
  
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

