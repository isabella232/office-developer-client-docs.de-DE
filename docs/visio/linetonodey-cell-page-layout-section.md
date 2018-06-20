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
ms.openlocfilehash: bd5216a68abc4bcd8c3ef807b98280edb0ad29b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797340"
---
# <a name="linetonodey-cell-page-layout-section"></a><span data-ttu-id="51900-103">LineToNodeY Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="51900-103">LineToNodeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="51900-104">Legt den vertikalen Abstand zwischen sämtlichen Verbindern und Shapes auf dem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="51900-104">Determines the vertical clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51900-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51900-105">Remarks</span></span>

<span data-ttu-id="51900-106">Sie können den Wert dieser Zelle auch im Dialogfeld **Layout und Routing Abstand** festlegen.</span><span class="sxs-lookup"><span data-stu-id="51900-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="51900-107">(Klicken Sie auf der Registerkarte **Entwurf** klicken Sie auf den Pfeil neben **Seite einrichten** , klicken Sie auf **Layout und Routing**, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="51900-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="51900-108">Wenn Sie einen Verweis auf die Zelle LineToNodeY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="51900-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51900-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="51900-109">Cell name:</span></span>  <br/> | <span data-ttu-id="51900-110">LineToNodeY</span><span class="sxs-lookup"><span data-stu-id="51900-110">LineToNodeY</span></span>  <br/> |
   
<span data-ttu-id="51900-111">Wenn Sie einen Verweis auf die Zelle LineToNodeY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="51900-111">To get a reference to the LineToNodeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51900-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="51900-112">Section index:</span></span>  <br/> |<span data-ttu-id="51900-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="51900-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="51900-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="51900-114">Row index:</span></span>  <br/> |<span data-ttu-id="51900-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="51900-115">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="51900-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="51900-116">Cell index:</span></span>  <br/> |<span data-ttu-id="51900-117">**visPLOLineToNodeY**</span><span class="sxs-lookup"><span data-stu-id="51900-117">**visPLOLineToNodeY**</span></span> <br/> |
   

