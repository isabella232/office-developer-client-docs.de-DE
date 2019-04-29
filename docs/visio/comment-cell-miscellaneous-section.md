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
# <a name="comment-cell-miscellaneous-section"></a><span data-ttu-id="877d2-103">Zelle "Comment" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="877d2-103">Comment Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="877d2-104">Enthält den Kommentartext im Zeichenformat für ein Shape.</span><span class="sxs-lookup"><span data-stu-id="877d2-104">Contains the comment text in string format for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="877d2-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="877d2-105">Remarks</span></span>

<span data-ttu-id="877d2-106">Sie können einen Kommentar auch einfügen, indem Sie auf der Registerkarte **Überprüfen** auf **Neuer Kommentar** klicken.</span><span class="sxs-lookup"><span data-stu-id="877d2-106">You can also insert a comment by clicking **New Comment** on the **Review** tab.</span></span> 
  
<span data-ttu-id="877d2-107">Wenn Sie einen Verweis auf die Zelle Comment aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="877d2-107">To get a reference to the Comment cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="877d2-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="877d2-108">Cell name:</span></span>  <br/> |<span data-ttu-id="877d2-109">Kommentar</span><span class="sxs-lookup"><span data-stu-id="877d2-109">Comment</span></span>  <br/> |
   
<span data-ttu-id="877d2-110">Wenn Sie einen Verweis auf die Zelle Comment aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="877d2-110">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="877d2-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="877d2-111">Section index:</span></span>  <br/> |<span data-ttu-id="877d2-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="877d2-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="877d2-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="877d2-113">Row index:</span></span>  <br/> |<span data-ttu-id="877d2-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="877d2-114">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="877d2-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="877d2-115">Cell index:</span></span>  <br/> |<span data-ttu-id="877d2-116">**visCom**</span><span class="sxs-lookup"><span data-stu-id="877d2-116">**visComment**</span></span> <br/> |
   

