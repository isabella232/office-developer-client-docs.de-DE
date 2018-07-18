---
title: Zelle "HideText" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Blendet den Text für ein Shape aus. Sie können Text anzeigen, Eigenschaften ändern und Formatvorlagen auf den Text im Textblock anwenden. Die Änderungen werden jedoch erst übernommen, wenn Sie HideText auf FALSE (0) zurücksetzen.
ms.openlocfilehash: e2d220e9d7874382f2aaeade5488bd4809f3a9dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797159"
---
# <a name="hidetext-cell-miscellaneous-section"></a><span data-ttu-id="5b38c-104">HideText Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="5b38c-104">HideText Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="5b38c-p102">Blendet den Text für ein Shape aus. Sie können Text anzeigen, Eigenschaften ändern und Formatvorlagen auf den Text im Textblock anwenden. Die Änderungen werden jedoch erst übernommen, wenn Sie HideText auf FALSE (0) zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="5b38c-p102">Hides the text for a shape. You can view text, edit properties, and apply styles to the text in the text block, although the changes will not appear until you reset HideText to FALSE (0).</span></span>
  
|<span data-ttu-id="5b38c-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5b38c-107">**Value**</span></span>|<span data-ttu-id="5b38c-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b38c-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5b38c-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="5b38c-109">TRUE</span></span>  <br/> | <span data-ttu-id="5b38c-110">Text ist verborgen und wird nicht ausgedruckt.</span><span class="sxs-lookup"><span data-stu-id="5b38c-110">Text is hidden and does not print.</span></span>  <br/> |
| <span data-ttu-id="5b38c-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="5b38c-111">FALSE</span></span>  <br/> | <span data-ttu-id="5b38c-112">Text ist nicht verborgen.</span><span class="sxs-lookup"><span data-stu-id="5b38c-112">Text is not hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b38c-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5b38c-113">Remarks</span></span>

<span data-ttu-id="5b38c-114">Wenn Sie einen Verweis auf die Zelle "HideText" nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5b38c-114">To get a reference to the HideText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5b38c-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5b38c-115">Cell name:</span></span>  <br/> | <span data-ttu-id="5b38c-116">HideText</span><span class="sxs-lookup"><span data-stu-id="5b38c-116">HideText</span></span>  <br/> |
   
<span data-ttu-id="5b38c-117">Wenn Sie einen Verweis auf die Zelle "HideText" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5b38c-117">To get a reference to the HideText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5b38c-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5b38c-118">Section index:</span></span>  <br/> |<span data-ttu-id="5b38c-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5b38c-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5b38c-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5b38c-120">Row index:</span></span>  <br/> |<span data-ttu-id="5b38c-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="5b38c-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="5b38c-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5b38c-122">Cell index:</span></span>  <br/> |<span data-ttu-id="5b38c-123">**visHideText**</span><span class="sxs-lookup"><span data-stu-id="5b38c-123">**visHideText**</span></span> <br/> |
   

