---
title: XGridOrigin Cell (Ruler &amp; Grid Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1155
localization_priority: Normal
ms.assetid: 2b1a8902-b1d4-c3d9-8c9f-1a28fddacc59
description: Gibt die horizontale Koordinate des Gitterursprungs an.
ms.openlocfilehash: 0cc6ff10f9bb4ba7ee0a13a48cb55b7dcd0fa013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798445"
---
# <a name="xgridorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="91108-103">XGridOrigin Cell (Ruler &amp; Grid Section)</span><span class="sxs-lookup"><span data-stu-id="91108-103">XGridOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="91108-104">Gibt die horizontale Koordinate des Gitterursprungs an.</span><span class="sxs-lookup"><span data-stu-id="91108-104">Specifies the horizontal coordinate of the grid origin.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91108-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91108-105">Remarks</span></span>

<span data-ttu-id="91108-106">Diese Zelle entspricht der horizontalen **Gitterursprung** option in der **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil **angezeigt** .</span><span class="sxs-lookup"><span data-stu-id="91108-106">This cell corresponds to the horizontal **Grid origin** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow.</span></span> 
  
<span data-ttu-id="91108-107">Wenn Sie einen Verweis auf die Zelle XGridOrigin aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="91108-107">To get a reference to the XGridOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91108-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="91108-108">Cell name:</span></span>  <br/> |<span data-ttu-id="91108-109">XGridOrigin</span><span class="sxs-lookup"><span data-stu-id="91108-109">XGridOrigin</span></span>  <br/> |
   
<span data-ttu-id="91108-110">Wenn Sie einen Verweis auf die Zelle XGridOrigin aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="91108-110">To get a reference to the XGridOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91108-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="91108-111">Section index:</span></span>  <br/> |<span data-ttu-id="91108-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="91108-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="91108-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="91108-113">Row index:</span></span>  <br/> |<span data-ttu-id="91108-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="91108-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="91108-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="91108-115">Cell index:</span></span>  <br/> |<span data-ttu-id="91108-116">**visXGridOrigin**</span><span class="sxs-lookup"><span data-stu-id="91108-116">**visXGridOrigin**</span></span> <br/> |
   

