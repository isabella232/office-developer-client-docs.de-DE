---
title: Zelle "Font" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Stellt die Nummer der Schriftart dar, die zum Formatieren des Texts verwendet wird. Schriftartnummern können abhängig von den auf Ihrem System installierten Schriftarten variieren. Die Nummer 0 stellt die Standardschriftart dar, bei der es sich i. A. um die Schriftart Arial handelt.
ms.openlocfilehash: d9182932b8fa63c30473b93e420aa9efe30bf5eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346158"
---
# <a name="font-cell-character-section"></a><span data-ttu-id="8360d-105">Zelle "Font" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="8360d-105">Font Cell (Character Section)</span></span>

<span data-ttu-id="8360d-p102">Stellt die Nummer der Schriftart dar, die zum Formatieren des Texts verwendet wird. Schriftartnummern können abhängig von den auf Ihrem System installierten Schriftarten variieren. Die Nummer 0 stellt die Standardschriftart dar, bei der es sich i. A. um die Schriftart Arial handelt.</span><span class="sxs-lookup"><span data-stu-id="8360d-p102">Represents the number of the font used to format the text. Font numbers vary according to the fonts installed on your system. The number 0 represents the default font, which is typically Arial.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8360d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8360d-109">Remarks</span></span>

<span data-ttu-id="8360d-110">Wenn Sie einen Verweis auf die Zelle Font aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8360d-110">To get a reference to the Font cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8360d-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8360d-111">Cell name:</span></span>  <br/> | <span data-ttu-id="8360d-112">Char. Font [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8360d-112">Char.Font[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8360d-113">Wenn Sie einen Verweis auf die Zelle Font aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8360d-113">To get a reference to the Font cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8360d-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8360d-114">Section index:</span></span>  <br/> |<span data-ttu-id="8360d-115">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="8360d-115">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="8360d-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8360d-116">Row index:</span></span>  <br/> |<span data-ttu-id="8360d-117">**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8360d-117">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8360d-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8360d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="8360d-119">**visCharacterFont**</span><span class="sxs-lookup"><span data-stu-id="8360d-119">**visCharacterFont**</span></span> <br/> |
   

