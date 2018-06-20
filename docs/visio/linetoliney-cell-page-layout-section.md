---
title: Zelle "LineToLineY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm570
localization_priority: Normal
ms.assetid: db9a8232-25c5-7087-2ae9-50470d0cf16e
description: Legt den vertikalen Abstand zwischen sämtlichen Verbindern auf dem Zeichenblatt fest.
ms.openlocfilehash: 781d166fe0b81cc2402fde2894cd1d0480a0895f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797337"
---
# <a name="linetoliney-cell-page-layout-section"></a><span data-ttu-id="0855e-103">Zelle "LineToLineY" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="0855e-103">LineToLineY Cell (Page Layout Section)</span></span>

<span data-ttu-id="0855e-104">Legt den vertikalen Abstand zwischen sämtlichen Verbindern auf dem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="0855e-104">Determines the vertical clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0855e-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0855e-105">Remarks</span></span>

<span data-ttu-id="0855e-106">Sie können den Wert dieser Zelle auch im Dialogfeld **Layout und Routing Abstand** festlegen.</span><span class="sxs-lookup"><span data-stu-id="0855e-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="0855e-107">(Klicken Sie auf der Registerkarte **Entwurf** klicken Sie auf den Pfeil neben **Seite einrichten** , klicken Sie auf **Layout und Routing**, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="0855e-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="0855e-108">Wenn Sie einen Verweis auf die Zelle LineToLineY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0855e-108">To get a reference to the LineToLineY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0855e-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0855e-109">Cell name:</span></span>  <br/> |<span data-ttu-id="0855e-110">LineToLineY</span><span class="sxs-lookup"><span data-stu-id="0855e-110">LineToLineY</span></span>  <br/> |
   
<span data-ttu-id="0855e-111">Wenn Sie einen Verweis auf die Zelle LineToLineY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0855e-111">To get a reference to the LineToLineY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0855e-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0855e-112">Section index:</span></span>  <br/> |<span data-ttu-id="0855e-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0855e-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0855e-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0855e-114">Row index:</span></span>  <br/> |<span data-ttu-id="0855e-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="0855e-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="0855e-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0855e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="0855e-117">**visPLOLineToLineY**</span><span class="sxs-lookup"><span data-stu-id="0855e-117">**visPLOLineToLineY**</span></span> <br/> |
   

