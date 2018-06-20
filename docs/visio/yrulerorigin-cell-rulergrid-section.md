---
title: Zelle "YRulerOrigin" (Lineal &amp; Rasterabschnitt)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1220
localization_priority: Normal
ms.assetid: 5d21b64f-a559-76ef-06df-d24c048cc6ef
description: Gibt den Nullpunkt auf der y-Achse-Achsenlineal des Zeichenblatts an.
ms.openlocfilehash: 143f372d66ee25e90608a9b2eb252a99e7bcc52f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798473"
---
# <a name="yrulerorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="db8cc-103">Zelle "YRulerOrigin" (Lineal &amp; Rasterabschnitt)</span><span class="sxs-lookup"><span data-stu-id="db8cc-103">YRulerOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="db8cc-104">Gibt den Nullpunkt auf der y-Achse-Achsenlineal des Zeichenblatts an.</span><span class="sxs-lookup"><span data-stu-id="db8cc-104">Specifies the zero point on the y-axis ruler for the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="db8cc-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="db8cc-105">Remarks</span></span>

<span data-ttu-id="db8cc-106">Diese Zelle entspricht der vertikalen Option **Linealursprung** in die **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ).</span><span class="sxs-lookup"><span data-stu-id="db8cc-106">This cell corresponds to the vertical **Ruler zero** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="db8cc-107">Wenn Sie einen Verweis auf die Zelle YRulerOrigin nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="db8cc-107">To get a reference to the YRulerOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db8cc-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="db8cc-108">Cell name:</span></span>  <br/> |<span data-ttu-id="db8cc-109">YRulerOrigin</span><span class="sxs-lookup"><span data-stu-id="db8cc-109">YRulerOrigin</span></span>  <br/> |
   
<span data-ttu-id="db8cc-110">Wenn Sie einen Verweis auf die Zelle YRulerOrigin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="db8cc-110">To get a reference to the YRulerOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db8cc-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="db8cc-111">Section index:</span></span>  <br/> |<span data-ttu-id="db8cc-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="db8cc-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="db8cc-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="db8cc-113">Row index:</span></span>  <br/> |<span data-ttu-id="db8cc-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="db8cc-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="db8cc-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="db8cc-115">Cell index:</span></span>  <br/> |<span data-ttu-id="db8cc-116">**visYRulerOrigin**</span><span class="sxs-lookup"><span data-stu-id="db8cc-116">**visYRulerOrigin**</span></span> <br/> |
   

