---
title: Zelle "DirX / A" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Legt die X-Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts. Die Zelle DirX / eine Zelle wird auch verwendet, um die Ausrichtung des verbundenen Abschnitts eines dynamischen Verbinders. Diese Zelle benötigt einen Gleitkommawert Codepunktwert.
ms.openlocfilehash: 49feba7cefbccc4efcbd04e8940c1f801563539e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796869"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="24783-105">DirX / A Cell (Connection Points Section)</span><span class="sxs-lookup"><span data-stu-id="24783-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="24783-106">Legt die *X* -Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts.</span><span class="sxs-lookup"><span data-stu-id="24783-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="24783-107">Die Zelle DirX / eine Zelle wird auch verwendet, um die Ausrichtung des verbundenen Abschnitts eines dynamischen Verbinders.</span><span class="sxs-lookup"><span data-stu-id="24783-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="24783-108">Diese Zelle benötigt einen Gleitkommawert Codepunktwert.</span><span class="sxs-lookup"><span data-stu-id="24783-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="24783-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24783-109">Remarks</span></span>

<span data-ttu-id="24783-110">Wenn Sie einen Verweis auf die Zelle DirX / A aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="24783-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24783-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="24783-111">Cell name:</span></span>  <br/> | <span data-ttu-id="24783-112">Verbindungen.RichtX [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="24783-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="24783-113">Wenn Sie einen Verweis auf die Zelle DirX / A aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="24783-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24783-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="24783-114">Section index:</span></span>  <br/> |<span data-ttu-id="24783-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="24783-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="24783-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="24783-116">Row index:</span></span>  <br/> |<span data-ttu-id="24783-117">**VisRowConnectionPts** +  *i* wobei *i* = 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="24783-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="24783-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="24783-118">Cell index:</span></span>  <br/> |<span data-ttu-id="24783-119">**visCnnctDirX** (nicht erweiterte Zeilen)           **visCnnctA** (erweiterte Zeilen)</span><span class="sxs-lookup"><span data-stu-id="24783-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="24783-120">Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.</span><span class="sxs-lookup"><span data-stu-id="24783-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

