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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360249"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="9366f-104">Zelle "Denoise" (Abschnitt "Image Properties")</span><span class="sxs-lookup"><span data-stu-id="9366f-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="9366f-105">Entfernt Rauschen (Pixel mit wahllos verteilten Farbstufen) aus einem Bitmapbild.</span><span class="sxs-lookup"><span data-stu-id="9366f-105">Removes noise (pixels with randomly distributed color levels) from a bitmap image.</span></span> <span data-ttu-id="9366f-106">Der Standardwert lautet 0 %.</span><span class="sxs-lookup"><span data-stu-id="9366f-106">The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9366f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9366f-107">Remarks</span></span>

<span data-ttu-id="9366f-108">Wenn Sie einen Verweis auf die Zelle Denoise aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9366f-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9366f-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9366f-109">Cell name:</span></span>  <br/> | <span data-ttu-id="9366f-110">Denoise</span><span class="sxs-lookup"><span data-stu-id="9366f-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="9366f-111">Wenn Sie einen Verweis auf die Zelle Denoise aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9366f-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9366f-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9366f-112">Section index:</span></span>  <br/> |<span data-ttu-id="9366f-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9366f-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9366f-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9366f-114">Row index:</span></span>  <br/> |<span data-ttu-id="9366f-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="9366f-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="9366f-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9366f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="9366f-117">**visImageDenoise**</span><span class="sxs-lookup"><span data-stu-id="9366f-117">**visImageDenoise**</span></span> <br/> |
   

