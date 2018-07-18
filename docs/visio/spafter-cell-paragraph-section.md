---
title: Zelle "SpAfter" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
localization_priority: Normal
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: Legt den Platz fest, der zusätzlich zum Platz, der in der Zelle SpLine angegeben wurde, nach jedem Absatz im Textblock des Shapes eingefügt wird, wenn es sich um den letzten Absatz in einem Textblock handelt (die Zelle BottomMargin).
ms.openlocfilehash: 93db93e58124b5f176fb57f843580eff6a3d4d3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798196"
---
# <a name="spafter-cell-paragraph-section"></a><span data-ttu-id="307d5-103">SpAfter Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="307d5-103">SpAfter Cell (Paragraph Section)</span></span>

<span data-ttu-id="307d5-104">Legt den Platz fest, der zusätzlich zum Platz, der in der Zelle SpLine angegeben wurde, nach jedem Absatz im Textblock des Shapes eingefügt wird, wenn es sich um den letzten Absatz in einem Textblock handelt (die Zelle BottomMargin).</span><span class="sxs-lookup"><span data-stu-id="307d5-104">Determines the amount of space inserted after each paragraph in the shape's text block, in addition to any space from the SpLine cell and, if it is the last paragraph in a text block, the BottomMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="307d5-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="307d5-105">Remarks</span></span>

<span data-ttu-id="307d5-p101">Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn es sich um eine skalierte Zeichnung handelt, bleibt die Einstellung für Abstand nach unverändert.</span><span class="sxs-lookup"><span data-stu-id="307d5-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space After setting remains the same.</span></span>
  
<span data-ttu-id="307d5-108">Wenn Sie einen Verweis auf die Zelle SpAfter aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="307d5-108">To get a reference to the SpAfter cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="307d5-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="307d5-109">Cell name:</span></span>  <br/> | <span data-ttu-id="307d5-110">Para.SpAfter [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="307d5-110">Para.SpAfter[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="307d5-111">Wenn Sie einen Verweis auf die Zelle SpAfter aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="307d5-111">To get a reference to the SpAfter cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="307d5-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="307d5-112">Section index:</span></span>  <br/> |<span data-ttu-id="307d5-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="307d5-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="307d5-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="307d5-114">Row index:</span></span>  <br/> |<span data-ttu-id="307d5-115">**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="307d5-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="307d5-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="307d5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="307d5-117">**visSpaceAfter**</span><span class="sxs-lookup"><span data-stu-id="307d5-117">**visSpaceAfter**</span></span> <br/> |
   

