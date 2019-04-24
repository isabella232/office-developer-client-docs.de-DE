---
title: Zelle "LineToNodeX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm575
localization_priority: Normal
ms.assetid: 9d58e23e-b411-c5c1-b785-5014488d42c8
description: Legt den horizontalen Abstand zwischen sämtlichen Verbindern und Shapes auf dem Zeichenblatt fest.
ms.openlocfilehash: c5a27edb25ce7b1449ad6e2988027b474bd79fdb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358933"
---
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="5052f-103">Zelle "LineToNodeX" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="5052f-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="5052f-104">Legt den horizontalen Abstand zwischen sämtlichen Verbindern und Shapes auf dem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="5052f-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5052f-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5052f-105">Remarks</span></span>

<span data-ttu-id="5052f-p101">Sie können den Wert dieser Zelle auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, wählen Sie **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="5052f-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="5052f-108">Wenn Sie einen Verweis auf die Zelle Zelle LineToNodeY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5052f-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5052f-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5052f-109">Cell name:</span></span>  <br/> |<span data-ttu-id="5052f-110">Zelle LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="5052f-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="5052f-111">Wenn Sie einen Verweis auf die Zelle Zelle LineToNodeX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5052f-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5052f-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5052f-112">Section index:</span></span>  <br/> |<span data-ttu-id="5052f-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5052f-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5052f-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5052f-114">Row index:</span></span>  <br/> |<span data-ttu-id="5052f-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="5052f-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="5052f-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5052f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="5052f-117">**visPLOLineToNodeX**</span><span class="sxs-lookup"><span data-stu-id="5052f-117">**visPLOLineToNodeX**</span></span> <br/> |
   

