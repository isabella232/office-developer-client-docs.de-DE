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
ms.openlocfilehash: fb6205407070485a0e234ee594e84979bca40891
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797320"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a><span data-ttu-id="5c4a4-104">LineJumpFactorX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="5c4a4-104">LineJumpFactorX Cell (Page Layout Section)</span></span>

<span data-ttu-id="5c4a4-p102">Bestimmt die Größe von Liniensprüngen auf horizontalen dynamischen Verbindern auf dem Zeichenblatt, und zwar relativ zum Wert der Zelle LineToLineX. Der Wert dieser Zelle kann im Bereich zwischen 0 und 10 liegen, jedoch sind Bruchwerte zwischen 0 und 1 empfehlenswert.</span><span class="sxs-lookup"><span data-stu-id="5c4a4-p102">Determines the size of line jumps on horizontal dynamic connectors on the page, relative to the value of the LineToLineX cell. The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c4a4-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c4a4-107">Remarks</span></span>

<span data-ttu-id="5c4a4-108">Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).</span><span class="sxs-lookup"><span data-stu-id="5c4a4-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="5c4a4-109">Wenn Sie einen Verweis auf die Zelle LineJumpFactorX aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5c4a4-109">To get a reference to the LineJumpFactorX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c4a4-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5c4a4-110">Cell name:</span></span>  <br/> |<span data-ttu-id="5c4a4-111">LineJumpFactorX</span><span class="sxs-lookup"><span data-stu-id="5c4a4-111">LineJumpFactorX</span></span>  <br/> |
   
<span data-ttu-id="5c4a4-112">Wenn Sie einen Verweis auf die Zelle LineJumpFactorX aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5c4a4-112">To get a reference to the LineJumpFactorX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c4a4-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5c4a4-113">Section index:</span></span>  <br/> |<span data-ttu-id="5c4a4-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5c4a4-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5c4a4-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5c4a4-115">Row index:</span></span>  <br/> |<span data-ttu-id="5c4a4-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="5c4a4-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="5c4a4-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5c4a4-117">Cell index:</span></span>  <br/> |<span data-ttu-id="5c4a4-118">**visPLOJumpFactorX**</span><span class="sxs-lookup"><span data-stu-id="5c4a4-118">**visPLOJumpFactorX**</span></span> <br/> |
   

