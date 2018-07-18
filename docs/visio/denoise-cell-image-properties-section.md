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
ms.openlocfilehash: f08d09126a24935c0dd4dcda5e88fdd559c8d176
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796851"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="27c46-104">Denoise Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="27c46-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="27c46-p102">Entfernt Rauschen (Pixel mit wahllos verteilten Farbstufen) aus einem Bitmapbild. Der Standardwert lautet 0 %.</span><span class="sxs-lookup"><span data-stu-id="27c46-p102">Removes noise (pixels with randomly distributed color levels) from a bitmap image. The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27c46-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="27c46-107">Remarks</span></span>

<span data-ttu-id="27c46-108">Wenn Sie einen Verweis auf die Zelle Denoise aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="27c46-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27c46-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="27c46-109">Cell name:</span></span>  <br/> | <span data-ttu-id="27c46-110">Denoise</span><span class="sxs-lookup"><span data-stu-id="27c46-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="27c46-111">Wenn Sie einen Verweis auf die Zelle Denoise aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="27c46-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27c46-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="27c46-112">Section index:</span></span>  <br/> |<span data-ttu-id="27c46-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="27c46-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="27c46-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="27c46-114">Row index:</span></span>  <br/> |<span data-ttu-id="27c46-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="27c46-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="27c46-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="27c46-116">Cell index:</span></span>  <br/> |<span data-ttu-id="27c46-117">**visImageDenoise**</span><span class="sxs-lookup"><span data-stu-id="27c46-117">**visImageDenoise**</span></span> <br/> |
   

