---
title: Zelle "Prompt" (Abschnitt "User-Defined Cells")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an. Die Anwendung schließt den Eingabeaufforderungstext automatisch in Anführungszeichen (), um anzugeben, dass es sich um eine Textzeichenfolge handelt. Wenn Sie ein Gleichheitszeichen (=) eingeben und die Anführungszeichen weglassen, können Sie eine Formel in diese Zelle eingeben, die von der Anwendung ausgewertet wird.
ms.openlocfilehash: 7684025e03bd3f4f68893179b1df00cc0cb535e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435726"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="e7bf3-105">Zelle "Prompt" (Abschnitt "User-Defined Cells")</span><span class="sxs-lookup"><span data-stu-id="e7bf3-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="e7bf3-p102">Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an. Die Anwendung schließt den Aufforderungstext automatisch in Anführungszeichen (" ") ein, um anzuzeigen, dass es sich um eine Textzeichenfolge handelt. Wenn Sie ein Gleichheitszeichen (=) eingeben und die Anführungszeichen auslassen, können Sie eine Formel in diese Zelle eingeben, die von der Anwendung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-p102">Specifies a descriptive prompt or comment for the user-defined cell. The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string. If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7bf3-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e7bf3-109">Remarks</span></span>

<span data-ttu-id="e7bf3-110">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Eingabeaufforderung anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="e7bf3-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e7bf3-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e7bf3-111">Cell name:</span></span>  <br/> | <span data-ttu-id="e7bf3-112">User.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-112">User.</span></span>  <span data-ttu-id="e7bf3-113">*Name*  . Eingabeaufforderung, wo Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="e7bf3-114">*Name*  ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="e7bf3-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="e7bf3-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Prompt nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="e7bf3-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e7bf3-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e7bf3-116">Section index:</span></span>  <br/> |<span data-ttu-id="e7bf3-117">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="e7bf3-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="e7bf3-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e7bf3-118">Row index:</span></span>  <br/> |<span data-ttu-id="e7bf3-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e7bf3-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e7bf3-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e7bf3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e7bf3-121">**visUserPrompt**</span><span class="sxs-lookup"><span data-stu-id="e7bf3-121">**visUserPrompt**</span></span> <br/> |
   

