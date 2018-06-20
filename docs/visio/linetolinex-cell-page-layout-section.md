---
title: Zelle "LineToLineX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm565
localization_priority: Normal
ms.assetid: f6b461fe-56ac-4c0e-31cd-6b3c1075db6e
description: Legt den horizontalen Abstand zwischen sämtlichen Verbindern auf dem Zeichenblatt fest.
ms.openlocfilehash: aa6476eab9d5bcf7aab12235fd23f0f5675d6ad5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797332"
---
# <a name="linetolinex-cell-page-layout-section"></a><span data-ttu-id="78193-103">Zelle "LineToLineX" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="78193-103">LineToLineX Cell (Page Layout Section)</span></span>

<span data-ttu-id="78193-104">Legt den horizontalen Abstand zwischen sämtlichen Verbindern auf dem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="78193-104">Determines the horizontal clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="78193-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78193-105">Remarks</span></span>

<span data-ttu-id="78193-106">Sie können den Wert dieser Zelle auch im Dialogfeld **Layout und Routing Abstand** festlegen.</span><span class="sxs-lookup"><span data-stu-id="78193-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="78193-107">(Klicken Sie auf der Registerkarte **Entwurf** klicken Sie auf den Pfeil neben **Seite einrichten** , klicken Sie auf **Layout und Routing**, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="78193-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="78193-108">Wenn Sie einen Verweis auf die Zelle LineToLineX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="78193-108">To get a reference to the LineToLineX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78193-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="78193-109">Cell name:</span></span>  <br/> |<span data-ttu-id="78193-110">LineToLineX</span><span class="sxs-lookup"><span data-stu-id="78193-110">LineToLineX</span></span>  <br/> |
   
<span data-ttu-id="78193-111">Wenn Sie einen Verweis auf die Zelle LineToLineX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="78193-111">To get a reference to the LineToLineX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78193-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="78193-112">Section index:</span></span>  <br/> |<span data-ttu-id="78193-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="78193-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="78193-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="78193-114">Row index:</span></span>  <br/> |<span data-ttu-id="78193-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="78193-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="78193-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="78193-116">Cell index:</span></span>  <br/> |<span data-ttu-id="78193-117">**visPLOLineToLineX**</span><span class="sxs-lookup"><span data-stu-id="78193-117">**visPLOLineToLineX**</span></span> <br/> |
   

