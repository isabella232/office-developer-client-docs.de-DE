---
title: Zelle "SpLine" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
localization_priority: Normal
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: Legt den Abstand zwischen einer Textzeile und der nächsten in Prozent fest. 100 % ist dabei die Höhe einer Textzeile.
ms.openlocfilehash: f2f290564d49a056bc3366707b25a7991f8c4401
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798172"
---
# <a name="spline-cell-paragraph-section"></a><span data-ttu-id="48728-103">SpLine Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="48728-103">SpLine Cell (Paragraph Section)</span></span>

<span data-ttu-id="48728-104">Legt den Abstand zwischen einer Textzeile und der nächsten in Prozent fest. 100 % ist dabei die Höhe einer Textzeile.</span><span class="sxs-lookup"><span data-stu-id="48728-104">Determines the distance between one line of text and the next, expressed as a percentage, where 100% is the height of a text line.</span></span>
  
|<span data-ttu-id="48728-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="48728-105">**Value**</span></span>|<span data-ttu-id="48728-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48728-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="48728-107">\>0</span><span class="sxs-lookup"><span data-stu-id="48728-107">\>0</span></span>  <br/> | <span data-ttu-id="48728-108">Absoluter Abstand, unabhängig vom Schriftgrad</span><span class="sxs-lookup"><span data-stu-id="48728-108">Absolute spacing, regardless of font size</span></span>  <br/> |
| <span data-ttu-id="48728-109">=0</span><span class="sxs-lookup"><span data-stu-id="48728-109">=0</span></span>  <br/> | <span data-ttu-id="48728-110">Fester Abstand (Abstand = 100 % des Schriftgrads)</span><span class="sxs-lookup"><span data-stu-id="48728-110">Set solid (spacing = 100% of font size)</span></span>  <br/> |
| <span data-ttu-id="48728-111">\<0</span><span class="sxs-lookup"><span data-stu-id="48728-111">\<0</span></span>  <br/> | <span data-ttu-id="48728-112">Ein Prozentsatz des Schriftgrads (z. B. -120 % ergibt einen Abstand von 120 %)</span><span class="sxs-lookup"><span data-stu-id="48728-112">A percentage of font size (for example, -120% yields 120% spacing)</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48728-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="48728-113">Remarks</span></span>

<span data-ttu-id="48728-114">Wenn Sie einen Verweis auf die Zelle SpLine nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="48728-114">To get a reference to the SpLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="48728-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="48728-115">Cell name:</span></span>  <br/> | <span data-ttu-id="48728-116">Absatz.</span><span class="sxs-lookup"><span data-stu-id="48728-116">Para.</span></span> <span data-ttu-id="48728-117">SpLine [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="48728-117">SpLine [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="48728-118">Wenn Sie einen Verweis auf die Zelle SpLine aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="48728-118">To get a reference to the SpLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="48728-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="48728-119">Section index:</span></span>  <br/> |<span data-ttu-id="48728-120">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="48728-120">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="48728-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="48728-121">Row index:</span></span>  <br/> |<span data-ttu-id="48728-122">**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="48728-122">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="48728-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="48728-123">Cell index:</span></span>  <br/> |<span data-ttu-id="48728-124">**visSpaceLine**</span><span class="sxs-lookup"><span data-stu-id="48728-124">**visSpaceLine**</span></span> <br/> |
   

