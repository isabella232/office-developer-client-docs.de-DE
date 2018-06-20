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
ms.openlocfilehash: c7b6764e25deab3345b7b3cecd6cf12dde74a84c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796553"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="80ca5-103">Can Glue Cell (Controls Section)</span><span class="sxs-lookup"><span data-stu-id="80ca5-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="80ca5-104">Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.</span><span class="sxs-lookup"><span data-stu-id="80ca5-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="80ca5-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="80ca5-105">**Value**</span></span>|<span data-ttu-id="80ca5-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80ca5-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="80ca5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="80ca5-107">TRUE</span></span>  <br/> | <span data-ttu-id="80ca5-108">Steuerpunkt kann geklebt werden.</span><span class="sxs-lookup"><span data-stu-id="80ca5-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="80ca5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="80ca5-109">FALSE</span></span>  <br/> | <span data-ttu-id="80ca5-110">Steuerpunkt kann nicht geklebt werden.</span><span class="sxs-lookup"><span data-stu-id="80ca5-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80ca5-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80ca5-111">Remarks</span></span>

<span data-ttu-id="80ca5-112">Wenn Sie einen Verweis auf die Zelle Can Glue nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="80ca5-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="80ca5-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="80ca5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="80ca5-114">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="80ca5-114">Controls.</span></span>  <span data-ttu-id="80ca5-115">*Name* . CanGluewhere-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="80ca5-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="80ca5-116">*Name* ist der Name der Zeile mit Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="80ca5-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="80ca5-117">Wenn Sie einen Verweis auf die Zelle Can Glue aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="80ca5-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="80ca5-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="80ca5-118">Section index:</span></span>  <br/> |<span data-ttu-id="80ca5-119">**Konstanten visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="80ca5-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="80ca5-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="80ca5-120">Row index:</span></span>  <br/> |<span data-ttu-id="80ca5-121">**VisRowControl** +  *i* wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="80ca5-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="80ca5-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="80ca5-122">Cell index:</span></span>  <br/> |<span data-ttu-id="80ca5-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="80ca5-123">**visCtlGlue**</span></span> <br/> |
   

