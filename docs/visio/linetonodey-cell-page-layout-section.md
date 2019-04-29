---
title: Zelle "LineToNodeY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251650
localization_priority: Normal
ms.assetid: 49d649e8-1603-192b-2984-e5d0b713da89
description: Legt den vertikalen Abstand zwischen sämtlichen Verbindern und Shapes auf dem Zeichenblatt fest.
ms.openlocfilehash: 2a5e4469fae2fb3142db2745f26c2009d42c0d2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432331"
---
# <a name="linetonodey-cell-page-layout-section"></a><span data-ttu-id="dfb20-103">Zelle "LineToNodeY" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="dfb20-103">LineToNodeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="dfb20-104">Legt den vertikalen Abstand zwischen sämtlichen Verbindern und Shapes auf dem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="dfb20-104">Determines the vertical clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfb20-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfb20-105">Remarks</span></span>

<span data-ttu-id="dfb20-p101">Sie können den Wert dieser Zelle auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, wählen Sie **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="dfb20-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="dfb20-108">Wenn Sie einen Verweis auf die Zelle Zelle LineToNodeY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dfb20-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dfb20-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dfb20-109">Cell name:</span></span>  <br/> | <span data-ttu-id="dfb20-110">Zelle LineToNodeY</span><span class="sxs-lookup"><span data-stu-id="dfb20-110">LineToNodeY</span></span>  <br/> |
   
<span data-ttu-id="dfb20-111">Wenn Sie einen Verweis auf die Zelle Zelle LineToNodeY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="dfb20-111">To get a reference to the LineToNodeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dfb20-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dfb20-112">Section index:</span></span>  <br/> |<span data-ttu-id="dfb20-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dfb20-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dfb20-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dfb20-114">Row index:</span></span>  <br/> |<span data-ttu-id="dfb20-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="dfb20-115">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="dfb20-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dfb20-116">Cell index:</span></span>  <br/> |<span data-ttu-id="dfb20-117">**visPLOLineToNodeY**</span><span class="sxs-lookup"><span data-stu-id="dfb20-117">**visPLOLineToNodeY**</span></span> <br/> |
   

