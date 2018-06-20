---
title: Zelle "Y Dynamics" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Stellt die y-Koordinate für den Verankerungspunkt eines Steuerpunkts, in lokalen Koordinaten dar. Der Verankerungspunkt wird zum Rubber-Banding bei aktivierter Dynamik verwendet.
ms.openlocfilehash: 162f062d382f3f303ae39db725f3fbfa0790bfc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798487"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="a2487-104">Zelle "Y Dynamics" (Abschnitt "Controls")</span><span class="sxs-lookup"><span data-stu-id="a2487-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="a2487-105">Stellt die *y* -Koordinate für den Verankerungspunkt eines Steuerpunkts, in lokalen Koordinaten dar.</span><span class="sxs-lookup"><span data-stu-id="a2487-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="a2487-106">Der Verankerungspunkt wird zum Rubber-Banding bei aktivierter Dynamik verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2487-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a2487-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a2487-107">Remarks</span></span>

<span data-ttu-id="a2487-108">Wenn Sie einen Verweis auf die Zelle Y Dynamics nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a2487-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2487-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a2487-109">Cell name:</span></span>  <br/> | <span data-ttu-id="a2487-110">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="a2487-110">Controls.</span></span>  <span data-ttu-id="a2487-111">*Name* . YDynwhere-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="a2487-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="a2487-112">*Name* ist der Name der Zeile mit Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="a2487-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="a2487-113">Wenn Sie einen Verweis auf die Zelle Y Dynamics aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a2487-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2487-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a2487-114">Section index:</span></span>  <br/> |<span data-ttu-id="a2487-115">**Konstanten visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="a2487-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="a2487-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a2487-116">Row index:</span></span>  <br/> |<span data-ttu-id="a2487-117">**VisRowControl** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a2487-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a2487-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a2487-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a2487-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="a2487-119">**visCtlYDyn**</span></span> <br/> |
   

