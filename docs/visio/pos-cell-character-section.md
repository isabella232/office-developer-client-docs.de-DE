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
ms.openlocfilehash: 50ce5a3f7caf3e716f430aa08326281c8dc847f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797714"
---
# <a name="pos-cell-character-section"></a><span data-ttu-id="63678-103">Zelle "Pos" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="63678-103">Pos Cell (Character Section)</span></span>

<span data-ttu-id="63678-104">Bestimmt die Position des Shape-Texts relativ zur Grundlinie.</span><span class="sxs-lookup"><span data-stu-id="63678-104">Determines the position of the shape's text relative to the baseline.</span></span>
  
|<span data-ttu-id="63678-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="63678-105">**Value**</span></span>|<span data-ttu-id="63678-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63678-106">**Description**</span></span>|<span data-ttu-id="63678-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="63678-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="63678-108">0</span><span class="sxs-lookup"><span data-stu-id="63678-108">0</span></span>  <br/> | <span data-ttu-id="63678-109">Normale Position</span><span class="sxs-lookup"><span data-stu-id="63678-109">Normal position</span></span>  <br/> |<span data-ttu-id="63678-110">**visPosNormal**</span><span class="sxs-lookup"><span data-stu-id="63678-110">**visPosNormal**</span></span> <br/> |
| <span data-ttu-id="63678-111">1</span><span class="sxs-lookup"><span data-stu-id="63678-111">1</span></span>  <br/> | <span data-ttu-id="63678-112">Hochgestellt</span><span class="sxs-lookup"><span data-stu-id="63678-112">Superscript</span></span>  <br/> |<span data-ttu-id="63678-113">**visPosSuper**</span><span class="sxs-lookup"><span data-stu-id="63678-113">**visPosSuper**</span></span> <br/> |
| <span data-ttu-id="63678-114">2</span><span class="sxs-lookup"><span data-stu-id="63678-114">2</span></span>  <br/> | <span data-ttu-id="63678-115">Tiefgestellt</span><span class="sxs-lookup"><span data-stu-id="63678-115">Subscript</span></span>  <br/> |<span data-ttu-id="63678-116">**visPosSub**</span><span class="sxs-lookup"><span data-stu-id="63678-116">**visPosSub**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63678-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="63678-117">Remarks</span></span>

<span data-ttu-id="63678-118">Wenn Sie einen Verweis auf die Zelle Pos nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="63678-118">To get a reference to the Pos cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="63678-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="63678-119">Cell name:</span></span>  <br/> | <span data-ttu-id="63678-120">Zeichen.POS [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="63678-120">Char.Pos[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="63678-121">Wenn Sie einen Verweis auf die Zelle Pos aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="63678-121">To get a reference to the Pos cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="63678-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="63678-122">Section index:</span></span>  <br/> |<span data-ttu-id="63678-123">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="63678-123">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="63678-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="63678-124">Row index:</span></span>  <br/> |<span data-ttu-id="63678-125">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="63678-125">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="63678-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="63678-126">Cell index:</span></span>  <br/> |<span data-ttu-id="63678-127">**visCharacterPos**</span><span class="sxs-lookup"><span data-stu-id="63678-127">**visCharacterPos**</span></span> <br/> |
   

