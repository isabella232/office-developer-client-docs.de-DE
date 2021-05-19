---
title: Zelle "Comment" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm170
localization_priority: Normal
ms.assetid: 6f52ed60-d58b-86e6-f7e2-2ef19d4afa75
description: Enthält den Kommentartext im Zeichenformat für ein Shape.
ms.openlocfilehash: e6f21875928bce31dc2004d88f2d281e31265d65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419065"
---
# <a name="comment-cell-miscellaneous-section"></a><span data-ttu-id="e80fc-103">Zelle "Comment" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="e80fc-103">Comment Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="e80fc-104">Enthält den Kommentartext im Zeichenformat für ein Shape.</span><span class="sxs-lookup"><span data-stu-id="e80fc-104">Contains the comment text in string format for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e80fc-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e80fc-105">Remarks</span></span>

<span data-ttu-id="e80fc-106">Sie können einen Kommentar auch einfügen, indem Sie auf der Registerkarte **Überprüfen** auf **Neuer Kommentar** klicken.</span><span class="sxs-lookup"><span data-stu-id="e80fc-106">You can also insert a comment by clicking **New Comment** on the **Review** tab.</span></span> 
  
<span data-ttu-id="e80fc-107">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Comment anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="e80fc-107">To get a reference to the Comment cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e80fc-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e80fc-108">Cell name:</span></span>  <br/> |<span data-ttu-id="e80fc-109">Kommentar</span><span class="sxs-lookup"><span data-stu-id="e80fc-109">Comment</span></span>  <br/> |
   
<span data-ttu-id="e80fc-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Comment nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="e80fc-110">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e80fc-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e80fc-111">Section index:</span></span>  <br/> |<span data-ttu-id="e80fc-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e80fc-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e80fc-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e80fc-113">Row index:</span></span>  <br/> |<span data-ttu-id="e80fc-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="e80fc-114">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="e80fc-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e80fc-115">Cell index:</span></span>  <br/> |<span data-ttu-id="e80fc-116">**visComment**</span><span class="sxs-lookup"><span data-stu-id="e80fc-116">**visComment**</span></span> <br/> |
   

