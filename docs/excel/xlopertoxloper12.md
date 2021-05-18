---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- xlopertoxloper12-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404596"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="cb7a2-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="cb7a2-104">XLOperToXLOper12</span></span>

<span data-ttu-id="cb7a2-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cb7a2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cb7a2-106">Konvertierungsroutine, die zum Konvertieren von der alten **XLOPER** in die neue **XLOPER12 verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="cb7a2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb7a2-107">Parameters</span></span>

<span data-ttu-id="cb7a2-108">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="cb7a2-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="cb7a2-109">Zeiger auf die zu **konvertierte XLOPER-Quelle.**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="cb7a2-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="cb7a2-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="cb7a2-111">Zeiger auf das **Ziel XLOPER12,** um den konvertierten Wert zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="cb7a2-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="cb7a2-112">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb7a2-112">Property value/Return value</span></span>

<span data-ttu-id="cb7a2-113">**TRUE,** wenn die Konvertierung erfolgreich war, **andernfalls FALSE.**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cb7a2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cb7a2-114">Remarks</span></span>

<span data-ttu-id="cb7a2-115">Je nach Typ der **XLOPER** weist diese Funktion einen neuen Speicherpuffer für die konvertierten Werte zu, auf die im Ziel **XLOPER12 verwiesen wird.**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="cb7a2-116">Der Aufrufer ist dafür verantwortlich, alle der Kopie zugeordneten Arbeitsspeicher frei zu machen, wenn die Konvertierung erfolgreich war. **FreeXLOper12T** kann verwendet werden oder direkt mit kostenlosem **.**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="cb7a2-117">Wenn die Konvertierung fehlschlägt, muss der Aufrufer keinen Arbeitsspeicher freispeichern.</span><span class="sxs-lookup"><span data-stu-id="cb7a2-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="cb7a2-118">Im Allgemeinen ist eine Konvertierung von **xlOPER** in **xlOPER12** möglich.</span><span class="sxs-lookup"><span data-stu-id="cb7a2-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="cb7a2-119">Im Gegensatz dazu kann die Konvertierung von **xlOPER12** in einen **XLOPER** fehlschlagen, wenn der **XLOPER12** ein Array oder einen Verweis enthält, der zu groß oder eine Zeichenfolge ist, die zu lang ist, damit der **XLOPER** enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="cb7a2-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="cb7a2-120">**XLOPER** ASCII-Bytezeichenfolgen werden in xlOPER12-Unicode-Breitzeichenzeichenfolgen auf eine vom Locale abhängige Weise konvertiert. </span><span class="sxs-lookup"><span data-stu-id="cb7a2-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="cb7a2-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cb7a2-121">Example</span></span>

<span data-ttu-id="cb7a2-122">In der Datei  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` finden Sie den Code für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="cb7a2-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

