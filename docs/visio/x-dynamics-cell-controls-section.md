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
description: Stellt die x-Koordinate für den Verankerungspunkt eines Steuerelements in lokalen Koordinaten dar.
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432128"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="a6233-103">Zelle "X Dynamics" (Abschnitt "Controls")</span><span class="sxs-lookup"><span data-stu-id="a6233-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="a6233-104">Stellt die *x* -Koordinate für den Verankerungspunkt eines Steuerelements in lokalen Koordinaten dar.</span><span class="sxs-lookup"><span data-stu-id="a6233-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6233-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6233-105">Remarks</span></span>

<span data-ttu-id="a6233-106">Der Verankerungspunkt wird zum Rubber-Banding bei aktivierter Dynamik verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6233-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="a6233-107">Wenn Sie einen Verweis auf die Zelle X Dynamics aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a6233-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6233-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a6233-108">Cell name:</span></span>  <br/> | <span data-ttu-id="a6233-109">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="a6233-109">Controls.</span></span>  <span data-ttu-id="a6233-110">*Name* . XDynwhere-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="a6233-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="a6233-111">*Name* ist der Name der Zeile Controls.</span><span class="sxs-lookup"><span data-stu-id="a6233-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="a6233-112">Wenn Sie einen Verweis auf die Zelle X Dynamics nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a6233-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6233-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a6233-113">Section index:</span></span>  <br/> |<span data-ttu-id="a6233-114">**Konstanten visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="a6233-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="a6233-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a6233-115">Row index:</span></span>  <br/> |<span data-ttu-id="a6233-116">**visRowControl** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a6233-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a6233-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a6233-117">Cell index:</span></span>  <br/> |<span data-ttu-id="a6233-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="a6233-118">**visCtlXDyn**</span></span> <br/> |
   

