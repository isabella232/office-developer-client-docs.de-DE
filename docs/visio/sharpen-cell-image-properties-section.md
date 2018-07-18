---
title: Zelle "Sharpen" (Abschnitt "Image Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm910
localization_priority: Normal
ms.assetid: aa2bebfc-a6bb-a6b3-3ae9-8553f96b5738
description: Schärft eine Bitmapgrafik. Der Standardwert ist 0 %. Beim Scharfzeichnen einer Grafik wird diese durch Erhöhen des Kontrasts angrenzender Pixel fokussiert.
ms.openlocfilehash: fbc66f8c88cde67ad1f259f8392f6d3bd0457be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798068"
---
# <a name="sharpen-cell-image-properties-section"></a><span data-ttu-id="feb14-105">Sharpen Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="feb14-105">Sharpen Cell (Image Properties Section)</span></span>

<span data-ttu-id="feb14-p102">Schärft eine Bitmapgrafik. Der Standardwert ist 0 %. Beim Scharfzeichnen einer Grafik wird diese durch Erhöhen des Kontrasts angrenzender Pixel fokussiert.</span><span class="sxs-lookup"><span data-stu-id="feb14-p102">Sharpens a bitmap image. The default value is 0%. Sharpening an image focuses it by increasing the contrast of adjacent pixels.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="feb14-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="feb14-109">Remarks</span></span>

<span data-ttu-id="feb14-110">Wenn Sie einen Verweis auf die Zelle Sharpen aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="feb14-110">To get a reference to the Sharpen cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="feb14-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="feb14-111">Cell name:</span></span>  <br/> | <span data-ttu-id="feb14-112">Sharpen</span><span class="sxs-lookup"><span data-stu-id="feb14-112">Sharpen</span></span>  <br/> |
   
<span data-ttu-id="feb14-113">Wenn Sie einen Verweis auf die Zelle Sharpen aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="feb14-113">To get a reference to the Sharpen cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="feb14-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="feb14-114">Section index:</span></span>  <br/> |<span data-ttu-id="feb14-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="feb14-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="feb14-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="feb14-116">Row index:</span></span>  <br/> |<span data-ttu-id="feb14-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="feb14-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="feb14-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="feb14-118">Cell index:</span></span>  <br/> |<span data-ttu-id="feb14-119">**visImageSharpen**</span><span class="sxs-lookup"><span data-stu-id="feb14-119">**visImageSharpen**</span></span> <br/> |
   

