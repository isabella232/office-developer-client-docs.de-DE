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
ms.openlocfilehash: 5219becdd1af888e424a2fe33faa7df5a06f61fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332606"
---
# <a name="about-error-values"></a><span data-ttu-id="58861-103">Informationen zu Fehlerwerten</span><span class="sxs-lookup"><span data-stu-id="58861-103">About Error Values</span></span>

<span data-ttu-id="58861-104">Fehlerwerte werden in Zellen angezeigt, bei denen falsche Formeln für diese Zelle angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="58861-104">Error values are displayed in cells that have incorrect formulas for that cell.</span></span>
  
<span data-ttu-id="58861-p101">Wenn eine Formel auf eine Zelle verweist, die einen Fehlerwert enthält, zeigt diese Formel ebenfalls einen Fehlerwert an. Sie können die Funktionen ISERR, ISERRNA, ISTFEHLER oder ISERROR verwenden, um nach Fehlerwerten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="58861-p101">If a formula references a cell that contains an error value, that formula also displays an error value. You can use the function ISERR, ISERRNA, ISERROR, or ISERRVALUE to look for error values.</span></span>
  
<span data-ttu-id="58861-107">**Fehlerwerte**</span><span class="sxs-lookup"><span data-stu-id="58861-107">**Error values**</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="58861-108">**Wenn die Zelle anzeigt**</span><span class="sxs-lookup"><span data-stu-id="58861-108">**If the cell displays**</span></span> <br/> |<span data-ttu-id="58861-109">**Formel enthält**</span><span class="sxs-lookup"><span data-stu-id="58861-109">**The formula includes**</span></span> <br/> |<span data-ttu-id="58861-110">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="58861-110">**Example**</span></span> <br/> |
| <span data-ttu-id="58861-111">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="58861-111">#DIV/0!</span></span>  <br/> |<span data-ttu-id="58861-112">Division durch 0</span><span class="sxs-lookup"><span data-stu-id="58861-112">Division by 0</span></span>  <br/> |<span data-ttu-id="58861-113">10/0</span><span class="sxs-lookup"><span data-stu-id="58861-113">10/0</span></span>  <br/> |
| <span data-ttu-id="58861-114">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="58861-114">#VALUE!</span></span>  <br/> | <span data-ttu-id="58861-115">Ein Argument oder Operand vom falschen Typ</span><span class="sxs-lookup"><span data-stu-id="58861-115">An argument or operand of the wrong type</span></span>  <br/> | <span data-ttu-id="58861-116">5 + "Haus"</span><span class="sxs-lookup"><span data-stu-id="58861-116">5 + "House"</span></span>  <br/> |
| <span data-ttu-id="58861-117">#REF!</span><span class="sxs-lookup"><span data-stu-id="58861-117">#REF!</span></span>  <br/> | <span data-ttu-id="58861-118">Ein Bezug auf eine nicht vorhandene Zelle</span><span class="sxs-lookup"><span data-stu-id="58861-118">A reference to a cell that does not exist</span></span>  <br/> | <span data-ttu-id="58861-119">Eine Zelle, die auf eine nicht mehr vorhandene Zelle verweist</span><span class="sxs-lookup"><span data-stu-id="58861-119">A cell that refers to another cell that no longer exists</span></span>  <br/> |
| <span data-ttu-id="58861-120">#NUM!</span><span class="sxs-lookup"><span data-stu-id="58861-120">#NUM!</span></span>  <br/> | <span data-ttu-id="58861-121">Eine ungültige Zahl</span><span class="sxs-lookup"><span data-stu-id="58861-121">An invalid number</span></span>  <br/> | <span data-ttu-id="58861-122">Quadratwurzel einer negativen Zahl</span><span class="sxs-lookup"><span data-stu-id="58861-122">Square root of a negative number</span></span>  <br/> |
| <span data-ttu-id="58861-123">#N/A!</span><span class="sxs-lookup"><span data-stu-id="58861-123">#N/A!</span></span>  <br/> | <span data-ttu-id="58861-124">Kein verfügbarer Wert</span><span class="sxs-lookup"><span data-stu-id="58861-124">Not an available value</span></span>  <br/> | <span data-ttu-id="58861-125">Funktion NA( )</span><span class="sxs-lookup"><span data-stu-id="58861-125">NA( ) function</span></span>  <br/> |
| <span data-ttu-id="58861-126">#DIM!</span><span class="sxs-lookup"><span data-stu-id="58861-126">#DIM!</span></span>  <br/> | <span data-ttu-id="58861-127">Ein dimensionaler Wert, der den Dimensions Umfang überschreitet (gültige Potenzen \<sind ganze \<Zahlen-128 = n = 127)</span><span class="sxs-lookup"><span data-stu-id="58861-127">A dimensional value that exceeds the dimension range (valid powers are integers -128 \<= n \<= 127)</span></span>  <br/> <span data-ttu-id="58861-128">Ein Bemaßungswert, der in einer nicht zulässigen Operation verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="58861-128">A dimensional value used with an inappropriate operation</span></span>  <br/> |<span data-ttu-id="58861-129">1In ^ 100 \* 1In ^ 100 (das Ergebnis ist 1In ^ 200, das sich jenseits des Dimensions befindet)</span><span class="sxs-lookup"><span data-stu-id="58861-129">1in^100 \* 1in^100 (the result is 1in^200, which is beyond the dimension range)</span></span>  <br/> <span data-ttu-id="58861-130">5,2cm^1,5 (ist keine ganzzahlige Potenz)</span><span class="sxs-lookup"><span data-stu-id="58861-130">5.2cm^1.5 (not an integer power)</span></span>  <br/> |
   

