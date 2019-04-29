---
title: Zelle "LineToLineX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm565
localization_priority: Normal
ms.assetid: f6b461fe-56ac-4c0e-31cd-6b3c1075db6e
description: Legt den horizontalen Abstand zwischen sämtlichen Verbindern auf dem Zeichenblatt fest.
ms.openlocfilehash: f3dbf43c737fef1fa1156fb4dc8d0f23449328c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416328"
---
# <a name="linetolinex-cell-page-layout-section"></a><span data-ttu-id="39430-103">Zelle "LineToLineX" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="39430-103">LineToLineX Cell (Page Layout Section)</span></span>

<span data-ttu-id="39430-104">Legt den horizontalen Abstand zwischen sämtlichen Verbindern auf dem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="39430-104">Determines the horizontal clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39430-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39430-105">Remarks</span></span>

<span data-ttu-id="39430-p101">Sie können den Wert dieser Zelle auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, wählen Sie **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="39430-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="39430-108">Wenn Sie einen Verweis auf die Zelle Zelle LineToLineX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="39430-108">To get a reference to the LineToLineX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39430-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="39430-109">Cell name:</span></span>  <br/> |<span data-ttu-id="39430-110">Zelle LineToLineX</span><span class="sxs-lookup"><span data-stu-id="39430-110">LineToLineX</span></span>  <br/> |
   
<span data-ttu-id="39430-111">Wenn Sie einen Verweis auf die Zelle Zelle LineToLineX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="39430-111">To get a reference to the LineToLineX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39430-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="39430-112">Section index:</span></span>  <br/> |<span data-ttu-id="39430-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="39430-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="39430-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="39430-114">Row index:</span></span>  <br/> |<span data-ttu-id="39430-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="39430-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="39430-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="39430-116">Cell index:</span></span>  <br/> |<span data-ttu-id="39430-117">**visPLOLineToLineX**</span><span class="sxs-lookup"><span data-stu-id="39430-117">**visPLOLineToLineX**</span></span> <br/> |
   

