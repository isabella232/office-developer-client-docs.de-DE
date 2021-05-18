---
title: Zelle "ShapeShdwObliqueAngle" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033174
localization_priority: Normal
ms.assetid: bad4c512-e91f-d459-d65c-a4ab725c3c14
description: Gibt den Winkel der Schrägrichtung des Shape-Schattens an.
ms.openlocfilehash: 005415e497a4d985d3fb8ec70d62ba40d9e80c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414032"
---
# <a name="shapeshdwobliqueangle-cell-fill-format-section"></a><span data-ttu-id="94861-103">Zelle "ShapeShdwObliqueAngle" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="94861-103">ShapeShdwObliqueAngle Cell (Fill Format Section)</span></span>

<span data-ttu-id="94861-104">Gibt den Winkel der Schrägrichtung des Shape-Schattens an.</span><span class="sxs-lookup"><span data-stu-id="94861-104">Specifies the angle of oblique direction of a shape's shadow.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94861-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="94861-105">Remarks</span></span>

<span data-ttu-id="94861-106">Der Wert Null (0) in dieser Zelle zeigt an, dass die Winkelrichtung genau nach oben verläuft, sie wird im Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="94861-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
<span data-ttu-id="94861-107">Dieser Wert entspricht dem Wert der Einstellung **Richtung** im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).</span><span class="sxs-lookup"><span data-stu-id="94861-107">This value corresponds to the value of the **Direction** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="94861-108">Verwenden Sie zum Erhalten eines Verweises auf die Zelle ShapeShdwObliqueAngle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="94861-108">To get a reference to the ShapeShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94861-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="94861-109">Cell name:</span></span>  <br/> | <span data-ttu-id="94861-110">ShapeShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="94861-110">ShapeShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="94861-111">Um einen Verweis auf die Zelle ShapeShdwObliqueAngle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="94861-111">To get a reference to the ShapeShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94861-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="94861-112">Section index:</span></span>  <br/> |<span data-ttu-id="94861-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="94861-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="94861-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="94861-114">Row index:</span></span>  <br/> |<span data-ttu-id="94861-115">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="94861-115">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="94861-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="94861-116">Cell index:</span></span>  <br/> |<span data-ttu-id="94861-117">**visFillShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="94861-117">**visFillShdwObliqueAngle**</span></span> <br/> |
   

