---
title: Zelle "Size" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
localization_priority: Normal
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: Definiert die Größe des Texts im Textblock des Shapes.
ms.openlocfilehash: ea747620301a07cafaf179106b54510edb95f7ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415600"
---
# <a name="size-cell-character-section"></a><span data-ttu-id="c5f8a-103">Zelle "Size" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="c5f8a-103">Size Cell (Character Section)</span></span>

<span data-ttu-id="c5f8a-104">Definiert die Größe des Texts im Textblock des Shapes.</span><span class="sxs-lookup"><span data-stu-id="c5f8a-104">Determines the size of the text in the shape's text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5f8a-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5f8a-105">Remarks</span></span>

<span data-ttu-id="c5f8a-p101">Die Größe des Texts ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Textgröße unverändert.</span><span class="sxs-lookup"><span data-stu-id="c5f8a-p101">The text's size is independent of the scale of the drawing. If the drawing is scaled, the text size remains the same.</span></span>
  
<span data-ttu-id="c5f8a-108">Um einen Verweis auf die Zelle Size anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="c5f8a-108">To get a reference to the Size cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c5f8a-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c5f8a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c5f8a-110">Char.Size[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c5f8a-110">Char.Size[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c5f8a-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Size nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="c5f8a-111">To get a reference to the Size cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c5f8a-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c5f8a-112">Section index:</span></span>  <br/> |<span data-ttu-id="c5f8a-113">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="c5f8a-113">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="c5f8a-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c5f8a-114">Row index:</span></span>  <br/> |<span data-ttu-id="c5f8a-115">**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c5f8a-115">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c5f8a-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c5f8a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c5f8a-117">**visCharacterSize**</span><span class="sxs-lookup"><span data-stu-id="c5f8a-117">**visCharacterSize**</span></span> <br/> |
   

