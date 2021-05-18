---
title: Zelle "Pos" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: Bestimmt die Position des Shape-Texts relativ zur Grundlinie.
ms.openlocfilehash: d5f6823d6f55493095d29054745f62b579a47893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414018"
---
# <a name="pos-cell-character-section"></a><span data-ttu-id="45611-103">Zelle "Pos" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="45611-103">Pos Cell (Character Section)</span></span>

<span data-ttu-id="45611-104">Bestimmt die Position des Shape-Texts relativ zur Grundlinie.</span><span class="sxs-lookup"><span data-stu-id="45611-104">Determines the position of the shape's text relative to the baseline.</span></span>
  
|<span data-ttu-id="45611-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="45611-105">**Value**</span></span>|<span data-ttu-id="45611-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="45611-106">**Description**</span></span>|<span data-ttu-id="45611-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="45611-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="45611-108">0</span><span class="sxs-lookup"><span data-stu-id="45611-108">0</span></span>  <br/> | <span data-ttu-id="45611-109">Normale Position</span><span class="sxs-lookup"><span data-stu-id="45611-109">Normal position</span></span>  <br/> |<span data-ttu-id="45611-110">**visPosNormal**</span><span class="sxs-lookup"><span data-stu-id="45611-110">**visPosNormal**</span></span> <br/> |
| <span data-ttu-id="45611-111">1</span><span class="sxs-lookup"><span data-stu-id="45611-111">1</span></span>  <br/> | <span data-ttu-id="45611-112">Hochgestellt</span><span class="sxs-lookup"><span data-stu-id="45611-112">Superscript</span></span>  <br/> |<span data-ttu-id="45611-113">**visPosSuper**</span><span class="sxs-lookup"><span data-stu-id="45611-113">**visPosSuper**</span></span> <br/> |
| <span data-ttu-id="45611-114">2</span><span class="sxs-lookup"><span data-stu-id="45611-114">2</span></span>  <br/> | <span data-ttu-id="45611-115">Tiefgestellt</span><span class="sxs-lookup"><span data-stu-id="45611-115">Subscript</span></span>  <br/> |<span data-ttu-id="45611-116">**visPosSub**</span><span class="sxs-lookup"><span data-stu-id="45611-116">**visPosSub**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45611-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45611-117">Remarks</span></span>

<span data-ttu-id="45611-118">Um einen Verweis auf die Zelle Pos anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="45611-118">To get a reference to the Pos cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="45611-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="45611-119">Cell name:</span></span>  <br/> | <span data-ttu-id="45611-120">Char.Pos[  *i*  ] wobei  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="45611-120">Char.Pos[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="45611-121">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Pos nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="45611-121">To get a reference to the Pos cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="45611-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="45611-122">Section index:</span></span>  <br/> |<span data-ttu-id="45611-123">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="45611-123">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="45611-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="45611-124">Row index:</span></span>  <br/> |<span data-ttu-id="45611-125">**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="45611-125">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="45611-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="45611-126">Cell index:</span></span>  <br/> |<span data-ttu-id="45611-127">**visCharacterPos**</span><span class="sxs-lookup"><span data-stu-id="45611-127">**visCharacterPos**</span></span> <br/> |
   

