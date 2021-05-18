---
title: Zelle "LineJumpFactorY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
localization_priority: Normal
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: Bestimmt die Größe von Liniensprüngen auf vertikalen dynamischen Verbindern auf dem Zeichenblatt, und zwar relativ zum Wert der Zelle LineToLineY. Der Wert dieser Zelle kann im Bereich zwischen 0 und 10 liegen, jedoch sind Bruchwerte zwischen 0 und 1 empfehlenswert.
ms.openlocfilehash: 36712c1558ff2f50309dc31e8f918061180c8fa4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411960"
---
# <a name="linejumpfactory-cell-page-layout-section"></a><span data-ttu-id="d00cb-104">Zelle "LineJumpFactorY" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="d00cb-104">LineJumpFactorY Cell (Page Layout Section)</span></span>

<span data-ttu-id="d00cb-p102">Bestimmt die Größe von Liniensprüngen auf vertikalen dynamischen Verbindern auf dem Zeichenblatt, und zwar relativ zum Wert der Zelle LineToLineY. Der Wert dieser Zelle kann im Bereich zwischen 0 und 10 liegen, jedoch sind Bruchwerte zwischen 0 und 1 empfehlenswert.</span><span class="sxs-lookup"><span data-stu-id="d00cb-p102">Determines the size of line jumps on vertical dynamic connectors on the page, relative to the value of the LineToLineY cell. The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d00cb-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d00cb-107">Remarks</span></span>

<span data-ttu-id="d00cb-108">Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).</span><span class="sxs-lookup"><span data-stu-id="d00cb-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="d00cb-109">Um einen Verweis auf die Zelle LineJumpFactorY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="d00cb-109">To get a reference to the LineJumpFactorY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d00cb-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d00cb-110">Cell name:</span></span>  <br/> |<span data-ttu-id="d00cb-111">LineJumpFactorY</span><span class="sxs-lookup"><span data-stu-id="d00cb-111">LineJumpFactorY</span></span>  <br/> |
   
<span data-ttu-id="d00cb-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LineJumpFactorY-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="d00cb-112">To get a reference to the LineJumpFactorY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d00cb-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d00cb-113">Section index:</span></span>  <br/> |<span data-ttu-id="d00cb-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d00cb-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d00cb-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d00cb-115">Row index:</span></span>  <br/> |<span data-ttu-id="d00cb-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="d00cb-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="d00cb-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d00cb-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d00cb-118">**visPLOJumpFactorY**</span><span class="sxs-lookup"><span data-stu-id="d00cb-118">**visPLOJumpFactorY**</span></span> <br/> |
   

