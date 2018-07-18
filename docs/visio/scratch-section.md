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
ms.openlocfilehash: 16f0bac8f139c0b03d7826ac377a964d15296dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797976"
---
# <a name="scratch-section"></a><span data-ttu-id="d1399-103">Scratch-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d1399-103">Scratch Section</span></span>

<span data-ttu-id="d1399-104">Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1399-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1399-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1399-105">Remarks</span></span>

<span data-ttu-id="d1399-p101">Sie können diesen Abschnitt über das Dialogfeld **Abschnitt einfügen** hinzufügen. Klicken Sie mit der rechten Maustaste in das ShapeSheet-Fenster, und klicken Sie dann auf **Abschnitt einfügen**.</span><span class="sxs-lookup"><span data-stu-id="d1399-p101">You can add this section by using the **Insert Section** dialog box. Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="d1399-108">Im Abschnitt **"Scratch"** wird in der Regel wiederholte komplexe Berechnungen zu isolieren.</span><span class="sxs-lookup"><span data-stu-id="d1399-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="d1399-109">Wenn Ihre Lösung einen eindeutig definierten Zweck hat, ist es weiser eine Zelle im Abschnitt **User-Defined Cells** aus Gründen der Übersichtlichkeit verwendet werden, da benannt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1399-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="d1399-110">Zellen im Abschnitt **"Scratch"** verwenden Einheiten auf zwei verschiedene Arten.</span><span class="sxs-lookup"><span data-stu-id="d1399-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="d1399-111">Die Zellen X und Y verwenden Zeichnungseinheiten; Zellen a bis D verwenden keine Einheiten.</span><span class="sxs-lookup"><span data-stu-id="d1399-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="d1399-112">(Klicken Sie in der C-Programmierer benutzerdefinierten Desktops werden auch Zellen X und Y sind "typisiert" und Zellen A bis D sind "void".) Die Zellen **Scratch X** und **Y Scratch** werden häufig zum Ableiten von *x-* und *y -* Koordinaten wie **DrehbezX** und **DrehbezY**oder für die Zellen X und Y in einer Zelle der **Geometrie** -Abschnitt gefunden.</span><span class="sxs-lookup"><span data-stu-id="d1399-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="d1399-113">Entwurfszellen Sie A bis D alle Einheiten anzeigen, können Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="d1399-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="d1399-114">Ein weiterer Unterschied besteht die Möglichkeit, die diese Zellen Punktwerte zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d1399-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="d1399-115">Ein Punkt in Visio ist ein single-Paket für eine Koordinate ( *X, y*).</span><span class="sxs-lookup"><span data-stu-id="d1399-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="d1399-116">Wenn eine Formel einen Punktwert zurückgibt, wird dieser Wert in drei verschiedene Arten, abhängig von der ShapeSheet-Zelle interpretiert, die in die Formel ist.</span><span class="sxs-lookup"><span data-stu-id="d1399-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="d1399-117">Zellen, die auf *x* beziehen-Koordinaten (beispielsweise **DrehbezX**oder Zellen in der Spalte X von einem Abschnitt **"Geometry"** ) extrahiert nur die *X* -Teil einer Punktwert koordinieren.</span><span class="sxs-lookup"><span data-stu-id="d1399-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="d1399-118">Zellen, die sich, die *y beziehen* -Koordinaten extrahieren nur der *y* -Teil einer Punktwert koordinieren.</span><span class="sxs-lookup"><span data-stu-id="d1399-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="d1399-119">Visio extrahiert beispielsweise die Formel `PNT(3,4)` auf diese drei Arten.</span><span class="sxs-lookup"><span data-stu-id="d1399-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="d1399-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d1399-120">**Cell**</span></span>|<span data-ttu-id="d1399-121">**Eingabe**</span><span class="sxs-lookup"><span data-stu-id="d1399-121">**If you enter**</span></span>|<span data-ttu-id="d1399-122">**Behandlung durch Visio**</span><span class="sxs-lookup"><span data-stu-id="d1399-122">**Visio treats it as**</span></span>|<span data-ttu-id="d1399-123">**Ergebnis**</span><span class="sxs-lookup"><span data-stu-id="d1399-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d1399-124">X</span><span class="sxs-lookup"><span data-stu-id="d1399-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="d1399-125">3,0000 Zoll</span><span class="sxs-lookup"><span data-stu-id="d1399-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="d1399-126">Y</span><span class="sxs-lookup"><span data-stu-id="d1399-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="d1399-127">4,0000 Zoll</span><span class="sxs-lookup"><span data-stu-id="d1399-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="d1399-128">A-D</span><span class="sxs-lookup"><span data-stu-id="d1399-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="d1399-129">PNT (3.0000 Zoll, 4,0000 In.)</span><span class="sxs-lookup"><span data-stu-id="d1399-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

