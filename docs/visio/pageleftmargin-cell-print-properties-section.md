---
title: Zelle "PageLeftMargin" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: Gibt den linken Rand der gedruckten Seite an.
ms.openlocfilehash: 289bd0bf16c6dcd9b26ec1a8c7920a29dab724a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334461"
---
# <a name="pageleftmargin-cell-print-properties-section"></a><span data-ttu-id="2eef5-103">Zelle "PageLeftMargin" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="2eef5-103">PageLeftMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="2eef5-104">Gibt den linken Rand der gedruckten Seite an.</span><span class="sxs-lookup"><span data-stu-id="2eef5-104">Specifies the margin on the left of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2eef5-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2eef5-105">Remarks</span></span>

<span data-ttu-id="2eef5-p101">Durch diesen Wert werden physische Einheiten dargestellt, und er wird weder durch Skalierung noch durch Zeichnungseinheiten beeinflusst. Wenn diese Zelle beispielsweise den Wert 0,25 cm aufweist, beträgt der Rand 0,25 Zentimeter, selbst wenn als Einheit der Seite Dezimeter angegeben werden. Wenn keine Einheiten explizit angegeben sind, ist die Standardeinstellung Seiteneinheiten.</span><span class="sxs-lookup"><span data-stu-id="2eef5-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="2eef5-109">Wenn Sie einen Verweis auf die Zelle PageLeftMargin aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2eef5-109">To get a reference to the PageLeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2eef5-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2eef5-110">Cell name:</span></span>  <br/> | <span data-ttu-id="2eef5-111">PageLeftMargin</span><span class="sxs-lookup"><span data-stu-id="2eef5-111">PageLeftMargin</span></span>  <br/> |
   
<span data-ttu-id="2eef5-112">Wenn Sie einen Verweis auf die Zelle PageLeftMargin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2eef5-112">To get a reference to the PageLeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2eef5-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2eef5-113">Section index:</span></span>  <br/> |<span data-ttu-id="2eef5-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2eef5-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2eef5-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2eef5-115">Row index:</span></span>  <br/> |<span data-ttu-id="2eef5-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="2eef5-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="2eef5-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2eef5-117">Cell index:</span></span>  <br/> |<span data-ttu-id="2eef5-118">**visPrintPropertiesLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="2eef5-118">**visPrintPropertiesLeftMargin**</span></span> <br/> |
   

