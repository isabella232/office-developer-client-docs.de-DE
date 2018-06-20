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
- Freexlopert-Funktion [excel 2007], FreeXLOper12T-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 8fb3fdfd-8a43-4c50-82ff-e701fed3d83f
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7411bc51770dadc7c2d4a5c2c65d2d546f6025f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790508"
---
# <a name="freexlopertfreexloper12t"></a>FreeXLOperT/FreeXLOper12T

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Funktion, die ein **XLOPER**zugeordneten Arbeitsspeicher frei/ **XLOPER12**. Die Funktion wird davon ausgegangen, dass der Speicher mit Aufrufen in der DLL Malloc belegt wurde. Wenn der Speicher von Microsoft Excel oder auf andere Weise oder von einem anderen Prozess belegt wurde, sollte diese Funktion nicht verwendet werden, um den Arbeitsspeicher freizugeben. Mit der Speicher von Excel für **XLOPER** [XlFree](xlfree.md) / **XLOPER12**s. 
  
```cs
void FreeXLOperT(LPXLOPER pxloper);
void FreeXLOper12T(LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Parameter

 _pxloper_ (**LPXLOPER**)
  
 _pxloper12_ (**LPXLOPER12**)
  
Zeiger auf die **XLOPER**/ **XLOPER12** freigegeben werden. 
  
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

