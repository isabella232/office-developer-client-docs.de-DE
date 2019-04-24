---
title: Zelle "DoubleULine" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Legt fest, ob der Textbereich doppelt unterstrichen ist.
ms.openlocfilehash: 2708e7f55e1fd04d5fb902b3d382035790cbbcc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357463"
---
# <a name="doubleuline-cell-character-section"></a><span data-ttu-id="3a8bb-103">Zelle "DoubleULine" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="3a8bb-103">DoubleULine Cell (Character Section)</span></span>

<span data-ttu-id="3a8bb-104">Legt fest, ob der Textbereich doppelt unterstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="3a8bb-104">Determines whether the range of text has a double underline below it.</span></span>
  
|<span data-ttu-id="3a8bb-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3a8bb-105">**Value**</span></span>|<span data-ttu-id="3a8bb-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3a8bb-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3a8bb-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3a8bb-107">TRUE</span></span>  <br/> |<span data-ttu-id="3a8bb-108">Text ist doppelt unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="3a8bb-108">Text has a double underline below it.</span></span>  <br/> |
|<span data-ttu-id="3a8bb-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3a8bb-109">FALSE</span></span>  <br/> |<span data-ttu-id="3a8bb-110">Text ist nicht doppelt unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="3a8bb-110">Text does not have a double underline below it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a8bb-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a8bb-111">Remarks</span></span>

<span data-ttu-id="3a8bb-p101">Die Zelle DoubleULine enthält Formatierungsinformationen für einen Unterbereich des Texts eines Shapes, wenn der Abschnitt Character mehrere Zeilen enthält. Andernfalls enthält diese Zelle Formatierungsinformationen für den gesamten Text des Shapes.</span><span class="sxs-lookup"><span data-stu-id="3a8bb-p101">The DoubleULine cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="3a8bb-114">Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**).</span><span class="sxs-lookup"><span data-stu-id="3a8bb-114">You can also set the value of this cell by using the **Text** dialog box (click the **Font** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="3a8bb-115">Wenn Sie einen Verweis auf die Zelle "DoubleULine aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3a8bb-115">To get a reference to the DoubleULine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a8bb-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="3a8bb-116">Cell name:</span></span>  <br/> |<span data-ttu-id="3a8bb-117">Char. DoubleULine [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3a8bb-117">Char.DblUnderline[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3a8bb-118">Wenn Sie einen Verweis auf die Zelle "DoubleULine aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="3a8bb-118">To get a reference to the DoubleULine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a8bb-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="3a8bb-119">Section index:</span></span>  <br/> |<span data-ttu-id="3a8bb-120">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="3a8bb-120">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="3a8bb-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3a8bb-121">Row index:</span></span>  <br/> |<span data-ttu-id="3a8bb-122">**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3a8bb-122">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="3a8bb-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="3a8bb-123">Cell index:</span></span>  <br/> |<span data-ttu-id="3a8bb-124">**visCharacterDblUnderline**</span><span class="sxs-lookup"><span data-stu-id="3a8bb-124">**visCharacterDblUnderline**</span></span> <br/> |
   

