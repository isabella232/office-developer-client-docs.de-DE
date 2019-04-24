---
title: Zelle "PageTopMargin" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
localization_priority: Normal
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: Gibt den oberen Rand der gedruckten Seite an.
ms.openlocfilehash: ff2bffffed39c5571386e792d2ffc8d20d6b291e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327363"
---
# <a name="pagetopmargin-cell-print-properties-section"></a><span data-ttu-id="807b4-103">Zelle "PageTopMargin" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="807b4-103">PageTopMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="807b4-104">Gibt den oberen Rand der gedruckten Seite an.</span><span class="sxs-lookup"><span data-stu-id="807b4-104">Specifies the margin at the top of the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="807b4-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="807b4-105">Remarks</span></span>

<span data-ttu-id="807b4-p101">Durch diesen Wert werden physische Einheiten dargestellt, und er wird weder durch Skalierung noch durch Zeichnungseinheiten beeinflusst. Wenn diese Zelle beispielsweise den Wert 0,25 cm aufweist, beträgt der Rand 0,25 Zentimeter, selbst wenn als Einheit der Seite Dezimeter angegeben werden. Wenn keine Einheiten explizit angegeben sind, ist die Standardeinstellung Seiteneinheiten.</span><span class="sxs-lookup"><span data-stu-id="807b4-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="807b4-109">Wenn Sie einen Verweis auf die Zelle PageTopMargin aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="807b4-109">To get a reference to the PageTopMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="807b4-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="807b4-110">Cell name:</span></span>  <br/> | <span data-ttu-id="807b4-111">PageTopMargin</span><span class="sxs-lookup"><span data-stu-id="807b4-111">PageTopMargin</span></span>  <br/> |
   
<span data-ttu-id="807b4-112">Wenn Sie einen Verweis auf die Zelle PageTopMargin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="807b4-112">To get a reference to the PageTopMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="807b4-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="807b4-113">Section index:</span></span>  <br/> |<span data-ttu-id="807b4-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="807b4-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="807b4-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="807b4-115">Row index:</span></span>  <br/> |<span data-ttu-id="807b4-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="807b4-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="807b4-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="807b4-117">Cell index:</span></span>  <br/> |<span data-ttu-id="807b4-118">**visPrintPropertiesTopMargin**</span><span class="sxs-lookup"><span data-stu-id="807b4-118">**visPrintPropertiesTopMargin**</span></span> <br/> |
   

