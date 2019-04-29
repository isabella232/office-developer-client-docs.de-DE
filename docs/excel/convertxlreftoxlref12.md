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
# <a name="convertxlreftoxlref12"></a><span data-ttu-id="f5e6b-104">ConvertXLRefToXLRef12</span><span class="sxs-lookup"><span data-stu-id="f5e6b-104">ConvertXLRefToXLRef12</span></span>

<span data-ttu-id="f5e6b-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f5e6b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f5e6b-106">Framework-Funktion, die versucht, ein **XLREF** in ein **XLREF12**zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="f5e6b-106">Framework function that attempts to convert an **XLREF** into an **XLREF12**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a><span data-ttu-id="f5e6b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5e6b-107">Parameters</span></span>

 <span data-ttu-id="f5e6b-108">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="f5e6b-108">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="f5e6b-109">Zeiger auf die Quellverweis Struktur.</span><span class="sxs-lookup"><span data-stu-id="f5e6b-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="f5e6b-110">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="f5e6b-110">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="f5e6b-111">Zeiger auf die Zielverweis Struktur, in die der konvertierte Wert eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5e6b-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f5e6b-112">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5e6b-112">Property value/Return value</span></span>

 <span data-ttu-id="f5e6b-113">**True** , wenn die Konvertierung erfolgreich war, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="f5e6b-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f5e6b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5e6b-114">Remarks</span></span>

<span data-ttu-id="f5e6b-115">Sofern die übergebene **XLREF** gültig ist, sollte dieser Vorgang immer erfolgreich sein.</span><span class="sxs-lookup"><span data-stu-id="f5e6b-115">Provided that the passed-in **XLREF** is valid, this operation should always be successful.</span></span> <span data-ttu-id="f5e6b-116">Im Gegensatz dazu schlägt die Konvertierung in die andere Richtung von **XLREF12** zu **XLREF**, die von [ConvertXLRef12ToXLRef](convertxlref12toxlref.md)ausgeführt wird, fehl, wenn der angegebene verweis auf einen Teil eines Excel 2007-Arbeitsblatts verweist, das in früheren Versionen nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f5e6b-116">In contrast, conversion the other way from **XLREF12** to **XLREF**, performed by [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), fails if the supplied reference refers to part of an Excel 2007 worksheet that is not supported in earlier versions.</span></span>
  
## <a name="example"></a><span data-ttu-id="f5e6b-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f5e6b-117">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="f5e6b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5e6b-118">See also</span></span>



[<span data-ttu-id="f5e6b-119">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="f5e6b-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

