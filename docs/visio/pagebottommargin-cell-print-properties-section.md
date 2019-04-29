---
title: Zelle "PageBottomMargin" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Gibt den unteren Rand der gedruckten Seite an.
ms.openlocfilehash: f546d89b8761c6c1b7340af69d2b48f16c180767
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438596"
---
# <a name="pagebottommargin-cell-print-properties-section"></a><span data-ttu-id="f41bb-103">Zelle "PageBottomMargin" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="f41bb-103">PageBottomMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="f41bb-104">Gibt den unteren Rand der gedruckten Seite an.</span><span class="sxs-lookup"><span data-stu-id="f41bb-104">Specifies the margin at the bottom of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f41bb-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f41bb-105">Remarks</span></span>

<span data-ttu-id="f41bb-p101">Durch diesen Wert werden physische Einheiten dargestellt, und er wird weder durch Skalierung noch durch Zeichnungseinheiten beeinflusst. Wenn diese Zelle beispielsweise den Wert 0,5 cm aufweist, beträgt der Rand 0,5 Zentimeter, selbst wenn als Einheit der Seite Dezimeter angegeben werden. Wenn keine Einheiten explizit angegeben sind, ist die Standardeinstellung Seiteneinheiten.</span><span class="sxs-lookup"><span data-stu-id="f41bb-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.5 in., this margin is 0.5 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="f41bb-109">Wenn Sie einen Verweis auf die Zelle PageBottomMargin aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f41bb-109">To get a reference to the PageBottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f41bb-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f41bb-110">Cell name:</span></span>  <br/> | <span data-ttu-id="f41bb-111">PageBottomMargin</span><span class="sxs-lookup"><span data-stu-id="f41bb-111">PageBottomMargin</span></span>  <br/> |
   
<span data-ttu-id="f41bb-112">Wenn Sie einen Verweis auf die Zelle PageBottomMargin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f41bb-112">To get a reference to the PageBottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f41bb-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f41bb-113">Section index:</span></span>  <br/> |<span data-ttu-id="f41bb-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f41bb-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f41bb-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f41bb-115">Row index:</span></span>  <br/> |<span data-ttu-id="f41bb-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="f41bb-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="f41bb-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f41bb-117">Cell index:</span></span>  <br/> |<span data-ttu-id="f41bb-118">**visPrintPropertiesBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="f41bb-118">**visPrintPropertiesBottomMargin**</span></span> <br/> |
   

