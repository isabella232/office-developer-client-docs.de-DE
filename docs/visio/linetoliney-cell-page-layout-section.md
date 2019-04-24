---
title: Zelle "LineToLineY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm570
localization_priority: Normal
ms.assetid: db9a8232-25c5-7087-2ae9-50470d0cf16e
description: Legt den vertikalen Abstand zwischen sämtlichen Verbindern auf dem Zeichenblatt fest.
ms.openlocfilehash: e98c3e05ffb1739f9b2739ce4e0ee8012afe2266
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358968"
---
# <a name="linetoliney-cell-page-layout-section"></a><span data-ttu-id="b8fb2-103">Zelle "LineToLineY" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="b8fb2-103">LineToLineY Cell (Page Layout Section)</span></span>

<span data-ttu-id="b8fb2-104">Legt den vertikalen Abstand zwischen sämtlichen Verbindern auf dem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="b8fb2-104">Determines the vertical clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b8fb2-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8fb2-105">Remarks</span></span>

<span data-ttu-id="b8fb2-p101">Sie können den Wert dieser Zelle auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, wählen Sie **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="b8fb2-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="b8fb2-108">Wenn Sie einen Verweis auf die Zelle Zelle LineToLineY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b8fb2-108">To get a reference to the LineToLineY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8fb2-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b8fb2-109">Cell name:</span></span>  <br/> |<span data-ttu-id="b8fb2-110">Zelle LineToLineY</span><span class="sxs-lookup"><span data-stu-id="b8fb2-110">LineToLineY</span></span>  <br/> |
   
<span data-ttu-id="b8fb2-111">Wenn Sie einen Verweis auf die Zelle Zelle LineToLineY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b8fb2-111">To get a reference to the LineToLineY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8fb2-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b8fb2-112">Section index:</span></span>  <br/> |<span data-ttu-id="b8fb2-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b8fb2-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b8fb2-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b8fb2-114">Row index:</span></span>  <br/> |<span data-ttu-id="b8fb2-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b8fb2-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b8fb2-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b8fb2-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b8fb2-117">**visPLOLineToLineY**</span><span class="sxs-lookup"><span data-stu-id="b8fb2-117">**visPLOLineToLineY**</span></span> <br/> |
   

