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
ms.openlocfilehash: 3e1be814984ed15247c451f5cd86d0f7a6dba71a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425484"
---
# <a name="hidetext-cell-miscellaneous-section"></a><span data-ttu-id="71dc0-104">Zelle "HideText" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="71dc0-104">HideText Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="71dc0-p102">Blendet den Text für ein Shape aus. Sie können Text anzeigen, Eigenschaften ändern und Formatvorlagen auf den Text im Textblock anwenden. Die Änderungen werden jedoch erst übernommen, wenn Sie HideText auf FALSE (0) zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="71dc0-p102">Hides the text for a shape. You can view text, edit properties, and apply styles to the text in the text block, although the changes will not appear until you reset HideText to FALSE (0).</span></span>
  
|<span data-ttu-id="71dc0-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="71dc0-107">**Value**</span></span>|<span data-ttu-id="71dc0-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="71dc0-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="71dc0-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="71dc0-109">TRUE</span></span>  <br/> | <span data-ttu-id="71dc0-110">Text ist verborgen und wird nicht ausgedruckt.</span><span class="sxs-lookup"><span data-stu-id="71dc0-110">Text is hidden and does not print.</span></span>  <br/> |
| <span data-ttu-id="71dc0-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="71dc0-111">FALSE</span></span>  <br/> | <span data-ttu-id="71dc0-112">Text ist nicht verborgen.</span><span class="sxs-lookup"><span data-stu-id="71dc0-112">Text is not hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71dc0-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="71dc0-113">Remarks</span></span>

<span data-ttu-id="71dc0-114">Um einen Verweis auf die Zelle HideText anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="71dc0-114">To get a reference to the HideText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71dc0-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="71dc0-115">Cell name:</span></span>  <br/> | <span data-ttu-id="71dc0-116">HideText</span><span class="sxs-lookup"><span data-stu-id="71dc0-116">HideText</span></span>  <br/> |
   
<span data-ttu-id="71dc0-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die HideText-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="71dc0-117">To get a reference to the HideText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71dc0-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="71dc0-118">Section index:</span></span>  <br/> |<span data-ttu-id="71dc0-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="71dc0-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="71dc0-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="71dc0-120">Row index:</span></span>  <br/> |<span data-ttu-id="71dc0-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="71dc0-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="71dc0-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="71dc0-122">Cell index:</span></span>  <br/> |<span data-ttu-id="71dc0-123">**visHideText**</span><span class="sxs-lookup"><span data-stu-id="71dc0-123">**visHideText**</span></span> <br/> |
   

