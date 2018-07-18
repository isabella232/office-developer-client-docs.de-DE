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
ms.openlocfilehash: c6d5a66d76cfea61b1c9923c5b904dadec5495f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796418"
---
# <a name="beginarrow-cell-line-format-section"></a><span data-ttu-id="29011-104">BeginArrow Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="29011-104">BeginArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="29011-p102">Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem ersten Scheitelpunkt hat. Geben Sie eine Zahl zwischen 0 und 45 oder die USE-Funktion zusammen mit dem Namen des benutzerdefinierten Linienendes ein, oder verwenden Sie das Dialogfeld **Linie**.</span><span class="sxs-lookup"><span data-stu-id="29011-p102">Indicates whether a line has an arrowhead or other line end format at its first vertex. Enter a number from 0 to 45 or the USE function with the name of a custom line end, or use the **Line** dialog box.</span></span> 
  
|<span data-ttu-id="29011-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="29011-107">**Value**</span></span>|<span data-ttu-id="29011-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="29011-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="29011-109">0</span><span class="sxs-lookup"><span data-stu-id="29011-109">0</span></span>  <br/> | <span data-ttu-id="29011-110">Keine Pfeilspitze</span><span class="sxs-lookup"><span data-stu-id="29011-110">No arrowhead.</span></span>  <br/> |
| <span data-ttu-id="29011-111">1 – 45</span><span class="sxs-lookup"><span data-stu-id="29011-111">1 - 45</span></span>  <br/> | <span data-ttu-id="29011-112">Verschiedene Pfeilspitzenformatvorlagen, die den indizierten Einträgen im Dialogfeld **Linie** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="29011-112">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29011-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="29011-113">Remarks</span></span>

<span data-ttu-id="29011-114">Die Größe der Pfeilspitze wird in der Zelle PfeilBeginnGröße angegeben.</span><span class="sxs-lookup"><span data-stu-id="29011-114">The size of the arrowhead is set in the BeginArrowSize cell.</span></span>
  
<span data-ttu-id="29011-115">Wenn Sie einen Verweis auf die Zelle BeginArrow aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="29011-115">To get a reference to the BeginArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="29011-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="29011-116">Cell name:</span></span>  <br/> | <span data-ttu-id="29011-117">BeginArrow</span><span class="sxs-lookup"><span data-stu-id="29011-117">BeginArrow</span></span>  <br/> |
   
<span data-ttu-id="29011-118">Wenn Sie einen Verweis auf die Zelle BeginArrow aus einem Programm nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="29011-118">To get a reference to the BeginArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="29011-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="29011-119">Section index:</span></span>  <br/> |<span data-ttu-id="29011-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="29011-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="29011-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="29011-121">Row index:</span></span>  <br/> |<span data-ttu-id="29011-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="29011-122">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="29011-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="29011-123">Cell index:</span></span>  <br/> |<span data-ttu-id="29011-124">**visLineBeginArrow**</span><span class="sxs-lookup"><span data-stu-id="29011-124">**visLineBeginArrow**</span></span> <br/> |
   

