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
description: Represents the x -coordinate for a control handle's anchor point in local coordinates.
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432128"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="5b314-103">Zelle "X Dynamics" (Abschnitt "Controls")</span><span class="sxs-lookup"><span data-stu-id="5b314-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="5b314-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span><span class="sxs-lookup"><span data-stu-id="5b314-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5b314-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5b314-105">Remarks</span></span>

<span data-ttu-id="5b314-106">Der Verankerungspunkt wird zum Rubber-Banding bei aktivierter Dynamik verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b314-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="5b314-107">Um einen Verweis auf die X Dynamics-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="5b314-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5b314-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5b314-108">Cell name:</span></span>  <br/> | <span data-ttu-id="5b314-109">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="5b314-109">Controls.</span></span>  <span data-ttu-id="5b314-110">*Name*  . XDynwhere-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="5b314-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="5b314-111">*name*  ist der Name der Steuerelementzeile.</span><span class="sxs-lookup"><span data-stu-id="5b314-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="5b314-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die X Dynamics-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="5b314-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5b314-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5b314-113">Section index:</span></span>  <br/> |<span data-ttu-id="5b314-114">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="5b314-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="5b314-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5b314-115">Row index:</span></span>  <br/> |<span data-ttu-id="5b314-116">**visRowControl**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5b314-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5b314-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5b314-117">Cell index:</span></span>  <br/> |<span data-ttu-id="5b314-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="5b314-118">**visCtlXDyn**</span></span> <br/> |
   

