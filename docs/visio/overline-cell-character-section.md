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
ms.openlocfilehash: d5df39c2f12890d5fb4881346516abdb4f2b8099
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431645"
---
# <a name="overline-cell-character-section"></a><span data-ttu-id="7c14a-103">Zelle "Overline" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="7c14a-103">Overline Cell (Character Section)</span></span>

<span data-ttu-id="7c14a-104">Legt fest, ob der Text überstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="7c14a-104">Determines whether the text has a line above it.</span></span>
  
|<span data-ttu-id="7c14a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7c14a-105">**Value**</span></span>|<span data-ttu-id="7c14a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7c14a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7c14a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="7c14a-107">TRUE</span></span>  <br/> |<span data-ttu-id="7c14a-108">Text ist überstrichen.</span><span class="sxs-lookup"><span data-stu-id="7c14a-108">Text has a line above it.</span></span>  <br/> |
|<span data-ttu-id="7c14a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="7c14a-109">FALSE</span></span>  <br/> |<span data-ttu-id="7c14a-110">Text ist nicht überstrichen.</span><span class="sxs-lookup"><span data-stu-id="7c14a-110">Text does not have a line above it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c14a-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7c14a-111">Remarks</span></span>

<span data-ttu-id="7c14a-112">Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**).</span><span class="sxs-lookup"><span data-stu-id="7c14a-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="7c14a-113">Verwenden Sie zum Erhalten eines Verweises auf die Zelle "Überline" anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="7c14a-113">To get a reference to the Overline cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c14a-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7c14a-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7c14a-115">Char.Overline[ *i*  ] wobei  *i*  = <1>, 2.</span><span class="sxs-lookup"><span data-stu-id="7c14a-115">Char.Overline[ *i*  ] where  *i*  = <1>, 2.</span></span> <span data-ttu-id="7c14a-116">3...</span><span class="sxs-lookup"><span data-stu-id="7c14a-116">3...</span></span>  <br/> |
   
<span data-ttu-id="7c14a-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Überleitungszelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="7c14a-117">To get a reference to the Overline cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c14a-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7c14a-118">Section index:</span></span>  <br/> |<span data-ttu-id="7c14a-119">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="7c14a-119">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="7c14a-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7c14a-120">Row index:</span></span>  <br/> |<span data-ttu-id="7c14a-121">**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7c14a-121">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7c14a-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7c14a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="7c14a-123">**visCharacterOverline**</span><span class="sxs-lookup"><span data-stu-id="7c14a-123">**visCharacterOverline**</span></span> <br/> |
   

