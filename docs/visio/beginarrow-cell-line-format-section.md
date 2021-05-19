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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410294"
---
# <a name="beginarrow-cell-line-format-section"></a><span data-ttu-id="85cfe-104">Zelle "BeginArrow" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="85cfe-104">BeginArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="85cfe-p102">Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem ersten Scheitelpunkt hat. Geben Sie eine Zahl zwischen 0 und 45 oder die USE-Funktion zusammen mit dem Namen des benutzerdefinierten Linienendes ein, oder verwenden Sie das Dialogfeld **Linie**.</span><span class="sxs-lookup"><span data-stu-id="85cfe-p102">Indicates whether a line has an arrowhead or other line end format at its first vertex. Enter a number from 0 to 45 or the USE function with the name of a custom line end, or use the **Line** dialog box.</span></span> 
  
|<span data-ttu-id="85cfe-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="85cfe-107">**Value**</span></span>|<span data-ttu-id="85cfe-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85cfe-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="85cfe-109">0</span><span class="sxs-lookup"><span data-stu-id="85cfe-109">0</span></span>  <br/> | <span data-ttu-id="85cfe-110">Keine Pfeilspitze</span><span class="sxs-lookup"><span data-stu-id="85cfe-110">No arrowhead.</span></span>  <br/> |
| <span data-ttu-id="85cfe-111">1 - 45</span><span class="sxs-lookup"><span data-stu-id="85cfe-111">1 - 45</span></span>  <br/> | <span data-ttu-id="85cfe-112">Verschiedene Pfeilspitzenformatvorlagen, die den indizierten Einträgen im Dialogfeld **Linie** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="85cfe-112">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85cfe-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="85cfe-113">Remarks</span></span>

<span data-ttu-id="85cfe-114">Die Größe der Pfeilspitze wird in der Zelle PfeilBeginnGröße angegeben.</span><span class="sxs-lookup"><span data-stu-id="85cfe-114">The size of the arrowhead is set in the BeginArrowSize cell.</span></span>
  
<span data-ttu-id="85cfe-115">Um einen Verweis auf die Zelle BeginArrow anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="85cfe-115">To get a reference to the BeginArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="85cfe-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="85cfe-116">Cell name:</span></span>  <br/> | <span data-ttu-id="85cfe-117">BeginArrow</span><span class="sxs-lookup"><span data-stu-id="85cfe-117">BeginArrow</span></span>  <br/> |
   
<span data-ttu-id="85cfe-118">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die BeginArrow-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="85cfe-118">To get a reference to the BeginArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="85cfe-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="85cfe-119">Section index:</span></span>  <br/> |<span data-ttu-id="85cfe-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="85cfe-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="85cfe-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="85cfe-121">Row index:</span></span>  <br/> |<span data-ttu-id="85cfe-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="85cfe-122">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="85cfe-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="85cfe-123">Cell index:</span></span>  <br/> |<span data-ttu-id="85cfe-124">**visLineBeginArrow**</span><span class="sxs-lookup"><span data-stu-id="85cfe-124">**visLineBeginArrow**</span></span> <br/> |
   

