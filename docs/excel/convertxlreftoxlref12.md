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
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 530cb9cce5b0023318ff6b8a0ff73472f8250aa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432030"
---
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Funktion, die versucht, eine **XLREF** in eine **XLREF12 zu konvertieren.**
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>Parameter

 _pxRef_ (**LPXLREF**)
  
Zeiger auf die Quellreferenzstruktur.
  
 _pxRef12_ (**LPXLREF12**)
  
Zeiger auf die Zielreferenzstruktur, in die der konvertierte Wert platziert werden soll.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

 **TRUE,** wenn die Konvertierung erfolgreich war, **andernfalls FALSE.** 
  
## <a name="remarks"></a>Hinweise

Sofern die übergebene **XLREF** gültig ist, sollte dieser Vorgang immer erfolgreich sein. Im Gegensatz dazu schlägt die Konvertierung von **XLREF12** in **XLREF**, die von [ConvertXLRef12ToXLRef](convertxlref12toxlref.md)ausgeführt wird, fehl, wenn sich der angegebene Verweis auf einen Teil eines Arbeitsblatts von Excel 2007 bezieht, das in früheren Versionen nicht unterstützt wird.
  
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

