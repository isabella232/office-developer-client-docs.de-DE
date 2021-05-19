---
title: Zelle "BlockSizeX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm105
localization_priority: Normal
ms.assetid: 253aac17-077e-48e0-39a8-a3abd5d4a257
description: Bestimmt die horizontale Blockgröße, den Bereich, in den jedes Ihrer Shapes auf das Zeichenblatt passen muss, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Re-Layout Seite, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 8e4cee4b2059d9b8f2fe77c2d4902e67246eac2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424189"
---
# <a name="blocksizex-cell-page-layout-section"></a><span data-ttu-id="37623-103">Zelle "BlockSizeX" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="37623-103">BlockSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="37623-104">Bestimmt die horizontale Blockgröße, den Bereich, in den die einzelnen Shapes auf das Zeichenblatt passen müssen, wenn Sie Shapes mithilfe des Dialogfelds **Layout** konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe **Layout** auf **Seite** neu layout, und klicken Sie dann auf Weitere **Layoutoptionen**). </span><span class="sxs-lookup"><span data-stu-id="37623-104">Determines the horizontal block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37623-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="37623-105">Remarks</span></span>

<span data-ttu-id="37623-106">Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="37623-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="37623-107">Verwenden Sie zum Erhalten eines Verweises auf die Zelle BlockSizeX anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="37623-107">To get a reference to the BlockSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37623-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="37623-108">Cell name:</span></span>  <br/> |<span data-ttu-id="37623-109">BlockSizeX</span><span class="sxs-lookup"><span data-stu-id="37623-109">BlockSizeX</span></span>  <br/> |
   
<span data-ttu-id="37623-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die BlockSizeX-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="37623-110">To get a reference to the BlockSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37623-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="37623-111">Section index:</span></span>  <br/> |<span data-ttu-id="37623-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="37623-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="37623-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="37623-113">Row index:</span></span>  <br/> |<span data-ttu-id="37623-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="37623-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="37623-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="37623-115">Cell index:</span></span>  <br/> |<span data-ttu-id="37623-116">**visPLOBlockSizeX**</span><span class="sxs-lookup"><span data-stu-id="37623-116">**visPLOBlockSizeX**</span></span> <br/> |
   

