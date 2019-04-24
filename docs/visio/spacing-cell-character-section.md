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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334902"
---
# <a name="spacing-cell-character-section"></a><span data-ttu-id="a1381-104">Zelle "Spacing" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="a1381-104">Spacing Cell (Character Section)</span></span>

<span data-ttu-id="a1381-105">Definiert den Platz zwischen zwei oder mehreren Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a1381-105">Controls the amount of space between two or more characters.</span></span> <span data-ttu-id="a1381-106">Dieser Platz kann in 1/20 Pkt-Schritten hinzugefügt oder abgezogen werden.</span><span class="sxs-lookup"><span data-stu-id="a1381-106">Space can be added or subtracted in 1/20th point increments.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a1381-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1381-107">Remarks</span></span>

<span data-ttu-id="a1381-108">Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**).</span><span class="sxs-lookup"><span data-stu-id="a1381-108">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="a1381-109">Wenn Sie einen Verweis auf die Zelle Spacing aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a1381-109">To get a reference to the Spacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1381-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a1381-110">Cell name:</span></span>  <br/> |<span data-ttu-id="a1381-111">Char. Letterspace [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a1381-111">Char.Letterspace[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a1381-112">Wenn Sie einen Verweis auf die Zelle Spacing nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a1381-112">To get a reference to the Spacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1381-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a1381-113">Section index:</span></span>  <br/> |<span data-ttu-id="a1381-114">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="a1381-114">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="a1381-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a1381-115">Row index:</span></span>  <br/> |<span data-ttu-id="a1381-116">**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a1381-116">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a1381-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a1381-117">Cell index:</span></span>  <br/> |<span data-ttu-id="a1381-118">**visCharacterLetterspace**</span><span class="sxs-lookup"><span data-stu-id="a1381-118">**visCharacterLetterspace**</span></span> <br/> |
   

