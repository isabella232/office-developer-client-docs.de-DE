---
title: Abschnitt "Scratch"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
localization_priority: Normal
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
description: Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.
ms.openlocfilehash: a7d2c6762e96fc19986521c2ba164666b925c928
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344527"
---
# <a name="scratch-section"></a><span data-ttu-id="a725b-103">Abschnitt "Scratch"</span><span class="sxs-lookup"><span data-stu-id="a725b-103">Scratch Section</span></span>

<span data-ttu-id="a725b-104">Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a725b-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a725b-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a725b-105">Remarks</span></span>

<span data-ttu-id="a725b-p101">Sie können diesen Abschnitt über das Dialogfeld **Abschnitt einfügen** hinzufügen. Klicken Sie mit der rechten Maustaste in das ShapeSheet-Fenster, und klicken Sie dann auf **Abschnitt einfügen**.</span><span class="sxs-lookup"><span data-stu-id="a725b-p101">You can add this section by using the **Insert Section** dialog box. Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="a725b-108">Der Abschnitt **Scratch** wird in der Regel verwendet, um wiederholte komplexe Berechnungen zu isolieren.</span><span class="sxs-lookup"><span data-stu-id="a725b-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="a725b-109">Wenn Ihre Lösung einen genau definierten Zweck hat, ist es klüger, eine Zelle im Abschnitt **benutzerdefinierte Zellen** zur besseren Übersichtlichkeit zu verwenden, da Benutzer Zellen benannt werden können.</span><span class="sxs-lookup"><span data-stu-id="a725b-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="a725b-110">Zellen im **Scratch** -Abschnitt verwenden Einheiten auf zwei verschiedene Arten.</span><span class="sxs-lookup"><span data-stu-id="a725b-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="a725b-111">X-und Y-Zellen verwenden Zeichnungseinheiten; A bis D-Zellen verwenden keine Einheiten.</span><span class="sxs-lookup"><span data-stu-id="a725b-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="a725b-112">(Im Jargon von C-Programmierern werden die Zellen X und Y "typisiert", und die Zellen A bis D sind "void"). Die \*\*\*\* x-und **Scratch y** -Zellen werden häufig zum Ableiten von *x-* und *y-* Koordinaten, wie **PinX** und **PinY**, oder den x-und y-Zellen in einer **Geometry** -Abschnitts Zelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="a725b-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="a725b-113">Kratzer Zellen A bis D können anzeigen, welche Einheiten Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="a725b-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="a725b-114">Ein weiterer Unterschied ist die Art und Weise, in der diese Zellen Punktwerte speichern.</span><span class="sxs-lookup"><span data-stu-id="a725b-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="a725b-115">Ein Punkt in Visio ist ein einzelnes Datenpaket für eine ( *x, y*)-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="a725b-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="a725b-116">Wenn eine Formel einen Point-Wert zurückgibt, wird dieser Wert auf eine von drei Arten interpretiert, abhängig von der ShapeSheet-Zelle, in der sich die Formel befindet.</span><span class="sxs-lookup"><span data-stu-id="a725b-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="a725b-117">Zellen, die sich auf *x* -Koordinaten beziehen (beispielsweise **PinX**oder Zellen in der Spalte x eines **Geometry** -Abschnitts) extrahieren nur den *x* -Koordinate-Teil eines Punktwerts.</span><span class="sxs-lookup"><span data-stu-id="a725b-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="a725b-118">Zellen, die sich auf *y* -Koordinaten beziehen, extrahieren nur den *y* -Koordinaten Teil eines Punktwerts.</span><span class="sxs-lookup"><span data-stu-id="a725b-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="a725b-119">Visio extrahiert die Formel `PNT(3,4)` beispielsweise auf drei Arten.</span><span class="sxs-lookup"><span data-stu-id="a725b-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="a725b-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="a725b-120">**Cell**</span></span>|<span data-ttu-id="a725b-121">**Eingabe**</span><span class="sxs-lookup"><span data-stu-id="a725b-121">**If you enter**</span></span>|<span data-ttu-id="a725b-122">**Behandlung durch Visio**</span><span class="sxs-lookup"><span data-stu-id="a725b-122">**Visio treats it as**</span></span>|<span data-ttu-id="a725b-123">**Ergebnis**</span><span class="sxs-lookup"><span data-stu-id="a725b-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a725b-124">X</span><span class="sxs-lookup"><span data-stu-id="a725b-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="a725b-125">3,0000 Zoll</span><span class="sxs-lookup"><span data-stu-id="a725b-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="a725b-126">v</span><span class="sxs-lookup"><span data-stu-id="a725b-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="a725b-127">4,0000 Zoll</span><span class="sxs-lookup"><span data-stu-id="a725b-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="a725b-128">A-D</span><span class="sxs-lookup"><span data-stu-id="a725b-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="a725b-129">PNT (3.0000 in., 4,0000 in.)</span><span class="sxs-lookup"><span data-stu-id="a725b-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

