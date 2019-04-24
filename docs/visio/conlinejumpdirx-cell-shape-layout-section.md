---
title: Zelle "ConLineJumpDirX" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem horizontalen dynamischen Verbinder für ein Shape auftreten.
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342749"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="8e505-103">Zelle "ConLineJumpDirX" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="8e505-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="8e505-104">Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem horizontalen dynamischen Verbinder für ein Shape auftreten.</span><span class="sxs-lookup"><span data-stu-id="8e505-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="8e505-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8e505-105">**Value**</span></span>|<span data-ttu-id="8e505-106">**Liniensprungrichtung**</span><span class="sxs-lookup"><span data-stu-id="8e505-106">**Line jump direction**</span></span>|<span data-ttu-id="8e505-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="8e505-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8e505-108">0</span><span class="sxs-lookup"><span data-stu-id="8e505-108">0</span></span>  <br/> | <span data-ttu-id="8e505-109">Zeichenblattstandard</span><span class="sxs-lookup"><span data-stu-id="8e505-109">Page default</span></span>  <br/> |<span data-ttu-id="8e505-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="8e505-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="8e505-111">1</span><span class="sxs-lookup"><span data-stu-id="8e505-111">1</span></span>  <br/> | <span data-ttu-id="8e505-112">Nach oben</span><span class="sxs-lookup"><span data-stu-id="8e505-112">Up</span></span>  <br/> |<span data-ttu-id="8e505-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="8e505-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="8e505-114">2</span><span class="sxs-lookup"><span data-stu-id="8e505-114">2</span></span>  <br/> | <span data-ttu-id="8e505-115">Nach unten</span><span class="sxs-lookup"><span data-stu-id="8e505-115">Down</span></span>  <br/> |<span data-ttu-id="8e505-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="8e505-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e505-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e505-117">Remarks</span></span>

<span data-ttu-id="8e505-118">Wenn Sie die standardmäßige horizontale Richtung für *alle* Verbinder auf einem Zeichenblatt festlegen möchten, verwenden Sie die Zelle Zelle PageLineJumpDirX im Abschnitt Seiten Layout.</span><span class="sxs-lookup"><span data-stu-id="8e505-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="8e505-119">Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpDirX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8e505-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e505-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8e505-120">Cell name:</span></span>  <br/> | <span data-ttu-id="8e505-121">Zelle ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="8e505-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="8e505-122">Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpDirX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8e505-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e505-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8e505-123">Section index:</span></span>  <br/> |<span data-ttu-id="8e505-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8e505-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8e505-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8e505-125">Row index:</span></span>  <br/> |<span data-ttu-id="8e505-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="8e505-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="8e505-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8e505-127">Cell index:</span></span>  <br/> |<span data-ttu-id="8e505-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="8e505-128">**visSLOJumpDirX**</span></span> <br/> |
   

