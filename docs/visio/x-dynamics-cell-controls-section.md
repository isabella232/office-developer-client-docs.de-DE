---
title: Zelle "X Dynamics" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Stellt die X-Koordinate für den Verankerungspunkt eines Steuerpunkts, in lokalen Koordinaten dar.
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798457"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="caa27-103">X Dynamics Cell (Controls Section)</span><span class="sxs-lookup"><span data-stu-id="caa27-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="caa27-104">Stellt die *X* -Koordinate für den Verankerungspunkt eines Steuerpunkts, in lokalen Koordinaten dar.</span><span class="sxs-lookup"><span data-stu-id="caa27-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="caa27-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="caa27-105">Remarks</span></span>

<span data-ttu-id="caa27-106">Der Verankerungspunkt wird zum Rubber-Banding bei aktivierter Dynamik verwendet.</span><span class="sxs-lookup"><span data-stu-id="caa27-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="caa27-107">Wenn Sie einen Verweis auf die Zelle X Dynamics aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="caa27-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="caa27-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="caa27-108">Cell name:</span></span>  <br/> | <span data-ttu-id="caa27-109">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="caa27-109">Controls.</span></span>  <span data-ttu-id="caa27-110">*Name* . XDynwhere-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="caa27-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="caa27-111">*Name* ist der Name der Zeile mit Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="caa27-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="caa27-112">Wenn Sie einen Verweis auf die Zelle X Dynamics aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="caa27-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="caa27-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="caa27-113">Section index:</span></span>  <br/> |<span data-ttu-id="caa27-114">**Konstanten visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="caa27-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="caa27-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="caa27-115">Row index:</span></span>  <br/> |<span data-ttu-id="caa27-116">**VisRowControl** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="caa27-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="caa27-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="caa27-117">Cell index:</span></span>  <br/> |<span data-ttu-id="caa27-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="caa27-118">**visCtlXDyn**</span></span> <br/> |
   

