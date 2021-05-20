---
title: Zelle "BlockSizeY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm110
localization_priority: Normal
ms.assetid: be51e18e-ea49-0788-1a17-866090afb9f4
description: Bestimmt die vertikale Blockgröße, den Bereich, in den die einzelnen Shapes auf das Zeichenblatt passen müssen, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren auspassen (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Re-Layout Seite, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 08f2012bb027267810c21ef253a0073bb42d3a96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427402"
---
# <a name="blocksizey-cell-page-layout-section"></a><span data-ttu-id="eeed5-103">Zelle "BlockSizeY" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="eeed5-103">BlockSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="eeed5-104">Bestimmt die vertikale Blockgröße, den Bereich, in den jedes Ihrer Shapes auf das Zeichenblatt passen muss, wenn Sie Shapes mithilfe des Dialogfelds **Layout** konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe **Layout** auf **Seite** neu layout, und klicken Sie dann auf Weitere **Layoutoptionen**). </span><span class="sxs-lookup"><span data-stu-id="eeed5-104">Determines the vertical block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eeed5-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eeed5-105">Remarks</span></span>

<span data-ttu-id="eeed5-106">Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="eeed5-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="eeed5-107">Verwenden Sie zum Erhalten eines Verweises auf die Zelle BlockSizeY anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="eeed5-107">To get a reference to the BlockSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eeed5-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="eeed5-108">Cell name:</span></span>  <br/> | <span data-ttu-id="eeed5-109">BlockSizeY</span><span class="sxs-lookup"><span data-stu-id="eeed5-109">BlockSizeY</span></span>  <br/> |
   
<span data-ttu-id="eeed5-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die BlockSizeY-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="eeed5-110">To get a reference to the BlockSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eeed5-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="eeed5-111">Section index:</span></span>  <br/> |<span data-ttu-id="eeed5-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eeed5-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eeed5-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="eeed5-113">Row index:</span></span>  <br/> |<span data-ttu-id="eeed5-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="eeed5-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="eeed5-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="eeed5-115">Cell index:</span></span>  <br/> |<span data-ttu-id="eeed5-116">**visPLOBlockSizeY**</span><span class="sxs-lookup"><span data-stu-id="eeed5-116">**visPLOBlockSizeY**</span></span> <br/> |
   

