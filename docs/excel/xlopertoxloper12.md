---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- xlopertoxloper12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303906"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="7f071-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="7f071-104">XLOperToXLOper12</span></span>

<span data-ttu-id="7f071-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7f071-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7f071-106">Konvertierungsroutine, die zum Konvertieren vom alten **XLOPER** in den neuen **XLOPER12**verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f071-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="7f071-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f071-107">Parameters</span></span>

<span data-ttu-id="7f071-108">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="7f071-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="7f071-109">Zeiger auf den zu konvertierenden Quell- **XLOPER** .</span><span class="sxs-lookup"><span data-stu-id="7f071-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="7f071-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="7f071-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="7f071-111">Zeiger auf die Ziel- **XLOPER12** , die den konvertierten Wert enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="7f071-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="7f071-112">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f071-112">Property value/Return value</span></span>

<span data-ttu-id="7f071-113">**True** , wenn die Konvertierung erfolgreich war, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="7f071-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7f071-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f071-114">Remarks</span></span>

<span data-ttu-id="7f071-115">Je nach Typ des **XLOPER**weist diese Funktion einen neuen Speicherpuffer für die konvertierten Werte zu, auf die im Ziel **XLOPER12**verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7f071-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="7f071-116">Der Aufrufer ist für das Freigeben von Speicher für die Kopie verantwortlich, wenn die Konvertierung erfolgreich ist; **FreeXLOper12T** kann verwendet werden, oder es kann direkt mit **Free**durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7f071-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="7f071-117">Wenn die Konvertierung fehlschlägt, muss der Aufrufer keinen Arbeitsspeicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="7f071-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="7f071-118">Im Allgemeinen ist die Konvertierung von einem **XLOPER** in ein **XLOPER12** möglich.</span><span class="sxs-lookup"><span data-stu-id="7f071-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="7f071-119">Im Gegensatz dazu kann die Konvertierung von einer **XLOPER12** in eine **XLOPER** fehlschlagen, wenn die **XLOPER12** ein Array oder einen Verweis enthält, der zu lang ist, oder eine Zeichenfolge, die zu lange für die **XLOPER** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7f071-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="7f071-120">**XLOPER** ASCII-Byte Zeichenfolgen werden in **XLOPER12** -Unicode-Breitzeichen Zeichenfolgen in einer gebietsschemaabhängigen Form konvertiert.</span><span class="sxs-lookup"><span data-stu-id="7f071-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="7f071-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7f071-121">Example</span></span>

<span data-ttu-id="7f071-122">Sehen Sie sich `\SAMPLES\FRAMEWRK\FRAMEWRK.C` die Datei für den Code für diese Funktion an.</span><span class="sxs-lookup"><span data-stu-id="7f071-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

