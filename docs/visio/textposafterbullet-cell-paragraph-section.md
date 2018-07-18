---
title: Zelle "TextPosAfterBullet" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Stellt den Abstand zwischen der ersten Zeile des Absatzes und dem Aufzählungszeichen dar.
ms.openlocfilehash: fe22b81113ab6537922ad4627aa53f34f2e62c48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798254"
---
# <a name="textposafterbullet-cell-paragraph-section"></a><span data-ttu-id="12c56-103">TextPosAfterBullet Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="12c56-103">TextPosAfterBullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="12c56-104">Stellt den Abstand zwischen der ersten Zeile des Absatzes und dem Aufzählungszeichen dar.</span><span class="sxs-lookup"><span data-stu-id="12c56-104">Represents the distance between the first line of the paragraph and the bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="12c56-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="12c56-105">Remarks</span></span>

<span data-ttu-id="12c56-p101">Dieser Abstand wird zum Abstand in der Zelle IndFirst addiert, der den Standardeinzug links darstellt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab.</span><span class="sxs-lookup"><span data-stu-id="12c56-p101">This distance is added to the distance contained in the IndFirst cell, which is the default left indent. This value is independent of the scale of the drawing.</span></span> 
  
<span data-ttu-id="12c56-108">Wenn Sie einen Verweis auf die Zelle TextPosAfterBullet aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="12c56-108">To get a reference to the TextPosAfterBullet cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12c56-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="12c56-109">Cell name:</span></span>  <br/> | <span data-ttu-id="12c56-110">Para.TextPosAfterBullet [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="12c56-110">Para.TextPosAfterBullet[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="12c56-111">Wenn Sie einen Verweis auf die Zelle TextPosAfterBullet aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="12c56-111">To get a reference to the TextPosAfterBullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12c56-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="12c56-112">Section index:</span></span>  <br/> |<span data-ttu-id="12c56-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="12c56-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="12c56-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="12c56-114">Row index:</span></span>  <br/> |<span data-ttu-id="12c56-115">**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="12c56-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="12c56-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="12c56-116">Cell index:</span></span>  <br/> |<span data-ttu-id="12c56-117">**visTextPosAfterBullet**</span><span class="sxs-lookup"><span data-stu-id="12c56-117">**visTextPosAfterBullet**</span></span> <br/> |
   

