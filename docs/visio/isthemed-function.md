---
title: ISTHEMED Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Gibt einen Boolean-Wert zurück, der angibt, ob ein Shape ein Design angewendet wurde.
ms.openlocfilehash: 4311780d8686b5792e999c204ec182d23efb723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797269"
---
# <a name="isthemed-function"></a><span data-ttu-id="59faa-103">ISTHEMED Function</span><span class="sxs-lookup"><span data-stu-id="59faa-103">ISTHEMED Function</span></span>

<span data-ttu-id="59faa-104">Gibt einen Boolean-Wert zurück, der angibt, ob ein Shape ein Design angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="59faa-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="59faa-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="59faa-105">Version Information</span></span>

<span data-ttu-id="59faa-106">Hinzugefügte Version: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="59faa-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="59faa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="59faa-107">Syntax</span></span>

 <span data-ttu-id="59faa-108">**ISTHEMED** ()</span><span class="sxs-lookup"><span data-stu-id="59faa-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="59faa-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59faa-109">Return value</span></span>

<span data-ttu-id="59faa-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="59faa-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59faa-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59faa-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="59faa-112">Die Funktion **ISTHEMED** in Visio 2013 ersetzt die **CELLISTHEMED** -Funktion aus früheren Versionen von Visio.</span><span class="sxs-lookup"><span data-stu-id="59faa-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="59faa-113">Der **ISTHEMED** -Funktion, den Sie entsprechende Teile der Formatierung eines Designs auf eine Form zuweisen können jedoch die Möglichkeit, andere Teile des Designs mit Formatierung manuell angewendete Formatierung überschreiben beibehalten.</span><span class="sxs-lookup"><span data-stu-id="59faa-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="59faa-114">Wenn Sie das Design anschließend erneut anwenden, manuelle Formatierung überschrieben, und die Form übernimmt alle Formatierungen des Designs.</span><span class="sxs-lookup"><span data-stu-id="59faa-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="59faa-115">**ISTHEMED** ergibt True, wenn die Zelle [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) in der Form größer als 0 ist.</span><span class="sxs-lookup"><span data-stu-id="59faa-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="59faa-116">Wenn diese Zelle gleich 0 ist, berechnet **ISTHEMED** auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="59faa-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="59faa-117">Das Design der DocumentSheet und PageSheet hat keine Auswirkung auf den Wert der **ISTHEMED** -Funktion, die in einem ShapeSheet verwendet.</span><span class="sxs-lookup"><span data-stu-id="59faa-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="59faa-118">Nur, wenn die Funktion **ISTHEMED** in wird wird die PageSheet der Seite Design Frage.</span><span class="sxs-lookup"><span data-stu-id="59faa-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="59faa-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="59faa-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="59faa-120">Zelle</span><span class="sxs-lookup"><span data-stu-id="59faa-120">Cell</span></span>  <br/> |<span data-ttu-id="59faa-121">Formel</span><span class="sxs-lookup"><span data-stu-id="59faa-121">Formula</span></span>  <br/> |<span data-ttu-id="59faa-122">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="59faa-122">Result</span></span>  <br/> |
|<span data-ttu-id="59faa-123">Char.Font</span><span class="sxs-lookup"><span data-stu-id="59faa-123">Char.Font</span></span>  <br/> |<span data-ttu-id="59faa-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span><span class="sxs-lookup"><span data-stu-id="59faa-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="59faa-125">Wenn die Form ein entsprechendes mit Design versehenes angewendet hat, akzeptiert der Shape-Text die Formatierung aus dem Design Schriftart an.</span><span class="sxs-lookup"><span data-stu-id="59faa-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="59faa-126">Wenn das Shape kein entsprechendes mit Design versehenes ist, wird der Shape-Text mit der Schriftart "Calibri" formatiert.</span><span class="sxs-lookup"><span data-stu-id="59faa-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="59faa-127">LineColor</span><span class="sxs-lookup"><span data-stu-id="59faa-127">LineColor</span></span>  <br/> |<span data-ttu-id="59faa-128">IF (ISTHEMED, RGB (255, 0, 0), RGB (0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="59faa-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="59faa-129">Wenn die Form ein entsprechendes mit Design versehenes angewendet hat, ist das Shape die Farbe Rot.</span><span class="sxs-lookup"><span data-stu-id="59faa-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="59faa-130">Wenn das Shape kein entsprechendes mit Design versehenes ist, ist das Shape die Farbe Grün.</span><span class="sxs-lookup"><span data-stu-id="59faa-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

