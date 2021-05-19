---
title: ISTHEMED Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Gibt einen booleschen Wert zurück, der angibt, ob auf ein Shape ein Design angewendet wurde.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418120"
---
# <a name="isthemed-function"></a><span data-ttu-id="596dd-103">ISTHEMED Function</span><span class="sxs-lookup"><span data-stu-id="596dd-103">ISTHEMED Function</span></span>

<span data-ttu-id="596dd-104">Gibt einen booleschen Wert zurück, der angibt, ob auf ein Shape ein Design angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="596dd-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="596dd-105">Informationen zur Version</span><span class="sxs-lookup"><span data-stu-id="596dd-105">Version Information</span></span>

<span data-ttu-id="596dd-106">Hinzugefügte Version: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="596dd-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="596dd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="596dd-107">Syntax</span></span>

 <span data-ttu-id="596dd-108">**ISTHEMED**()</span><span class="sxs-lookup"><span data-stu-id="596dd-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="596dd-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="596dd-109">Return value</span></span>

<span data-ttu-id="596dd-110">Boolesch</span><span class="sxs-lookup"><span data-stu-id="596dd-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="596dd-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="596dd-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="596dd-112">Die **ISTHEMED-Funktion** in Visio 2013 ersetzt die **CELLISTHEMED-Funktion** aus früheren Versionen Visio.</span><span class="sxs-lookup"><span data-stu-id="596dd-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="596dd-113">Mit **der ISTHEMED-Funktion** können Sie einem Shape entsprechende Teile der Formatierung eines Designs zuweisen, aber die Möglichkeit beibehalten, andere Teile der Designformatierung mit manuell angewendeter Formatierung zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="596dd-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="596dd-114">Wenn Sie das Design anschließend erneut anwenden, werden alle manuellen Formatierungen überschrieben, und die Form übernimmt alle Formatierungen des Designs.</span><span class="sxs-lookup"><span data-stu-id="596dd-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="596dd-115">**ISTHEMED wird** auf TRUE ausgewertet, wenn die [Zelle ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) in der Form größer als 0 ist.</span><span class="sxs-lookup"><span data-stu-id="596dd-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="596dd-116">Wenn diese Zelle gleich 0 ist, wird **ISTHEMED** als FALSE ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="596dd-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="596dd-117">Das Design von DocumentSheet und PageSheet hat keine Auswirkungen auf den Wert der **ISTHEMED-Funktion,** die in einem ShapeSheet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="596dd-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="596dd-118">Nur wenn die **ISTHEMED-Funktion** im PageSheet angezeigt wird, spielt das Design der Seite eine Rolle.</span><span class="sxs-lookup"><span data-stu-id="596dd-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="596dd-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="596dd-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="596dd-120">Cell</span><span class="sxs-lookup"><span data-stu-id="596dd-120">Cell</span></span>  <br/> |<span data-ttu-id="596dd-121">Formel</span><span class="sxs-lookup"><span data-stu-id="596dd-121">Formula</span></span>  <br/> |<span data-ttu-id="596dd-122">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="596dd-122">Result</span></span>  <br/> |
|<span data-ttu-id="596dd-123">Char.Font</span><span class="sxs-lookup"><span data-stu-id="596dd-123">Char.Font</span></span>  <br/> |<span data-ttu-id="596dd-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span><span class="sxs-lookup"><span data-stu-id="596dd-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="596dd-125">Wenn auf das Shape ein Designdesign angewendet wurde, akzeptiert der Formtext die Schriftartformatierung aus dem Design.</span><span class="sxs-lookup"><span data-stu-id="596dd-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="596dd-126">Wenn die Form nicht mit einem Bestimmten formatiert ist, wird der Formtext mit der Schriftart "Calibri" formatiert.</span><span class="sxs-lookup"><span data-stu-id="596dd-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="596dd-127">LineColor</span><span class="sxs-lookup"><span data-stu-id="596dd-127">LineColor</span></span>  <br/> |<span data-ttu-id="596dd-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="596dd-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="596dd-129">Wenn auf das Shape ein Gestaltungsschema angewendet wurde, ist die Linienfarbe des Shapes rot.</span><span class="sxs-lookup"><span data-stu-id="596dd-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="596dd-130">Wenn die Form nicht mit Einem -Shape-gefärbt ist, ist die Linienfarbe des Shapes grün.</span><span class="sxs-lookup"><span data-stu-id="596dd-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

