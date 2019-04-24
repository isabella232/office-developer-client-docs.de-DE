---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- convertxlref12toxlref-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 0a12052a93d030088feb548449955129ff5bdc0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311053"
---
# <a name="convertxlref12toxlref"></a><span data-ttu-id="ea0ca-104">ConvertXLRef12ToXLRef</span><span class="sxs-lookup"><span data-stu-id="ea0ca-104">ConvertXLRef12ToXLRef</span></span>

<span data-ttu-id="ea0ca-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ea0ca-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ea0ca-106">Versucht, ein **XLREF12** in ein **XLREF**zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="ea0ca-106">Tries to convert an **XLREF12** into an **XLREF**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a><span data-ttu-id="ea0ca-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea0ca-107">Parameters</span></span>

 <span data-ttu-id="ea0ca-108">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="ea0ca-108">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="ea0ca-109">Zeiger auf die Quellverweis Struktur.</span><span class="sxs-lookup"><span data-stu-id="ea0ca-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="ea0ca-110">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="ea0ca-110">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="ea0ca-111">Zeiger auf die Zielverweis Struktur, in die der konvertierte Wert eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea0ca-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ea0ca-112">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea0ca-112">Property value/Return value</span></span>

 <span data-ttu-id="ea0ca-113">**True** , wenn die Konvertierung erfolgreich war, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="ea0ca-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ea0ca-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea0ca-114">Remarks</span></span>

<span data-ttu-id="ea0ca-115">Die Konvertierung von **XLREF12** in **XLREF** schlägt fehl, wenn der angegebene Verweis auf einen Teil eines Excel 2007-Arbeitsblatts verweist, das in früheren Versionen nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ea0ca-115">The conversion from **XLREF12** to **XLREF** fails if the supplied reference refers to part of a Excel 2007 worksheet that is not supported in earlier versions.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ea0ca-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ea0ca-116">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="ea0ca-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea0ca-117">See also</span></span>



[<span data-ttu-id="ea0ca-118">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="ea0ca-118">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

