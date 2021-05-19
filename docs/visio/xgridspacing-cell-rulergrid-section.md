---
title: Zelle "XGridSpacing" (Abschnitt &amp; "Ruler Grid")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Gibt den Abstand zwischen den horizontalen Linien eines festen Gitters an (XGridDensity = 0).
ms.openlocfilehash: 05b68a9721dbfc9c03402d384d976c42ef05b134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435075"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="22b75-103">Zelle "XGridSpacing" (Abschnitt &amp; "Ruler Grid")</span><span class="sxs-lookup"><span data-stu-id="22b75-103">XGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="22b75-104">Gibt den Abstand zwischen den horizontalen Linien eines festen Gitters an (XGridDensity = 0).</span><span class="sxs-lookup"><span data-stu-id="22b75-104">Specifies the distance between horizontal lines in a fixed grid (XGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="22b75-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22b75-105">Remarks</span></span>

<span data-ttu-id="22b75-106">Diese Zelle entspricht der horizontalen Option **Minimaler Abstand** im  Dialogfeld **&amp; Linealraster** (klicken Sie auf der Registerkarte Ansicht auf den **Pfeil anzeigen).**</span><span class="sxs-lookup"><span data-stu-id="22b75-106">This cell corresponds to the horizontal **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="22b75-107">Um einen Verweis auf die Zelle XGridSpacing anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="22b75-107">To get a reference to the XGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22b75-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="22b75-108">Cell name:</span></span>  <br/> |<span data-ttu-id="22b75-109">XGridSpacing</span><span class="sxs-lookup"><span data-stu-id="22b75-109">XGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="22b75-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle XGridSpacing nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="22b75-110">To get a reference to the XGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22b75-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="22b75-111">Section index:</span></span>  <br/> |<span data-ttu-id="22b75-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="22b75-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="22b75-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="22b75-113">Row index:</span></span>  <br/> |<span data-ttu-id="22b75-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="22b75-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="22b75-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="22b75-115">Cell index:</span></span>  <br/> |<span data-ttu-id="22b75-116">**visXGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="22b75-116">**visXGridSpacing**</span></span> <br/> |
   

