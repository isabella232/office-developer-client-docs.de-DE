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
ms.openlocfilehash: 2b8fe7e2b0df09561d0db4367f917c8f4b71335d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439835"
---
# <a name="spafter-cell-paragraph-section"></a><span data-ttu-id="e354a-103">Zelle "SpAfter" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="e354a-103">SpAfter Cell (Paragraph Section)</span></span>

<span data-ttu-id="e354a-104">Legt den Platz fest, der zusätzlich zum Platz, der in der Zelle SpLine angegeben wurde, nach jedem Absatz im Textblock des Shapes eingefügt wird, wenn es sich um den letzten Absatz in einem Textblock handelt (die Zelle BottomMargin).</span><span class="sxs-lookup"><span data-stu-id="e354a-104">Determines the amount of space inserted after each paragraph in the shape's text block, in addition to any space from the SpLine cell and, if it is the last paragraph in a text block, the BottomMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e354a-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e354a-105">Remarks</span></span>

<span data-ttu-id="e354a-p101">Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn es sich um eine skalierte Zeichnung handelt, bleibt die Einstellung für Abstand nach unverändert.</span><span class="sxs-lookup"><span data-stu-id="e354a-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space After setting remains the same.</span></span>
  
<span data-ttu-id="e354a-108">Um einen Verweis auf die Zelle SpAfter anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="e354a-108">To get a reference to the SpAfter cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e354a-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e354a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="e354a-110">Para.SpAfter[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e354a-110">Para.SpAfter[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e354a-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle SpAfter nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="e354a-111">To get a reference to the SpAfter cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e354a-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e354a-112">Section index:</span></span>  <br/> |<span data-ttu-id="e354a-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="e354a-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="e354a-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e354a-114">Row index:</span></span>  <br/> |<span data-ttu-id="e354a-115">**visRowParagraph**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e354a-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e354a-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e354a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e354a-117">**visSpaceAfter**</span><span class="sxs-lookup"><span data-stu-id="e354a-117">**visSpaceAfter**</span></span> <br/> |
   

