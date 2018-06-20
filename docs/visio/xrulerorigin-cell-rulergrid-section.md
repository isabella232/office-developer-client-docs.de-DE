---
title: Zelle "XRulerOrigin" (Lineal &amp; Rasterabschnitt)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1170
localization_priority: Normal
ms.assetid: 328f8ab5-217f-0336-0d56-611eff509fe8
description: Gibt den Nullpunkt auf der x-Achse-Achsenlineal des Zeichenblatts an.
ms.openlocfilehash: 78fab70c8489ddcdfe450ef9f9fd88b6c5040211
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798446"
---
# <a name="xrulerorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="eff55-103">Zelle "XRulerOrigin" (Lineal &amp; Rasterabschnitt)</span><span class="sxs-lookup"><span data-stu-id="eff55-103">XRulerOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="eff55-104">Gibt den Nullpunkt auf der x-Achse-Achsenlineal des Zeichenblatts an.</span><span class="sxs-lookup"><span data-stu-id="eff55-104">Specifies the zero point on the x-axis ruler for the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eff55-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eff55-105">Remarks</span></span>

<span data-ttu-id="eff55-106">Diese Zelle entspricht der horizontalen Option **Linealursprung** in die **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ).</span><span class="sxs-lookup"><span data-stu-id="eff55-106">This cell corresponds to the horizontal **Ruler zero** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="eff55-107">Wenn Sie einen Verweis auf die Zelle XRulerOrigin nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="eff55-107">To get a reference to the XRulerOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eff55-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="eff55-108">Cell name:</span></span>  <br/> |<span data-ttu-id="eff55-109">XRulerOrigin</span><span class="sxs-lookup"><span data-stu-id="eff55-109">XRulerOrigin</span></span>  <br/> |
   
<span data-ttu-id="eff55-110">Wenn Sie einen Verweis auf die Zelle XRulerOrigin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="eff55-110">To get a reference to the XRulerOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eff55-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="eff55-111">Section index:</span></span>  <br/> |<span data-ttu-id="eff55-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eff55-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="eff55-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="eff55-113">Row index:</span></span>  <br/> |<span data-ttu-id="eff55-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="eff55-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="eff55-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="eff55-115">Cell index:</span></span>  <br/> |<span data-ttu-id="eff55-116">**visXRulerOrigin**</span><span class="sxs-lookup"><span data-stu-id="eff55-116">**visXRulerOrigin**</span></span> <br/> |
   

