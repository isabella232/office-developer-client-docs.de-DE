---
title: Zelle "Color" (Abschnitt "Reviewer")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Ein RGB-Wert, der die Farbe darstellt, die dem Markup eines Dokument Bearbeiters zugewiesen ist.
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341818"
---
# <a name="color-cell-reviewer-section"></a><span data-ttu-id="9028c-103">Zelle "Color" (Abschnitt "Reviewer")</span><span class="sxs-lookup"><span data-stu-id="9028c-103">Color Cell (Reviewer Section)</span></span>

<span data-ttu-id="9028c-104">Ein RGB-Wert, der die Farbe darstellt, die dem Markup eines Dokument Bearbeiters zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9028c-104">An RGB value that represents the color assigned to a document reviewer's markup.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9028c-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9028c-105">Remarks</span></span>

<span data-ttu-id="9028c-p101">Farben werden Bearbeitern in der folgenden Reihenfolge zugewiesen: Rot, Blau, Grün, Violett, Orange, Türkis, Grau. Diese Farben werden für alle verbleibenden Bearbeiter erneut durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="9028c-p101">Colors are assigned to reviewers in the following sequence: red, blue, green, violet, orange, turquoise, gray. These colors are cycled through again for any remaining reviewers.</span></span> 
  
<span data-ttu-id="9028c-108">Kommentare auf dem ursprünglichen Zeichenblatt weisen stets die Farbe Gelb auf, ungeachtet der Farbe, die einem Bearbeiter in der Zelle Color zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9028c-108">Comments entered on the original drawing page are always colored yellow, regardless of the color assigned to a reviewer in the Color cell.</span></span> 
  
<span data-ttu-id="9028c-109">Wenn Sie einen Verweis auf die Zelle Farbe aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9028c-109">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9028c-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9028c-110">Cell name:</span></span>  <br/> | <span data-ttu-id="9028c-111">Prüfer. Color [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9028c-111">Reviewer.Color [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9028c-112">Wenn Sie einen Verweis auf die Zelle Color nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9028c-112">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9028c-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9028c-113">Section index:</span></span>  <br/> |<span data-ttu-id="9028c-114">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="9028c-114">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="9028c-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9028c-115">Row index:</span></span>  <br/> |<span data-ttu-id="9028c-116">**visRowReviewer** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9028c-116">**visRowReviewer** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9028c-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9028c-117">Cell index:</span></span>  <br/> |<span data-ttu-id="9028c-118">**visReviewerColor**</span><span class="sxs-lookup"><span data-stu-id="9028c-118">**visReviewerColor**</span></span> <br/> |
   

