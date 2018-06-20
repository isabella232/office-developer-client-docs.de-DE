---
title: Zelle "XGridSpacing" (Lineal &amp; Rasterabschnitt)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Gibt den Abstand zwischen den horizontalen Linien eines festen Gitters an (XGridDensity = 0).
ms.openlocfilehash: 5f461d02dae1574fe2b186b43166ef14d8251df2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798434"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="1d7b6-103">Zelle "XGridSpacing" (Lineal &amp; Rasterabschnitt)</span><span class="sxs-lookup"><span data-stu-id="1d7b6-103">XGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="1d7b6-104">Gibt den Abstand zwischen den horizontalen Linien eines festen Gitters an (XGridDensity = 0).</span><span class="sxs-lookup"><span data-stu-id="1d7b6-104">Specifies the distance between horizontal lines in a fixed grid (XGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d7b6-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d7b6-105">Remarks</span></span>

<span data-ttu-id="1d7b6-106">Diese Zelle entspricht der horizontalen **minimaler Abstand** option in der **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ).</span><span class="sxs-lookup"><span data-stu-id="1d7b6-106">This cell corresponds to the horizontal **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="1d7b6-107">Wenn Sie einen Verweis auf die Zelle XGridSpacing nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1d7b6-107">To get a reference to the XGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d7b6-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1d7b6-108">Cell name:</span></span>  <br/> |<span data-ttu-id="1d7b6-109">XGridSpacing</span><span class="sxs-lookup"><span data-stu-id="1d7b6-109">XGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="1d7b6-110">Wenn Sie einen Verweis auf die Zelle XGridSpacing aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1d7b6-110">To get a reference to the XGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d7b6-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1d7b6-111">Section index:</span></span>  <br/> |<span data-ttu-id="1d7b6-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1d7b6-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1d7b6-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1d7b6-113">Row index:</span></span>  <br/> |<span data-ttu-id="1d7b6-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="1d7b6-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="1d7b6-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1d7b6-115">Cell index:</span></span>  <br/> |<span data-ttu-id="1d7b6-116">**visXGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="1d7b6-116">**visXGridSpacing**</span></span> <br/> |
   

