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
ms.openlocfilehash: 75f7e8150711421138a01175be34003d124e88ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797341"
---
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="87084-103">LineToNodeX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="87084-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="87084-104">Legt den horizontalen Abstand zwischen sämtlichen Verbindern und Shapes auf dem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="87084-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="87084-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87084-105">Remarks</span></span>

<span data-ttu-id="87084-106">Sie können den Wert dieser Zelle auch im Dialogfeld **Layout und Routing Abstand** festlegen.</span><span class="sxs-lookup"><span data-stu-id="87084-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="87084-107">(Klicken Sie auf der Registerkarte **Entwurf** klicken Sie auf den Pfeil neben **Seite einrichten** , klicken Sie auf **Layout und Routing**, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="87084-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="87084-108">Wenn Sie einen Verweis auf die Zelle LineToNodeY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="87084-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87084-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="87084-109">Cell name:</span></span>  <br/> |<span data-ttu-id="87084-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="87084-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="87084-111">Wenn Sie einen Verweis auf die Zelle LineToNodeX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="87084-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87084-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="87084-112">Section index:</span></span>  <br/> |<span data-ttu-id="87084-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="87084-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="87084-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="87084-114">Row index:</span></span>  <br/> |<span data-ttu-id="87084-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="87084-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="87084-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="87084-116">Cell index:</span></span>  <br/> |<span data-ttu-id="87084-117">**visPLOLineToNodeX**</span><span class="sxs-lookup"><span data-stu-id="87084-117">**visPLOLineToNodeX**</span></span> <br/> |
   

