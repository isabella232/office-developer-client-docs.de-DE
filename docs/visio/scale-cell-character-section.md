---
title: Zelle "Scale" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Steuert die Schriftartbreite. Der Standardwert für diese Zelle ist 100%.
ms.openlocfilehash: fedbc0aec23320d03ca358f34babda56eaab31e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797971"
---
# <a name="scale-cell-character-section"></a><span data-ttu-id="bd8ba-104">Scale Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="bd8ba-104">Scale Cell (Character Section)</span></span>

<span data-ttu-id="bd8ba-p102">Steuert die Schriftartbreite. Der Standardwert für diese Zelle ist 100%.</span><span class="sxs-lookup"><span data-stu-id="bd8ba-p102">Controls the font width. The default value for this cell is 100%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd8ba-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd8ba-107">Remarks</span></span>

<span data-ttu-id="bd8ba-p103">Legen Sie einen Prozentsatz zwischen 1% und 99% fest, um die Schriftartbreite zu reduzieren. Legen Sie einen Prozentsatz zwischen 101% und 600% fest, um die Schriftartbreite zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="bd8ba-p103">Set the percentage between 1% and 99% to decrease the font width. Set it between 101% and 600% to increase the font width.</span></span>
  
<span data-ttu-id="bd8ba-110">Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**).</span><span class="sxs-lookup"><span data-stu-id="bd8ba-110">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="bd8ba-111">Wenn Sie einen Verweis auf die Zelle Scale aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bd8ba-111">To get a reference to the Scale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd8ba-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bd8ba-112">Cell name:</span></span>  <br/> |<span data-ttu-id="bd8ba-113">Char.FontScale [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bd8ba-113">Char.FontScale[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bd8ba-114">Wenn Sie einen Verweis auf die Zelle Scale aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bd8ba-114">To get a reference to the Scale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd8ba-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bd8ba-115">Section index:</span></span>  <br/> |<span data-ttu-id="bd8ba-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="bd8ba-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="bd8ba-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bd8ba-117">Row index:</span></span>  <br/> |<span data-ttu-id="bd8ba-118">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bd8ba-118">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="bd8ba-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bd8ba-119">Cell index:</span></span>  <br/> |<span data-ttu-id="bd8ba-120">**visCharacterFontScale**</span><span class="sxs-lookup"><span data-stu-id="bd8ba-120">**visCharacterFontScale**</span></span> <br/> |
   

