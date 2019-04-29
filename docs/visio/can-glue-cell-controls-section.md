---
title: Zelle "Can Glue" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423293"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="d8b7c-103">Zelle "Can Glue" (Abschnitt "Controls")</span><span class="sxs-lookup"><span data-stu-id="d8b7c-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="d8b7c-104">Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="d8b7c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d8b7c-105">**Value**</span></span>|<span data-ttu-id="d8b7c-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8b7c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d8b7c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d8b7c-107">TRUE</span></span>  <br/> | <span data-ttu-id="d8b7c-108">Steuerpunkt kann geklebt werden.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="d8b7c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d8b7c-109">FALSE</span></span>  <br/> | <span data-ttu-id="d8b7c-110">Steuerpunkt kann nicht geklebt werden.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8b7c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8b7c-111">Remarks</span></span>

<span data-ttu-id="d8b7c-112">Wenn Sie einen Bezug auf die Zelle can Glue aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d8b7c-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d8b7c-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d8b7c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d8b7c-114">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-114">Controls.</span></span>  <span data-ttu-id="d8b7c-115">*Name* . CanGluewhere-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="d8b7c-116">*Name* ist der Name der Zeile Controls.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="d8b7c-117">Wenn Sie einen Verweis auf die Zelle can Glue aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d8b7c-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d8b7c-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d8b7c-118">Section index:</span></span>  <br/> |<span data-ttu-id="d8b7c-119">**Konstanten visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="d8b7c-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="d8b7c-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d8b7c-120">Row index:</span></span>  <br/> |<span data-ttu-id="d8b7c-121">**visRowControl** +  *i* , wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="d8b7c-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="d8b7c-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d8b7c-122">Cell index:</span></span>  <br/> |<span data-ttu-id="d8b7c-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="d8b7c-123">**visCtlGlue**</span></span> <br/> |
   

