---
title: Zelle "Spacing" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
localization_priority: Normal
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: Definiert den Platz zwischen zwei oder mehreren Zeichen. Dieser Platz kann in 1/20 Pkt-Schritten hinzugefügt oder abgezogen werden.
ms.openlocfilehash: 927b6203b81af453411cdd13b6f8c8342507a61b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430063"
---
# <a name="spacing-cell-character-section"></a><span data-ttu-id="2f9a4-104">Zelle "Spacing" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="2f9a4-104">Spacing Cell (Character Section)</span></span>

<span data-ttu-id="2f9a4-p102">Definiert den Platz zwischen zwei oder mehreren Zeichen. Dieser Platz kann in 1/20 Pkt-Schritten hinzugefügt oder abgezogen werden.</span><span class="sxs-lookup"><span data-stu-id="2f9a4-p102">Controls the amount of space between two or more characters. Space can be added or subtracted in 1/20th point increments.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f9a4-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2f9a4-107">Remarks</span></span>

<span data-ttu-id="2f9a4-108">Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**).</span><span class="sxs-lookup"><span data-stu-id="2f9a4-108">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="2f9a4-109">Um einen Verweis auf die Zelle "Spacing" anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="2f9a4-109">To get a reference to the Spacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f9a4-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2f9a4-110">Cell name:</span></span>  <br/> |<span data-ttu-id="2f9a4-111">Char.Letterspace[ *i*  ] wobei  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2f9a4-111">Char.Letterspace[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2f9a4-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Spacing nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2f9a4-112">To get a reference to the Spacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f9a4-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2f9a4-113">Section index:</span></span>  <br/> |<span data-ttu-id="2f9a4-114">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="2f9a4-114">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="2f9a4-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2f9a4-115">Row index:</span></span>  <br/> |<span data-ttu-id="2f9a4-116">**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2f9a4-116">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="2f9a4-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2f9a4-117">Cell index:</span></span>  <br/> |<span data-ttu-id="2f9a4-118">**visCharacterLetterspace**</span><span class="sxs-lookup"><span data-stu-id="2f9a4-118">**visCharacterLetterspace**</span></span> <br/> |
   

