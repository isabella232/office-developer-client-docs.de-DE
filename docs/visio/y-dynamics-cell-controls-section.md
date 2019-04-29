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
description: Stellt die y-Koordinate für den Verankerungspunkt eines Steuerelements in lokalen Koordinaten dar. Der Verankerungspunkt wird zum Rubber-Banding bei aktivierter Dynamik verwendet.
ms.openlocfilehash: 13d463ebccd9cc7a23641a036dc5dd967513b07f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404827"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="ddf44-104">Zelle "Y Dynamics" (Abschnitt "Controls")</span><span class="sxs-lookup"><span data-stu-id="ddf44-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="ddf44-105">Stellt die *y* -Koordinate für den Verankerungspunkt eines Steuerelements in lokalen Koordinaten dar.</span><span class="sxs-lookup"><span data-stu-id="ddf44-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="ddf44-106">Der Verankerungspunkt wird zum "Rubber-Banding" bei aktivierter Dynamik verwendet.</span><span class="sxs-lookup"><span data-stu-id="ddf44-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ddf44-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddf44-107">Remarks</span></span>

<span data-ttu-id="ddf44-108">Wenn Sie einen Verweis auf die Zelle Y Dynamics aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ddf44-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ddf44-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ddf44-109">Cell name:</span></span>  <br/> | <span data-ttu-id="ddf44-110">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="ddf44-110">Controls.</span></span>  <span data-ttu-id="ddf44-111">*Name* . YDynwhere-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="ddf44-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="ddf44-112">*Name* ist der Name der Zeile Controls.</span><span class="sxs-lookup"><span data-stu-id="ddf44-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="ddf44-113">Wenn Sie einen Verweis auf die Zelle Y Dynamics nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ddf44-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ddf44-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ddf44-114">Section index:</span></span>  <br/> |<span data-ttu-id="ddf44-115">**Konstanten visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="ddf44-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="ddf44-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ddf44-116">Row index:</span></span>  <br/> |<span data-ttu-id="ddf44-117">**visRowControl** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ddf44-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ddf44-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ddf44-118">Cell index:</span></span>  <br/> |<span data-ttu-id="ddf44-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="ddf44-119">**visCtlYDyn**</span></span> <br/> |
   

