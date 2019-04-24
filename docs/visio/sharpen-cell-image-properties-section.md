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
ms.openlocfilehash: e519cf6e5a168b64b4bc8aa083843163a47525ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349091"
---
# <a name="sharpen-cell-image-properties-section"></a><span data-ttu-id="1f676-105">Zelle "Sharpen" (Abschnitt "Image Properties")</span><span class="sxs-lookup"><span data-stu-id="1f676-105">Sharpen Cell (Image Properties Section)</span></span>

<span data-ttu-id="1f676-106">Schärft eine Bitmapgrafik.</span><span class="sxs-lookup"><span data-stu-id="1f676-106">Sharpens a bitmap image.</span></span> <span data-ttu-id="1f676-107">Der Standardwert ist 0 %.</span><span class="sxs-lookup"><span data-stu-id="1f676-107">The default value is 0%.</span></span> <span data-ttu-id="1f676-108">Beim Scharfzeichnen einer Grafik wird diese durch Erhöhen des Kontrasts angrenzender Pixel fokussiert.</span><span class="sxs-lookup"><span data-stu-id="1f676-108">Sharpening an image focuses it by increasing the contrast of adjacent pixels.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f676-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f676-109">Remarks</span></span>

<span data-ttu-id="1f676-110">Wenn Sie einen Verweis auf die Zelle schärfen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1f676-110">To get a reference to the Sharpen cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f676-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1f676-111">Cell name:</span></span>  <br/> | <span data-ttu-id="1f676-112">"Sharpen</span><span class="sxs-lookup"><span data-stu-id="1f676-112">Sharpen</span></span>  <br/> |
   
<span data-ttu-id="1f676-113">Wenn Sie einen Verweis auf die Zelle Scharfzeichnen aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1f676-113">To get a reference to the Sharpen cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f676-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1f676-114">Section index:</span></span>  <br/> |<span data-ttu-id="1f676-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1f676-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1f676-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1f676-116">Row index:</span></span>  <br/> |<span data-ttu-id="1f676-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="1f676-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="1f676-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1f676-118">Cell index:</span></span>  <br/> |<span data-ttu-id="1f676-119">**visImageSharpen**</span><span class="sxs-lookup"><span data-stu-id="1f676-119">**visImageSharpen**</span></span> <br/> |
   

