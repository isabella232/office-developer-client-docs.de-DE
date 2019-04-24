---
title: Zelle "BeginArrow" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem ersten Scheitelpunkt hat. Geben Sie eine Zahl zwischen 0 und 45 oder die USE-Funktion zusammen mit dem Namen des benutzerdefinierten Linienendes ein, oder verwenden Sie das Dialogfeld Linie.
ms.openlocfilehash: cf5a512dabd0e6296b83fa7bfd2a2a6134143d50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346235"
---
# <a name="beginarrow-cell-line-format-section"></a><span data-ttu-id="db849-104">Zelle "BeginArrow" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="db849-104">BeginArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="db849-p102">Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem ersten Scheitelpunkt hat. Geben Sie eine Zahl zwischen 0 und 45 oder die USE-Funktion zusammen mit dem Namen des benutzerdefinierten Linienendes ein, oder verwenden Sie das Dialogfeld **Linie**.</span><span class="sxs-lookup"><span data-stu-id="db849-p102">Indicates whether a line has an arrowhead or other line end format at its first vertex. Enter a number from 0 to 45 or the USE function with the name of a custom line end, or use the **Line** dialog box.</span></span> 
  
|<span data-ttu-id="db849-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="db849-107">**Value**</span></span>|<span data-ttu-id="db849-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db849-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="db849-109">0</span><span class="sxs-lookup"><span data-stu-id="db849-109">0</span></span>  <br/> | <span data-ttu-id="db849-110">Keine Pfeilspitze</span><span class="sxs-lookup"><span data-stu-id="db849-110">No arrowhead.</span></span>  <br/> |
| <span data-ttu-id="db849-111">1 - 45</span><span class="sxs-lookup"><span data-stu-id="db849-111">1 - 45</span></span>  <br/> | <span data-ttu-id="db849-112">Verschiedene Pfeilspitzenformatvorlagen, die den indizierten Einträgen im Dialogfeld **Linie** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="db849-112">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db849-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db849-113">Remarks</span></span>

<span data-ttu-id="db849-114">Die Größe der Pfeilspitze wird in der Zelle PfeilBeginnGröße angegeben.</span><span class="sxs-lookup"><span data-stu-id="db849-114">The size of the arrowhead is set in the BeginArrowSize cell.</span></span>
  
<span data-ttu-id="db849-115">Wenn Sie einen Verweis auf die Zelle beginArrow aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="db849-115">To get a reference to the BeginArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="db849-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="db849-116">Cell name:</span></span>  <br/> | <span data-ttu-id="db849-117">Zelle BeginArrow</span><span class="sxs-lookup"><span data-stu-id="db849-117">BeginArrow</span></span>  <br/> |
   
<span data-ttu-id="db849-118">Wenn Sie einen Verweis auf die Zelle beginArrow aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="db849-118">To get a reference to the BeginArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="db849-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="db849-119">Section index:</span></span>  <br/> |<span data-ttu-id="db849-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="db849-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="db849-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="db849-121">Row index:</span></span>  <br/> |<span data-ttu-id="db849-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="db849-122">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="db849-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="db849-123">Cell index:</span></span>  <br/> |<span data-ttu-id="db849-124">**visLineBeginArrow**</span><span class="sxs-lookup"><span data-stu-id="db849-124">**visLineBeginArrow**</span></span> <br/> |
   

