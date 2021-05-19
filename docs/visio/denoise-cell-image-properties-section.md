---
title: Zelle "Denoise" (Abschnitt "Image Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
localization_priority: Normal
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: Entfernt Rauschen (Pixel mit wahllos verteilten Farbstufen) aus einem Bitmapbild. Der Standardwert lautet 0 %.
ms.openlocfilehash: f970fde22e864239ea3f3f9bcb704e7f4692e9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415803"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="00fb7-104">Zelle "Denoise" (Abschnitt "Image Properties")</span><span class="sxs-lookup"><span data-stu-id="00fb7-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="00fb7-p102">Entfernt Rauschen (Pixel mit wahllos verteilten Farbstufen) aus einem Bitmapbild. Der Standardwert lautet 0 %.</span><span class="sxs-lookup"><span data-stu-id="00fb7-p102">Removes noise (pixels with randomly distributed color levels) from a bitmap image. The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00fb7-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00fb7-107">Remarks</span></span>

<span data-ttu-id="00fb7-108">Um einen Verweis auf die Zelle Denoise anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="00fb7-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00fb7-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="00fb7-109">Cell name:</span></span>  <br/> | <span data-ttu-id="00fb7-110">Denoise</span><span class="sxs-lookup"><span data-stu-id="00fb7-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="00fb7-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Denoise nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="00fb7-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00fb7-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="00fb7-112">Section index:</span></span>  <br/> |<span data-ttu-id="00fb7-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="00fb7-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="00fb7-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="00fb7-114">Row index:</span></span>  <br/> |<span data-ttu-id="00fb7-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="00fb7-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="00fb7-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="00fb7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="00fb7-117">**visImageDenoise**</span><span class="sxs-lookup"><span data-stu-id="00fb7-117">**visImageDenoise**</span></span> <br/> |
   

