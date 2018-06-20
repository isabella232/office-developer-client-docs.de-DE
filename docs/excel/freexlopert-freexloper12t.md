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
# <a name="freexlopertfreexloper12t"></a><span data-ttu-id="fb539-104">FreeXLOperT/FreeXLOper12T</span><span class="sxs-lookup"><span data-stu-id="fb539-104">FreeXLOperT/FreeXLOper12T</span></span>

 <span data-ttu-id="fb539-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fb539-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fb539-106">Framework-Funktion, die ein **XLOPER**zugeordneten Arbeitsspeicher frei/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="fb539-106">Framework function that frees memory associated with an **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="fb539-107">Die Funktion wird davon ausgegangen, dass der Speicher mit Aufrufen in der DLL Malloc belegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fb539-107">The function assumes that the memory was allocated with calls to malloc within the DLL.</span></span> <span data-ttu-id="fb539-108">Wenn der Speicher von Microsoft Excel oder auf andere Weise oder von einem anderen Prozess belegt wurde, sollte diese Funktion nicht verwendet werden, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="fb539-108">If the memory was allocated by Microsoft Excel or in some other way or by some other process, this function should not be used to free the memory.</span></span> <span data-ttu-id="fb539-109">Mit der Speicher von Excel für **XLOPER** [XlFree](xlfree.md) / **XLOPER12**s.</span><span class="sxs-lookup"><span data-stu-id="fb539-109">Use [xlFree](xlfree.md) to free memory allocated by Excel for **XLOPER**/ **XLOPER12**s.</span></span> 
  
```cs
void FreeXLOperT(LPXLOPER pxloper);
void FreeXLOper12T(LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="fb539-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb539-110">Parameters</span></span>

 <span data-ttu-id="fb539-111">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="fb539-111">_pxloper_ (**LPXLOPER**)</span></span>
  
 <span data-ttu-id="fb539-112">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="fb539-112">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="fb539-113">Zeiger auf die **XLOPER**/ **XLOPER12** freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fb539-113">Pointer to the **XLOPER**/ **XLOPER12** to be freed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fb539-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fb539-114">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="fb539-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb539-115">See also</span></span>



[<span data-ttu-id="fb539-116">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="fb539-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

