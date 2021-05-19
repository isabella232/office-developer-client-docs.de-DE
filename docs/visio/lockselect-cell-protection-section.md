---
title: Zelle "LockSelect" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Verhindert, dass ein Shape ausgewählt werden kann.
ms.openlocfilehash: c9f762f390dbea1e4ff2bd5bcf9566b8c67df11f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409755"
---
# <a name="lockselect-cell-protection-section"></a><span data-ttu-id="bbc3d-103">Zelle "LockSelect" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="bbc3d-103">LockSelect Cell (Protection Section)</span></span>

<span data-ttu-id="bbc3d-104">Verhindert, dass ein Shape ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bbc3d-104">Prevents a shape from being selected.</span></span>
  
|<span data-ttu-id="bbc3d-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bbc3d-105">**Value**</span></span>|<span data-ttu-id="bbc3d-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bbc3d-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bbc3d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bbc3d-107">TRUE</span></span>  <br/> | <span data-ttu-id="bbc3d-108">Shape kann nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="bbc3d-108">Shape cannot be selected.</span></span>  <br/> |
| <span data-ttu-id="bbc3d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bbc3d-109">FALSE</span></span>  <br/> | <span data-ttu-id="bbc3d-110">Shape kann ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="bbc3d-110">Shape can be selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbc3d-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bbc3d-111">Remarks</span></span>

<span data-ttu-id="bbc3d-112">Damit LockSelect wirksam wird, muss das Kontrollkästchen **Shapes** im Dialogfeld Dokument **schützen** aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="bbc3d-112">In order for LockSelect to take effect, the **Shapes** check box must be selected in the **Protect Document** dialog box.</span></span> 
  
<span data-ttu-id="bbc3d-113">Um einen Verweis auf die Zelle LockSelect anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="bbc3d-113">To get a reference to the LockSelect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bbc3d-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bbc3d-114">Cell name:</span></span>  <br/> | <span data-ttu-id="bbc3d-115">LockSelect</span><span class="sxs-lookup"><span data-stu-id="bbc3d-115">LockSelect</span></span>  <br/> |
   
<span data-ttu-id="bbc3d-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockSelect nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="bbc3d-116">To get a reference to the LockSelect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bbc3d-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bbc3d-117">Section index:</span></span>  <br/> |<span data-ttu-id="bbc3d-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bbc3d-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bbc3d-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bbc3d-119">Row index:</span></span>  <br/> |<span data-ttu-id="bbc3d-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="bbc3d-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="bbc3d-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bbc3d-121">Cell index:</span></span>  <br/> |<span data-ttu-id="bbc3d-122">**visLockSelect**</span><span class="sxs-lookup"><span data-stu-id="bbc3d-122">**visLockSelect**</span></span> <br/> |
   

