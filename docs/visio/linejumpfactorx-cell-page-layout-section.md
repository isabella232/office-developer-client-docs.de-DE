---
title: Zelle "LineJumpFactorX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
localization_priority: Normal
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: Bestimmt die Größe von Liniensprüngen auf horizontalen dynamischen Verbindern auf dem Zeichenblatt, und zwar relativ zum Wert der Zelle LineToLineX. Der Wert dieser Zelle kann im Bereich zwischen 0 und 10 liegen, jedoch sind Bruchwerte zwischen 0 und 1 empfehlenswert.
ms.openlocfilehash: 8698d99021ca64415417de8e946cbd80b586e759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424994"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a><span data-ttu-id="089a7-104">Zelle "LineJumpFactorX" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="089a7-104">LineJumpFactorX Cell (Page Layout Section)</span></span>

<span data-ttu-id="089a7-p102">Bestimmt die Größe von Liniensprüngen auf horizontalen dynamischen Verbindern auf dem Zeichenblatt, und zwar relativ zum Wert der Zelle LineToLineX. Der Wert dieser Zelle kann im Bereich zwischen 0 und 10 liegen, jedoch sind Bruchwerte zwischen 0 und 1 empfehlenswert.</span><span class="sxs-lookup"><span data-stu-id="089a7-p102">Determines the size of line jumps on horizontal dynamic connectors on the page, relative to the value of the LineToLineX cell. The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="089a7-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="089a7-107">Remarks</span></span>

<span data-ttu-id="089a7-108">Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).</span><span class="sxs-lookup"><span data-stu-id="089a7-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="089a7-109">Um einen Verweis auf die LineJumpFactorX-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="089a7-109">To get a reference to the LineJumpFactorX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="089a7-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="089a7-110">Cell name:</span></span>  <br/> |<span data-ttu-id="089a7-111">LineJumpFactorX</span><span class="sxs-lookup"><span data-stu-id="089a7-111">LineJumpFactorX</span></span>  <br/> |
   
<span data-ttu-id="089a7-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LineJumpFactorX-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="089a7-112">To get a reference to the LineJumpFactorX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="089a7-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="089a7-113">Section index:</span></span>  <br/> |<span data-ttu-id="089a7-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="089a7-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="089a7-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="089a7-115">Row index:</span></span>  <br/> |<span data-ttu-id="089a7-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="089a7-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="089a7-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="089a7-117">Cell index:</span></span>  <br/> |<span data-ttu-id="089a7-118">**visPLOJumpFactorX**</span><span class="sxs-lookup"><span data-stu-id="089a7-118">**visPLOJumpFactorX**</span></span> <br/> |
   

