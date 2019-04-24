---
title: FreeXLOperT/FreeXLOper12T
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FreeXLOper12T
- FreeXLOperT
keywords:
- freexlopert-Funktion [Excel 2007], FreeXLOper12T-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 8fb3fdfd-8a43-4c50-82ff-e701fed3d83f
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 0b604cbe5cb24ac7d8de28278dfbcf0d4fd92c7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304074"
---
# <a name="freexlopertfreexloper12t"></a>FreeXLOperT/FreeXLOper12T

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Funktion, die Arbeitsspeicher frei gibt, der einem **XLOPER**/ **XLOPER12**zugeordnet ist. Die Funktion geht davon aus, dass der Arbeitsspeicher mit Aufrufen von malloc innerhalb der DLL reserviert wurde. Wenn der Arbeitsspeicher von Microsoft Excel oder auf andere Weise oder durch einen anderen Prozess zugewiesen wurde, sollte diese Funktion nicht zum Freigeben des Speichers verwendet werden. Verwenden Sie [xlFree](xlfree.md) , um von Excel für **XLOPER**/ **XLOPER12**s zugewiesene Arbeitsspeicher freizugeben. 
  
```cs
void FreeXLOperT(LPXLOPER pxloper);
void FreeXLOper12T(LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Parameter

 _pxloper_ (**LPXLOPER**)
  
 _pxloper12_ (**LPXLOPER12**)
  
Zeiger auf die **XLOPER**/ -**XLOPER12** , die freigegeben werden soll. 
  
## <a name="example"></a>Beispiel

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
void FreeXLOper12T(LPXLOPER12 pxloper12)
{
   DWORD xltype;
   int cxloper12;
   LPXLOPER12 pxloper12Free;
   xltype = pxloper12->xltype;
   switch (xltype)
   {
   case xltypeStr:
      if (pxloper12->val.str != NULL)
         free(pxloper12->val.str);
      break;
   case xltypeRef:
      if (pxloper12->val.mref.lpmref != NULL)
         free(pxloper12->val.mref.lpmref);
      break;
   case xltypeMulti:
      cxloper12 = pxloper12->val.array.rows * pxloper12->val.array.columns;
      if (pxloper12->val.array.lparray)
      {
         pxloper12Free = pxloper12->val.array.lparray;
         while (cxloper12 > 0)
         {
            FreeXLOper12T(pxloper12Free);
            pxloper12Free++;
            cxloper12--;
         }
         free(pxloper12->val.array.lparray);
      }
      break;
   case xltypeBigData:
      if (pxloper12->val.bigdata.h.lpbData != NULL)
         free(pxloper12->val.bigdata.h.lpbData);
      break;
   }
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

