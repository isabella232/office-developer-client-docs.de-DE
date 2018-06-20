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
# <a name="convertxlreftoxlref12"></a><span data-ttu-id="882e4-104">ConvertXLRefToXLRef12</span><span class="sxs-lookup"><span data-stu-id="882e4-104">ConvertXLRefToXLRef12</span></span>

<span data-ttu-id="882e4-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="882e4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="882e4-106">Framework-Funktion, die versucht, eine **XLREF** in einer **XLREF12**zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="882e4-106">Framework function that attempts to convert an **XLREF** into an **XLREF12**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a><span data-ttu-id="882e4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="882e4-107">Parameters</span></span>

 <span data-ttu-id="882e4-108">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="882e4-108">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="882e4-109">Zeiger auf die Struktur der Datenquelle Verweis.</span><span class="sxs-lookup"><span data-stu-id="882e4-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="882e4-110">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="882e4-110">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="882e4-111">Zeiger auf die Ziel-Referenz-Struktur in den konvertierte Wert platziert werden.</span><span class="sxs-lookup"><span data-stu-id="882e4-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="882e4-112">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="882e4-112">Property value/Return value</span></span>

 <span data-ttu-id="882e4-113">**True,** Wenn **die Konvertierung erfolgreich; andernfalls** .</span><span class="sxs-lookup"><span data-stu-id="882e4-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="882e4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="882e4-114">Remarks</span></span>

<span data-ttu-id="882e4-115">Vorausgesetzt, dass die übergebenen **XLREF** gültig ist, sollte dieser Vorgang immer erfolgreich durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="882e4-115">Provided that the passed-in **XLREF** is valid, this operation should always be successful.</span></span> <span data-ttu-id="882e4-116">Im Gegensatz dazu schlägt Konvertierung die andere Möglichkeit von **XLREF12** , **XLREF**, [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), die von der angegebene Verweis auf Bestandteil einer Excel 2007-Arbeitsblatt bezieht, die in früheren Versionen nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="882e4-116">In contrast, conversion the other way from **XLREF12** to **XLREF**, performed by [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), fails if the supplied reference refers to part of an Excel 2007 worksheet that is not supported in earlier versions.</span></span>
  
## <a name="example"></a><span data-ttu-id="882e4-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="882e4-117">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="882e4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="882e4-118">See also</span></span>



[<span data-ttu-id="882e4-119">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="882e4-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

