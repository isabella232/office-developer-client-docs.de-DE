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
ms.openlocfilehash: e98c3e05ffb1739f9b2739ce4e0ee8012afe2266
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428473"
---
# <a name="linetoliney-cell-page-layout-section"></a><span data-ttu-id="b417c-103">Zelle "LineToLineY" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="b417c-103">LineToLineY Cell (Page Layout Section)</span></span>

<span data-ttu-id="b417c-104">Legt den vertikalen Abstand zwischen sämtlichen Verbindern auf dem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="b417c-104">Determines the vertical clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b417c-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b417c-105">Remarks</span></span>

<span data-ttu-id="b417c-p101">Sie können den Wert dieser Zelle auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, wählen Sie **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="b417c-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="b417c-108">Um einen Verweis auf die Zelle LineToLineY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="b417c-108">To get a reference to the LineToLineY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b417c-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b417c-109">Cell name:</span></span>  <br/> |<span data-ttu-id="b417c-110">LineToLineY</span><span class="sxs-lookup"><span data-stu-id="b417c-110">LineToLineY</span></span>  <br/> |
   
<span data-ttu-id="b417c-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LineToLineY-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b417c-111">To get a reference to the LineToLineY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b417c-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b417c-112">Section index:</span></span>  <br/> |<span data-ttu-id="b417c-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b417c-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b417c-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b417c-114">Row index:</span></span>  <br/> |<span data-ttu-id="b417c-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b417c-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b417c-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b417c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b417c-117">**visPLOLineToLineY**</span><span class="sxs-lookup"><span data-stu-id="b417c-117">**visPLOLineToLineY**</span></span> <br/> |
   

