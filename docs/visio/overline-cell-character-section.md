---
title: Zelle "Overline" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Legt fest, ob der Text überstrichen ist.
ms.openlocfilehash: 3ceb0f5bcb6f66098938e49ea5f176921d0c9808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797569"
---
# <a name="overline-cell-character-section"></a><span data-ttu-id="1b8cc-103">Overline Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="1b8cc-103">Overline Cell (Character Section)</span></span>

<span data-ttu-id="1b8cc-104">Legt fest, ob der Text überstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="1b8cc-104">Determines whether the text has a line above it.</span></span>
  
|<span data-ttu-id="1b8cc-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1b8cc-105">**Value**</span></span>|<span data-ttu-id="1b8cc-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1b8cc-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b8cc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="1b8cc-107">TRUE</span></span>  <br/> |<span data-ttu-id="1b8cc-108">Text ist überstrichen.</span><span class="sxs-lookup"><span data-stu-id="1b8cc-108">Text has a line above it.</span></span>  <br/> |
|<span data-ttu-id="1b8cc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="1b8cc-109">FALSE</span></span>  <br/> |<span data-ttu-id="1b8cc-110">Text ist nicht überstrichen.</span><span class="sxs-lookup"><span data-stu-id="1b8cc-110">Text does not have a line above it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b8cc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b8cc-111">Remarks</span></span>

<span data-ttu-id="1b8cc-112">Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Schriftart** ).</span><span class="sxs-lookup"><span data-stu-id="1b8cc-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="1b8cc-113">Wenn Sie einen Verweis auf die Zelle Overline nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1b8cc-113">To get a reference to the Overline cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b8cc-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1b8cc-114">Cell name:</span></span>  <br/> |<span data-ttu-id="1b8cc-115">Char.Overline [ *i* ] wobei *i* = < 1 >, 2.</span><span class="sxs-lookup"><span data-stu-id="1b8cc-115">Char.Overline[ *i*  ] where  *i*  = <1>, 2.</span></span> <span data-ttu-id="1b8cc-116">3...</span><span class="sxs-lookup"><span data-stu-id="1b8cc-116">3...</span></span>  <br/> |
   
<span data-ttu-id="1b8cc-117">Wenn Sie einen Verweis auf die Zelle Overline aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1b8cc-117">To get a reference to the Overline cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b8cc-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1b8cc-118">Section index:</span></span>  <br/> |<span data-ttu-id="1b8cc-119">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="1b8cc-119">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="1b8cc-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1b8cc-120">Row index:</span></span>  <br/> |<span data-ttu-id="1b8cc-121">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1b8cc-121">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="1b8cc-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1b8cc-122">Cell index:</span></span>  <br/> |<span data-ttu-id="1b8cc-123">**visCharacterOverline**</span><span class="sxs-lookup"><span data-stu-id="1b8cc-123">**visCharacterOverline**</span></span> <br/> |
   

