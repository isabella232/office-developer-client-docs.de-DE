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
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790631"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="2cf90-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="2cf90-104">XLOperToXLOper12</span></span>

<span data-ttu-id="2cf90-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2cf90-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2cf90-106">Konvertierungsroutine zum Konvertieren von der alten **XLOPER** in die neue **XLOPER12**verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cf90-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="2cf90-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cf90-107">Parameters</span></span>

<span data-ttu-id="2cf90-108">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="2cf90-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="2cf90-109">Zeiger auf die Quelle **XLOPER** konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cf90-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="2cf90-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="2cf90-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="2cf90-111">Zeiger auf das Ziel **XLOPER12** den konvertierten Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="2cf90-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2cf90-112">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cf90-112">Property value/Return value</span></span>

<span data-ttu-id="2cf90-113">**True,** Wenn **die Konvertierung erfolgreich; andernfalls** .</span><span class="sxs-lookup"><span data-stu-id="2cf90-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2cf90-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2cf90-114">Remarks</span></span>

<span data-ttu-id="2cf90-115">Je nach Typ des der **XLOPER**weist diese Funktion einen neuer Speicherpuffer für die konvertierten Werte, die auf das im Ziel **XLOPER12**verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="2cf90-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="2cf90-116">Der Aufrufer ist verantwortlich für das Freigeben von Arbeitsspeicher die Kopie zugeordnet wird, wenn die Konvertierung erfolgreich ist; **FreeXLOper12T** kann verwendet werden, oder es kann direkt mit **kostenlose**ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2cf90-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="2cf90-117">Wenn die Konvertierung fehlschlägt, muss der Anrufer nicht um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2cf90-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="2cf90-118">Im Allgemeinen ist die Konvertierung von jeder **XLOPER** in einer **XLOPER12** möglich.</span><span class="sxs-lookup"><span data-stu-id="2cf90-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="2cf90-119">Im Gegensatz dazu kann Konvertierung von einem **XLOPER12** in einer **XLOPER** misslingen, wenn die **XLOPER12** enthält ein Array oder Verweis, der zu groß ist oder eine Zeichenfolge, die zu lang für die **XLOPER** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2cf90-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="2cf90-120">**XLOPER** ASCII-Byte-Zeichenfolgen werden in Unicode **XLOPER12** Breitzeichen-Zeichenfolgen in einer Weise konvertiert, die Gebietsschema abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="2cf90-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="2cf90-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2cf90-121">Example</span></span>

<span data-ttu-id="2cf90-122">Finden Sie in der Datei `\SAMPLES\FRAMEWRK\FRAMEWRK.C` für den Code für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="2cf90-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

