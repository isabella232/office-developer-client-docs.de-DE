---
title: Zelle "Strikethru" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Legt fest, ob der Text als durchgestrichen formatiert ist.
ms.openlocfilehash: 4a58123814a4782c279a36d202e1293ec222ef93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349336"
---
# <a name="strikethru-cell-character-section"></a><span data-ttu-id="1f390-103">Zelle "Strikethru" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="1f390-103">Strikethru Cell (Character Section)</span></span>

<span data-ttu-id="1f390-104">Legt fest, ob der Text als durchgestrichen formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="1f390-104">Determines whether the text is formatted as strikethrough.</span></span>
  
|<span data-ttu-id="1f390-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1f390-105">**Value**</span></span>|<span data-ttu-id="1f390-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f390-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f390-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="1f390-107">TRUE</span></span>  <br/> |<span data-ttu-id="1f390-108">Text ist als durchgestrichen formatiert.</span><span class="sxs-lookup"><span data-stu-id="1f390-108">Text is formatted as strikethrough.</span></span>  <br/> |
|<span data-ttu-id="1f390-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="1f390-109">FALSE</span></span>  <br/> |<span data-ttu-id="1f390-110">Text ist nicht als durchgestrichen formatiert.</span><span class="sxs-lookup"><span data-stu-id="1f390-110">Text is not formatted as strikethrough.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f390-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f390-111">Remarks</span></span>

<span data-ttu-id="1f390-112">Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**).</span><span class="sxs-lookup"><span data-stu-id="1f390-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="1f390-113">Wenn Sie einen Verweis auf die Zelle Strikethru aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1f390-113">To get a reference to the Strikethru cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f390-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1f390-114">Cell name:</span></span>  <br/> |<span data-ttu-id="1f390-115">Char. Strikethru [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1f390-115">Char.Strikethru[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1f390-116">Wenn Sie einen Verweis auf die Zelle Strikethru aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1f390-116">To get a reference to the Strikethru cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f390-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1f390-117">Section index:</span></span>  <br/> |<span data-ttu-id="1f390-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="1f390-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="1f390-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1f390-119">Row index:</span></span>  <br/> |<span data-ttu-id="1f390-120">**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1f390-120">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="1f390-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1f390-121">Cell index:</span></span>  <br/> |<span data-ttu-id="1f390-122">**visCharacterStrikethru**</span><span class="sxs-lookup"><span data-stu-id="1f390-122">**visCharacterStrikethru**</span></span> <br/> |
   

