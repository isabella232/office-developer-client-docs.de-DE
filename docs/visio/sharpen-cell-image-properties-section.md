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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415922"
---
# <a name="sharpen-cell-image-properties-section"></a><span data-ttu-id="9142b-105">Zelle "Sharpen" (Abschnitt "Image Properties")</span><span class="sxs-lookup"><span data-stu-id="9142b-105">Sharpen Cell (Image Properties Section)</span></span>

<span data-ttu-id="9142b-106">Schärft eine Bitmapgrafik.</span><span class="sxs-lookup"><span data-stu-id="9142b-106">Sharpens a bitmap image.</span></span> <span data-ttu-id="9142b-107">Der Standardwert ist 0 %.</span><span class="sxs-lookup"><span data-stu-id="9142b-107">The default value is 0%.</span></span> <span data-ttu-id="9142b-108">Beim Scharfzeichnen einer Grafik wird diese durch Erhöhen des Kontrasts angrenzender Pixel fokussiert.</span><span class="sxs-lookup"><span data-stu-id="9142b-108">Sharpening an image focuses it by increasing the contrast of adjacent pixels.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9142b-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9142b-109">Remarks</span></span>

<span data-ttu-id="9142b-110">Wenn Sie einen Verweis auf die Zelle schärfen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9142b-110">To get a reference to the Sharpen cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9142b-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9142b-111">Cell name:</span></span>  <br/> | <span data-ttu-id="9142b-112">"Sharpen</span><span class="sxs-lookup"><span data-stu-id="9142b-112">Sharpen</span></span>  <br/> |
   
<span data-ttu-id="9142b-113">Wenn Sie einen Verweis auf die Zelle Scharfzeichnen aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9142b-113">To get a reference to the Sharpen cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9142b-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9142b-114">Section index:</span></span>  <br/> |<span data-ttu-id="9142b-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9142b-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9142b-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9142b-116">Row index:</span></span>  <br/> |<span data-ttu-id="9142b-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="9142b-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="9142b-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9142b-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9142b-119">**visImageSharpen**</span><span class="sxs-lookup"><span data-stu-id="9142b-119">**visImageSharpen**</span></span> <br/> |
   

