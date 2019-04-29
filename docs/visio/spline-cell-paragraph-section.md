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
ms.openlocfilehash: 82b2604a62608c0cc4333892d678b1eb886a9c7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434914"
---
# <a name="spline-cell-paragraph-section"></a><span data-ttu-id="17bed-103">Zelle "SpLine" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="17bed-103">SpLine Cell (Paragraph Section)</span></span>

<span data-ttu-id="17bed-104">Legt den Abstand zwischen einer Textzeile und der nächsten in Prozent fest. 100 % ist dabei die Höhe einer Textzeile.</span><span class="sxs-lookup"><span data-stu-id="17bed-104">Determines the distance between one line of text and the next, expressed as a percentage, where 100% is the height of a text line.</span></span>
  
|<span data-ttu-id="17bed-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="17bed-105">**Value**</span></span>|<span data-ttu-id="17bed-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17bed-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="17bed-107">\>0</span><span class="sxs-lookup"><span data-stu-id="17bed-107">\>0</span></span>  <br/> | <span data-ttu-id="17bed-108">Absoluter Abstand, unabhängig vom Schriftgrad</span><span class="sxs-lookup"><span data-stu-id="17bed-108">Absolute spacing, regardless of font size</span></span>  <br/> |
| <span data-ttu-id="17bed-109">= 0</span><span class="sxs-lookup"><span data-stu-id="17bed-109">=0</span></span>  <br/> | <span data-ttu-id="17bed-110">Fester Abstand (Abstand = 100 % des Schriftgrads)</span><span class="sxs-lookup"><span data-stu-id="17bed-110">Set solid (spacing = 100% of font size)</span></span>  <br/> |
| <span data-ttu-id="17bed-111">\<0</span><span class="sxs-lookup"><span data-stu-id="17bed-111">\<0</span></span>  <br/> | <span data-ttu-id="17bed-112">Ein Prozentsatz des Schriftgrads (z. B. -120 % ergibt einen Abstand von 120 %)</span><span class="sxs-lookup"><span data-stu-id="17bed-112">A percentage of font size (for example, -120% yields 120% spacing)</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17bed-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17bed-113">Remarks</span></span>

<span data-ttu-id="17bed-114">Wenn Sie einen Verweis auf die Zelle SpLine aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="17bed-114">To get a reference to the SpLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17bed-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="17bed-115">Cell name:</span></span>  <br/> | <span data-ttu-id="17bed-116">Para.</span><span class="sxs-lookup"><span data-stu-id="17bed-116">Para.</span></span> <span data-ttu-id="17bed-117">SpLine [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="17bed-117">SpLine [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="17bed-118">Wenn Sie einen Verweis auf die Zelle SpLine nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="17bed-118">To get a reference to the SpLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17bed-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="17bed-119">Section index:</span></span>  <br/> |<span data-ttu-id="17bed-120">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="17bed-120">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="17bed-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="17bed-121">Row index:</span></span>  <br/> |<span data-ttu-id="17bed-122">**visRowParagraph** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="17bed-122">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="17bed-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="17bed-123">Cell index:</span></span>  <br/> |<span data-ttu-id="17bed-124">**visSpaceLine**</span><span class="sxs-lookup"><span data-stu-id="17bed-124">**visSpaceLine**</span></span> <br/> |
   

