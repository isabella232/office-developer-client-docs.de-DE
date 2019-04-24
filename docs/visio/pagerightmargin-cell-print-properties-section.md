---
title: Zelle "PageRightMargin" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60062
localization_priority: Normal
ms.assetid: f864c759-ed94-8ab7-d664-cc04b3ed743e
description: Gibt den rechten Rand der gedruckten Seite an.
ms.openlocfilehash: d30669626fe07379521d61554010ae1bd7b0e83a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339494"
---
# <a name="pagerightmargin-cell-print-properties-section"></a><span data-ttu-id="d773e-103">Zelle "PageRightMargin" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="d773e-103">PageRightMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="d773e-104">Gibt den rechten Rand der gedruckten Seite an.</span><span class="sxs-lookup"><span data-stu-id="d773e-104">Specifies the margin on the right of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d773e-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d773e-105">Remarks</span></span>

<span data-ttu-id="d773e-p101">Durch diesen Wert werden physische Einheiten dargestellt, und er wird weder durch Skalierung noch durch Zeichnungseinheiten beeinflusst. Wenn diese Zelle beispielsweise den Wert 0,25 cm aufweist, beträgt der Rand 0,25 Zentimeter, selbst wenn als Einheit der Seite Dezimeter angegeben werden. Wenn keine Einheiten explizit angegeben sind, ist die Standardeinstellung Seiteneinheiten.</span><span class="sxs-lookup"><span data-stu-id="d773e-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="d773e-109">Wenn Sie einen Verweis auf die Zelle PageRightMargin aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d773e-109">To get a reference to the PageRightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d773e-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d773e-110">Cell name:</span></span>  <br/> | <span data-ttu-id="d773e-111">PageRightMargin</span><span class="sxs-lookup"><span data-stu-id="d773e-111">PageRightMargin</span></span>  <br/> |
   
<span data-ttu-id="d773e-112">Wenn Sie einen Verweis auf die Zelle PageRightMargin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d773e-112">To get a reference to the PageRightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d773e-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d773e-113">Section index:</span></span>  <br/> |<span data-ttu-id="d773e-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d773e-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d773e-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d773e-115">Row index:</span></span>  <br/> |<span data-ttu-id="d773e-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="d773e-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="d773e-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d773e-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d773e-118">**visPrintPropertiesRightMargin**</span><span class="sxs-lookup"><span data-stu-id="d773e-118">**visPrintPropertiesRightMargin**</span></span> <br/> |
   

