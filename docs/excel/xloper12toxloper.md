---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- xloper12toxloper-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790616"
---
# <a name="xloper12toxloper"></a><span data-ttu-id="28f94-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="28f94-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="28f94-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="28f94-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="28f94-106">Konvertierungsroutine zum Konvertieren von neuen **XLOPER12** in der alten **XLOPER**verwendet.</span><span class="sxs-lookup"><span data-stu-id="28f94-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="28f94-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="28f94-107">Parameters</span></span>

<span data-ttu-id="28f94-108">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="28f94-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="28f94-109">Zeiger auf die Quelle **XLOPER12** konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="28f94-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="28f94-110">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="28f94-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="28f94-111">Zeiger auf das Ziel **XLOPER** den konvertierten Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="28f94-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="28f94-112">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28f94-112">Property value/Return value</span></span>

<span data-ttu-id="28f94-113">**True,** Wenn **die Konvertierung erfolgreich; andernfalls** .</span><span class="sxs-lookup"><span data-stu-id="28f94-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="28f94-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28f94-114">Remarks</span></span>

<span data-ttu-id="28f94-115">Je nach Typ des **XLOPER12**weist diese Funktion einen neuen Speicherpuffer für für die konvertierten Werte, die auf das im Ziel **XLOPER**verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="28f94-115">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**.</span></span> <span data-ttu-id="28f94-116">Der Aufrufer ist verantwortlich für das Freigeben von Arbeitsspeicher die Kopie zugeordnet wird, wenn die Konvertierung erfolgreich ist; **FreeXLOperT** kann verwendet werden, oder kann direkt mithilfe von **kostenlose**erfolgen.</span><span class="sxs-lookup"><span data-stu-id="28f94-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="28f94-117">Wenn die Konvertierung fehlschlägt, muss der Anrufer nicht um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="28f94-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="28f94-118">Konvertierung von einem **XLOPER12** in einer **XLOPER** kann misslingen, wenn die **XLOPER12** enthält ein Array oder Verweis, der zu groß ist oder eine Zeichenfolge, die zu lang für die **XLOPER** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="28f94-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="28f94-119">**XLOPER12** Unicode-Breitzeichen-Zeichenfolgen werden in **XLOPER** ASCII-Byte-Zeichenfolgen in einer Weise d. h. Gebietsschema abhängigen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="28f94-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="28f94-120">Die **XLOPER12** **vom Typ XltypeInt** ist eine 32-Bit-Ganzzahl mit Vorzeichen, die **XLOPER** **vom Typ XltypeInt** eine 16-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="28f94-120">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer.</span></span> <span data-ttu-id="28f94-121">Bei einem angegebenen **XLOPER12** Integer ganze **XLOPER** überschreitet, wird die ganze Zahl in eine Double-8-Byte-Wert konvertiert und in ein **XLOPER** des Typs **XltypeNum**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="28f94-121">When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**.</span></span> <span data-ttu-id="28f94-122">Dies ist der einzige Fall, in dem diese Funktion den Typ des der konvertierten **XLOPER**ändert.</span><span class="sxs-lookup"><span data-stu-id="28f94-122">This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="28f94-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="28f94-123">Example</span></span>

<span data-ttu-id="28f94-124">Finden Sie in der Datei `\SAMPLES\FRAMEWRK\FRAMEWRK.C` für den Code für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="28f94-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="28f94-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28f94-125">See also</span></span>

- [<span data-ttu-id="28f94-126">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="28f94-126">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

