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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358954"
---
# <a name="linetolinex-cell-page-layout-section"></a><span data-ttu-id="30bfa-103">Zelle "LineToLineX" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="30bfa-103">LineToLineX Cell (Page Layout Section)</span></span>

<span data-ttu-id="30bfa-104">Legt den horizontalen Abstand zwischen sämtlichen Verbindern auf dem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="30bfa-104">Determines the horizontal clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30bfa-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30bfa-105">Remarks</span></span>

<span data-ttu-id="30bfa-p101">Sie können den Wert dieser Zelle auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, wählen Sie **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="30bfa-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="30bfa-108">Wenn Sie einen Verweis auf die Zelle Zelle LineToLineX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="30bfa-108">To get a reference to the LineToLineX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30bfa-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="30bfa-109">Cell name:</span></span>  <br/> |<span data-ttu-id="30bfa-110">Zelle LineToLineX</span><span class="sxs-lookup"><span data-stu-id="30bfa-110">LineToLineX</span></span>  <br/> |
   
<span data-ttu-id="30bfa-111">Wenn Sie einen Verweis auf die Zelle Zelle LineToLineX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="30bfa-111">To get a reference to the LineToLineX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30bfa-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="30bfa-112">Section index:</span></span>  <br/> |<span data-ttu-id="30bfa-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="30bfa-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="30bfa-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="30bfa-114">Row index:</span></span>  <br/> |<span data-ttu-id="30bfa-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="30bfa-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="30bfa-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="30bfa-116">Cell index:</span></span>  <br/> |<span data-ttu-id="30bfa-117">**visPLOLineToLineX**</span><span class="sxs-lookup"><span data-stu-id="30bfa-117">**visPLOLineToLineX**</span></span> <br/> |
   

