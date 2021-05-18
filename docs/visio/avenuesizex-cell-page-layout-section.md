---
title: Zelle "AvenueSizeX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Bestimmt den horizontalen Abstand zwischen Shapes auf dem Zeichenblatt, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Re-Layout Seite, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411645"
---
# <a name="avenuesizex-cell-page-layout-section"></a><span data-ttu-id="af1c2-103">Zelle "AvenueSizeX" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="af1c2-103">AvenueSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="af1c2-104">Bestimmt den horizontalen Abstand zwischen Shapes auf dem Zeichenblatt, wenn Sie Shapes  mithilfe des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe Layout auf **Seite** neu layout, und klicken Sie dann auf \*\* Weitere Layoutoptionen \*\*). </span><span class="sxs-lookup"><span data-stu-id="af1c2-104">Determines the amount of horizontal space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click \*\* More Layout Options \*\*).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af1c2-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="af1c2-105">Remarks</span></span>

<span data-ttu-id="af1c2-106">Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="af1c2-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="af1c2-107">Das dynamische Raster verwendet die Einstellung in der Zelle AvenueSizeX, wenn nur eine Form zum Berechnen des horizontalen Abstands verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="af1c2-107">The dynamic grid uses the setting in the AvenueSizeX cell when only one shape is available for calculating horizontal spacing.</span></span> <span data-ttu-id="af1c2-108">Um das dynamische Raster zu verwenden, wählen Sie auf **der** Registerkarte Ansicht in der **Gruppe Visuelle** Hilfen **dynamisches Raster aus.**</span><span class="sxs-lookup"><span data-stu-id="af1c2-108">To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="af1c2-109">Verwenden Sie zum Erhalten eines Verweises auf die Zelle AvenueSizeX anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="af1c2-109">To get a reference to the AvenueSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af1c2-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="af1c2-110">Cell name:</span></span>  <br/> | <span data-ttu-id="af1c2-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="af1c2-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="af1c2-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die AvenueSizeX-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="af1c2-112">To get a reference to the AvenueSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af1c2-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="af1c2-113">Section index:</span></span>  <br/> |<span data-ttu-id="af1c2-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="af1c2-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="af1c2-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="af1c2-115">Row index:</span></span>  <br/> |<span data-ttu-id="af1c2-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="af1c2-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="af1c2-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="af1c2-117">Cell index:</span></span>  <br/> |<span data-ttu-id="af1c2-118">**visPLOAvenueSizeX**</span><span class="sxs-lookup"><span data-stu-id="af1c2-118">**visPLOAvenueSizeX**</span></span> <br/> |
   

