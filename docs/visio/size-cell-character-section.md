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
ms.openlocfilehash: f3077441844b859cf224eccc8180d0d56cce851f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798120"
---
# <a name="size-cell-character-section"></a><span data-ttu-id="a0206-103">Size Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="a0206-103">Size Cell (Character Section)</span></span>

<span data-ttu-id="a0206-104">Definiert die Größe des Texts im Textblock des Shapes.</span><span class="sxs-lookup"><span data-stu-id="a0206-104">Determines the size of the text in the shape's text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0206-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a0206-105">Remarks</span></span>

<span data-ttu-id="a0206-p101">Die Größe des Texts ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Textgröße unverändert.</span><span class="sxs-lookup"><span data-stu-id="a0206-p101">The text's size is independent of the scale of the drawing. If the drawing is scaled, the text size remains the same.</span></span>
  
<span data-ttu-id="a0206-108">Wenn Sie einen Verweis auf die Zelle Size aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a0206-108">To get a reference to the Size cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a0206-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a0206-109">Cell name:</span></span>  <br/> | <span data-ttu-id="a0206-110">Char.Size [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a0206-110">Char.Size[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a0206-111">Wenn Sie einen Verweis auf die Zelle Size aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a0206-111">To get a reference to the Size cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a0206-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a0206-112">Section index:</span></span>  <br/> |<span data-ttu-id="a0206-113">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="a0206-113">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="a0206-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a0206-114">Row index:</span></span>  <br/> |<span data-ttu-id="a0206-115">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a0206-115">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a0206-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a0206-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a0206-117">**visCharacterSize**</span><span class="sxs-lookup"><span data-stu-id="a0206-117">**visCharacterSize**</span></span> <br/> |
   

