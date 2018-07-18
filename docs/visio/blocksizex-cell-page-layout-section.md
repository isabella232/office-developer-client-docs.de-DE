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
description: Bestimmt die horizontale Blockgröße, den Bereich in die jeweils auf dem Zeichenblatt passen müssen, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout, klicken Sie auf der Seite Re-Layout, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 68ed13b85583326c25635049d7e85babe62d5eb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796532"
---
# <a name="blocksizex-cell-page-layout-section"></a><span data-ttu-id="5f7b6-103">BlockSizeX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="5f7b6-103">BlockSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="5f7b6-104">Bestimmt die horizontale Blockgröße, den Bereich in die jeweils auf dem Zeichenblatt passen müssen, wenn Sie Shapes mithilfe des Dialogfelds **Layout konfigurieren** (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Re-Seitenlayout **, und klicken Sie dann auf **Weitere Layoutoptionen**).</span><span class="sxs-lookup"><span data-stu-id="5f7b6-104">Determines the horizontal block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f7b6-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f7b6-105">Remarks</span></span>

<span data-ttu-id="5f7b6-106">Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="5f7b6-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="5f7b6-107">Wenn Sie einen Verweis auf die Zelle BlockSizeX aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5f7b6-107">To get a reference to the BlockSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5f7b6-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5f7b6-108">Cell name:</span></span>  <br/> |<span data-ttu-id="5f7b6-109">BlockSizeX</span><span class="sxs-lookup"><span data-stu-id="5f7b6-109">BlockSizeX</span></span>  <br/> |
   
<span data-ttu-id="5f7b6-110">Wenn Sie einen Verweis auf die Zelle BlockSizeX aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5f7b6-110">To get a reference to the BlockSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5f7b6-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5f7b6-111">Section index:</span></span>  <br/> |<span data-ttu-id="5f7b6-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5f7b6-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5f7b6-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5f7b6-113">Row index:</span></span>  <br/> |<span data-ttu-id="5f7b6-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="5f7b6-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="5f7b6-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5f7b6-115">Cell index:</span></span>  <br/> |<span data-ttu-id="5f7b6-116">**visPLOBlockSizeX**</span><span class="sxs-lookup"><span data-stu-id="5f7b6-116">**visPLOBlockSizeX**</span></span> <br/> |
   

