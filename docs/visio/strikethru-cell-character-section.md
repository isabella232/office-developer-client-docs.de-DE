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
ms.openlocfilehash: 2b25d1d9b00d062214c02c3fc7b14569b43a5110
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798208"
---
# <a name="strikethru-cell-character-section"></a><span data-ttu-id="90338-103">Strikethru Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="90338-103">Strikethru Cell (Character Section)</span></span>

<span data-ttu-id="90338-104">Legt fest, ob der Text als durchgestrichen formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="90338-104">Determines whether the text is formatted as strikethrough.</span></span>
  
|<span data-ttu-id="90338-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="90338-105">**Value**</span></span>|<span data-ttu-id="90338-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="90338-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90338-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="90338-107">TRUE</span></span>  <br/> |<span data-ttu-id="90338-108">Text ist als durchgestrichen formatiert.</span><span class="sxs-lookup"><span data-stu-id="90338-108">Text is formatted as strikethrough.</span></span>  <br/> |
|<span data-ttu-id="90338-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="90338-109">FALSE</span></span>  <br/> |<span data-ttu-id="90338-110">Text ist nicht als durchgestrichen formatiert.</span><span class="sxs-lookup"><span data-stu-id="90338-110">Text is not formatted as strikethrough.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90338-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90338-111">Remarks</span></span>

<span data-ttu-id="90338-112">Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**).</span><span class="sxs-lookup"><span data-stu-id="90338-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="90338-113">Wenn Sie einen Verweis auf die Zelle Strikethru aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="90338-113">To get a reference to the Strikethru cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90338-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="90338-114">Cell name:</span></span>  <br/> |<span data-ttu-id="90338-115">Char.Strikethru [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="90338-115">Char.Strikethru[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="90338-116">Wenn Sie einen Verweis auf die Zelle Strikethru aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="90338-116">To get a reference to the Strikethru cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90338-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="90338-117">Section index:</span></span>  <br/> |<span data-ttu-id="90338-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="90338-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="90338-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="90338-119">Row index:</span></span>  <br/> |<span data-ttu-id="90338-120">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="90338-120">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="90338-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="90338-121">Cell index:</span></span>  <br/> |<span data-ttu-id="90338-122">**visCharacterStrikethru**</span><span class="sxs-lookup"><span data-stu-id="90338-122">**visCharacterStrikethru**</span></span> <br/> |
   

