---
title: Informationen zu Fehlerwerten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: Fehlerwerte werden in Zellen angezeigt, bei denen falsche Formeln für diese Zelle angegeben sind.
ms.openlocfilehash: 301f566151362727daf8236f8ca88fca8758054e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796352"
---
# <a name="about-error-values"></a><span data-ttu-id="368fa-103">Informationen zu Fehlerwerten</span><span class="sxs-lookup"><span data-stu-id="368fa-103">About Error Values</span></span>

<span data-ttu-id="368fa-104">Fehlerwerte werden in Zellen angezeigt, bei denen falsche Formeln für diese Zelle angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="368fa-104">Error values are displayed in cells that have incorrect formulas for that cell.</span></span>
  
<span data-ttu-id="368fa-p101">Wenn eine Formel auf eine Zelle verweist, die einen Fehlerwert enthält, zeigt diese Formel ebenfalls einen Fehlerwert an. Sie können die Funktionen ISERR, ISERRNA, ISTFEHLER oder ISERROR verwenden, um nach Fehlerwerten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="368fa-p101">If a formula references a cell that contains an error value, that formula also displays an error value. You can use the function ISERR, ISERRNA, ISERROR, or ISERRVALUE to look for error values.</span></span>
  
<span data-ttu-id="368fa-107">**Fehlerwerte**</span><span class="sxs-lookup"><span data-stu-id="368fa-107">**Error values**</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="368fa-108">**Wenn die Zelle anzeigt**</span><span class="sxs-lookup"><span data-stu-id="368fa-108">**If the cell displays**</span></span> <br/> |<span data-ttu-id="368fa-109">**Die Formel enthält.**</span><span class="sxs-lookup"><span data-stu-id="368fa-109">**The formula includes**</span></span> <br/> |<span data-ttu-id="368fa-110">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="368fa-110">**Example**</span></span> <br/> |
| <span data-ttu-id="368fa-111">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="368fa-111">#DIV/0!</span></span>  <br/> |<span data-ttu-id="368fa-112">Division durch 0</span><span class="sxs-lookup"><span data-stu-id="368fa-112">Division by 0</span></span>  <br/> |<span data-ttu-id="368fa-113">10/0</span><span class="sxs-lookup"><span data-stu-id="368fa-113">10/0</span></span>  <br/> |
| <span data-ttu-id="368fa-114">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="368fa-114">#VALUE!</span></span>  <br/> | <span data-ttu-id="368fa-115">Ein Argument oder Operand vom falschen Typ</span><span class="sxs-lookup"><span data-stu-id="368fa-115">An argument or operand of the wrong type</span></span>  <br/> | <span data-ttu-id="368fa-116">5 + "Hütte"</span><span class="sxs-lookup"><span data-stu-id="368fa-116">5 + "House"</span></span>  <br/> |
| <span data-ttu-id="368fa-117">#REF!</span><span class="sxs-lookup"><span data-stu-id="368fa-117">#REF!</span></span>  <br/> | <span data-ttu-id="368fa-118">Ein Verweis auf eine Zelle, die nicht vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="368fa-118">A reference to a cell that does not exist</span></span>  <br/> | <span data-ttu-id="368fa-119">Eine Zelle, die in eine andere Zelle verweist, die nicht mehr vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="368fa-119">A cell that refers to another cell that no longer exists</span></span>  <br/> |
| <span data-ttu-id="368fa-120">#NUM!</span><span class="sxs-lookup"><span data-stu-id="368fa-120">#NUM!</span></span>  <br/> | <span data-ttu-id="368fa-121">Eine ungültige Zahl</span><span class="sxs-lookup"><span data-stu-id="368fa-121">An invalid number</span></span>  <br/> | <span data-ttu-id="368fa-122">Quadratwurzel einer negativen Zahl</span><span class="sxs-lookup"><span data-stu-id="368fa-122">Square root of a negative number</span></span>  <br/> |
| <span data-ttu-id="368fa-123">#N/V!</span><span class="sxs-lookup"><span data-stu-id="368fa-123">#N/A!</span></span>  <br/> | <span data-ttu-id="368fa-124">Kein verfügbaren Wert</span><span class="sxs-lookup"><span data-stu-id="368fa-124">Not an available value</span></span>  <br/> | <span data-ttu-id="368fa-125">Funktion NA)</span><span class="sxs-lookup"><span data-stu-id="368fa-125">NA( ) function</span></span>  <br/> |
| <span data-ttu-id="368fa-126">#DIM!</span><span class="sxs-lookup"><span data-stu-id="368fa-126">#DIM!</span></span>  <br/> | <span data-ttu-id="368fa-127">Ein dimensionaler Wert, der den Bemaßungsbereich überschreitet (gültige Potenzen sind Ganzzahlen-128 \<n = \<= 127)</span><span class="sxs-lookup"><span data-stu-id="368fa-127">A dimensional value that exceeds the dimension range (valid powers are integers -128 \<= n \<= 127)</span></span>  <br/> <span data-ttu-id="368fa-128">Ein dimensionaler Wert, der mit einem Vorgang ungeeignetes verwendet</span><span class="sxs-lookup"><span data-stu-id="368fa-128">A dimensional value used with an inappropriate operation</span></span>  <br/> |<span data-ttu-id="368fa-129">1In ^ 100 \* 1In ^ 100 (das Ergebnis ist 1In ^ 200 und liegt außerhalb des Bemaßungsbereichs)</span><span class="sxs-lookup"><span data-stu-id="368fa-129">1in^100 \* 1in^100 (the result is 1in^200, which is beyond the dimension range)</span></span>  <br/> <span data-ttu-id="368fa-130">5, 2 cm ^ 1,5 (ist keine ganzzahlige Potenz)</span><span class="sxs-lookup"><span data-stu-id="368fa-130">5.2cm^1.5 (not an integer power)</span></span>  <br/> |
   

