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
description: Bestimmt die vertikale Blockgröße, den Bereich, in dem jede Ihrer Shapes auf das Zeichenblatt passen muss, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (Klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu Layout, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 08f2012bb027267810c21ef253a0073bb42d3a96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427402"
---
# <a name="blocksizey-cell-page-layout-section"></a><span data-ttu-id="ad005-103">Zelle "BlockSizeY" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="ad005-103">BlockSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="ad005-104">Bestimmt die vertikale Blockgröße, den Bereich, in dem jede Ihrer Shapes auf das Zeichenblatt passen muss, wenn Sie Shapes mithilfe des Dialogfelds **Layout konfigurieren** (Klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu Layout**). und klicken Sie dann auf **Weitere Layoutoptionen**).</span><span class="sxs-lookup"><span data-stu-id="ad005-104">Determines the vertical block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad005-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad005-105">Remarks</span></span>

<span data-ttu-id="ad005-106">Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="ad005-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="ad005-107">Wenn Sie einen Verweis auf die Zelle Zelle BlockSizeY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ad005-107">To get a reference to the BlockSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad005-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ad005-108">Cell name:</span></span>  <br/> | <span data-ttu-id="ad005-109">Zelle BlockSizeY</span><span class="sxs-lookup"><span data-stu-id="ad005-109">BlockSizeY</span></span>  <br/> |
   
<span data-ttu-id="ad005-110">Wenn Sie einen Verweis auf die Zelle Zelle BlockSizeY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ad005-110">To get a reference to the BlockSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad005-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ad005-111">Section index:</span></span>  <br/> |<span data-ttu-id="ad005-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ad005-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ad005-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ad005-113">Row index:</span></span>  <br/> |<span data-ttu-id="ad005-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="ad005-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="ad005-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ad005-115">Cell index:</span></span>  <br/> |<span data-ttu-id="ad005-116">**visPLOBlockSizeY**</span><span class="sxs-lookup"><span data-stu-id="ad005-116">**visPLOBlockSizeY**</span></span> <br/> |
   

