---
title: Zelle "YGridOrigin" (Lineal &amp; Rasterabschnitt)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1205
localization_priority: Normal
ms.assetid: eeec59f8-f301-5639-ffd6-8a36b2bf9c8f
description: Gibt den vertikalen Ursprung des Gitters an.
ms.openlocfilehash: 2d914fc15df8a100066ad17a2e35001fe8a4d587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798463"
---
# <a name="ygridorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="71f00-103">Zelle "YGridOrigin" (Lineal &amp; Rasterabschnitt)</span><span class="sxs-lookup"><span data-stu-id="71f00-103">YGridOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="71f00-104">Gibt den vertikalen Ursprung des Gitters an.</span><span class="sxs-lookup"><span data-stu-id="71f00-104">Specifies the vertical origin of the grid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="71f00-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71f00-105">Remarks</span></span>

<span data-ttu-id="71f00-106">Diese Zelle entspricht der vertikalen **Gitterursprung** option in der **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ).</span><span class="sxs-lookup"><span data-stu-id="71f00-106">This cell corresponds to the vertical **Grid origin** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="71f00-107">Wenn Sie einen Verweis auf die Zelle YGridOrigin nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="71f00-107">To get a reference to the YGridOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71f00-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="71f00-108">Cell name:</span></span>  <br/> |<span data-ttu-id="71f00-109">YGridOrigin</span><span class="sxs-lookup"><span data-stu-id="71f00-109">YGridOrigin</span></span>  <br/> |
   
<span data-ttu-id="71f00-110">Wenn Sie einen Verweis auf die Zelle YGridOrigin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="71f00-110">To get a reference to the YGridOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71f00-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="71f00-111">Section index:</span></span>  <br/> |<span data-ttu-id="71f00-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="71f00-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="71f00-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="71f00-113">Row index:</span></span>  <br/> |<span data-ttu-id="71f00-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="71f00-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="71f00-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="71f00-115">Cell index:</span></span>  <br/> |<span data-ttu-id="71f00-116">**visYGridOrigin**</span><span class="sxs-lookup"><span data-stu-id="71f00-116">**visYGridOrigin**</span></span> <br/> |
   

