---
title: ISTHEMED Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Gibt einen booleschen Wert zurück, der angibt, ob auf eine Form ein Design angewendet wurde.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418120"
---
# <a name="isthemed-function"></a><span data-ttu-id="46e3e-103">ISTHEMED Function</span><span class="sxs-lookup"><span data-stu-id="46e3e-103">ISTHEMED Function</span></span>

<span data-ttu-id="46e3e-104">Gibt einen booleschen Wert zurück, der angibt, ob auf eine Form ein Design angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="46e3e-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="46e3e-105">Informationen zur Version</span><span class="sxs-lookup"><span data-stu-id="46e3e-105">Version Information</span></span>

<span data-ttu-id="46e3e-106">Hinzugefügte Version: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="46e3e-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="46e3e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e3e-107">Syntax</span></span>

 <span data-ttu-id="46e3e-108">\*\*\*\* Isthemed ()</span><span class="sxs-lookup"><span data-stu-id="46e3e-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="46e3e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46e3e-109">Return value</span></span>

<span data-ttu-id="46e3e-110">Boolesch</span><span class="sxs-lookup"><span data-stu-id="46e3e-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46e3e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46e3e-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="46e3e-112">Die \*\*\*\* isdesigned-Funktion in Visio 2013 ersetzt die **CELLISTHEMED** -Funktion aus früheren Versionen von Visio.</span><span class="sxs-lookup"><span data-stu-id="46e3e-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="46e3e-113">Mit \*\*\*\* der isthemed-Funktion können Sie die entsprechenden Teile der Formatierung eines Designs einem Shape zuweisen, aber die Möglichkeit, andere Bereiche der Designformatierung mit manuell angewendeten Formatierungen außer Kraft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="46e3e-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="46e3e-114">Wenn Sie das Design anschließend erneut anwenden, werden alle manuellen Formatierungen außer Kraft gesetzt, und die Form übernimmt alle Formatierungen des Designs.</span><span class="sxs-lookup"><span data-stu-id="46e3e-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="46e3e-115">\*\*\*\* Isdesigned ergibt true, wenn die [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) -Zelle in der Form größer als 0 ist.</span><span class="sxs-lookup"><span data-stu-id="46e3e-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="46e3e-116">Wenn diese Zelle gleich 0 ist, wird isdesigned als FALSE ausgewertet. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="46e3e-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="46e3e-117">Das Design von DocumentSheet und PageSheet hat keinen Einfluss auf den Wert der \*\*\*\* isthemed-Funktion, die in einem ShapeSheet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46e3e-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="46e3e-118">Nur wenn die \*\*\*\* isthemed-Funktion in der PageSheet angezeigt wird, ist das Design der Seite wichtig.</span><span class="sxs-lookup"><span data-stu-id="46e3e-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="46e3e-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="46e3e-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="46e3e-120">Cell</span><span class="sxs-lookup"><span data-stu-id="46e3e-120">Cell</span></span>  <br/> |<span data-ttu-id="46e3e-121">Formel</span><span class="sxs-lookup"><span data-stu-id="46e3e-121">Formula</span></span>  <br/> |<span data-ttu-id="46e3e-122">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="46e3e-122">Result</span></span>  <br/> |
|<span data-ttu-id="46e3e-123">Char. Font</span><span class="sxs-lookup"><span data-stu-id="46e3e-123">Char.Font</span></span>  <br/> |<span data-ttu-id="46e3e-124">IF (isdesigned (), THEMEVAL (), FONT ("Calibri")))</span><span class="sxs-lookup"><span data-stu-id="46e3e-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="46e3e-125">Wenn auf die Form ein Design angewendet wird, akzeptiert der Shape-Text die Schriftartenformatierung des Designs.</span><span class="sxs-lookup"><span data-stu-id="46e3e-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="46e3e-126">Wenn es sich nicht um ein Design handelt, wird der Shape-Text mit der Schriftart "Calibri" formatiert.</span><span class="sxs-lookup"><span data-stu-id="46e3e-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="46e3e-127">Zelle LineColor</span><span class="sxs-lookup"><span data-stu-id="46e3e-127">LineColor</span></span>  <br/> |<span data-ttu-id="46e3e-128">IF (ISDESIGNED, RGB (255, 0, 0), RGB (0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="46e3e-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="46e3e-129">Wenn auf die Form ein Design angewendet wird, ist die Linienfarbe des Shapes rot.</span><span class="sxs-lookup"><span data-stu-id="46e3e-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="46e3e-130">Wenn es sich nicht um ein Design handelt, ist die Linienfarbe der Form grün.</span><span class="sxs-lookup"><span data-stu-id="46e3e-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

