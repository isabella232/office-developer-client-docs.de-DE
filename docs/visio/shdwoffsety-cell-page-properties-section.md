---
title: Zelle "ShdwOffsetY" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf vertikaler Ebene vom Shape entfernt ist.
ms.openlocfilehash: be7ec4cccd53cc9d74811e2e45122c8bc29497d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438141"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="e5fd3-103">Zelle "ShdwOffsetY" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="e5fd3-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="e5fd3-104">Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf vertikaler Ebene vom Shape entfernt ist.</span><span class="sxs-lookup"><span data-stu-id="e5fd3-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5fd3-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e5fd3-105">Remarks</span></span>

<span data-ttu-id="e5fd3-p101">Dieser Wert wird im Dialogfeld **Seite einrichten** festgelegt (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Bei Größenänderung der Zeichnung bleibt der Schattenabstand gleich.</span><span class="sxs-lookup"><span data-stu-id="e5fd3-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="e5fd3-109">Verwenden Sie zum Rufen eines Verweises auf die Zelle ShdwOffsetY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="e5fd3-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e5fd3-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e5fd3-110">Cell name:</span></span>  <br/> | <span data-ttu-id="e5fd3-111">ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="e5fd3-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="e5fd3-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ShdwOffsetY-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="e5fd3-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e5fd3-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e5fd3-113">Section index:</span></span>  <br/> |<span data-ttu-id="e5fd3-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e5fd3-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e5fd3-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e5fd3-115">Row index:</span></span>  <br/> |<span data-ttu-id="e5fd3-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="e5fd3-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="e5fd3-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e5fd3-117">Cell index:</span></span>  <br/> |<span data-ttu-id="e5fd3-118">**visPageShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="e5fd3-118">**visPageShdwOffsetY**</span></span> <br/> |
   

