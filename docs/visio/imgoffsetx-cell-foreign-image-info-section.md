---
title: Zelle "ImgOffsetX" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251308
localization_priority: Normal
ms.assetid: c079fb10-4db7-4657-75d2-2fb953c86670
description: Bestimmt den Abstand, den das Objekt horizontal vom Ursprung des Rahmens des Objekts entfernt ist. Der Standardwert ist 0. Durch Bearbeitung des Objekts mit dem Zuschneidetool wird dieser Wert geändert.
ms.openlocfilehash: d9b3e97a07bc1cadc0276905c4199861ab0590ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405233"
---
# <a name="imgoffsetx-cell-foreign-image-info-section"></a><span data-ttu-id="154fd-105">Zelle "ImgOffsetX" (Abschnitt "Foreign Image Info")</span><span class="sxs-lookup"><span data-stu-id="154fd-105">ImgOffsetX Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="154fd-p102">Bestimmt den Abstand, den das Objekt horizontal vom Ursprung des Rahmens des Objekts entfernt ist. Der Standardwert ist 0. Durch Bearbeitung des Objekts mit dem Zuschneidetool wird dieser Wert geändert.</span><span class="sxs-lookup"><span data-stu-id="154fd-p102">Determines the distance the object is offset horizontally from the origin of the object's border. The default is 0. Panning the object with the **Crop** tool changes this value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="154fd-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="154fd-109">Remarks</span></span>

<span data-ttu-id="154fd-110">Um einen Verweis auf die ImgOffsetX-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="154fd-110">To get a reference to the ImgOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="154fd-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="154fd-111">Cell name:</span></span>  <br/> | <span data-ttu-id="154fd-112">ImgOffsetX</span><span class="sxs-lookup"><span data-stu-id="154fd-112">ImgOffsetX</span></span>  <br/> |
   
<span data-ttu-id="154fd-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ImgOffsetX-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="154fd-113">To get a reference to the ImgOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="154fd-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="154fd-114">Section index:</span></span>  <br/> |<span data-ttu-id="154fd-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="154fd-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="154fd-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="154fd-116">Row index:</span></span>  <br/> |<span data-ttu-id="154fd-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="154fd-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="154fd-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="154fd-118">Cell index:</span></span>  <br/> |<span data-ttu-id="154fd-119">**visFrgnImgOffsetX**</span><span class="sxs-lookup"><span data-stu-id="154fd-119">**visFrgnImgOffsetX**</span></span> <br/> |
   

