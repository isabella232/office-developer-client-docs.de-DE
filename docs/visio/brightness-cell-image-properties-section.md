---
title: Zelle "Brightness" (Abschnitt "Image Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251608
localization_priority: Normal
ms.assetid: 5bb1cc81-f3fd-a835-1449-233dbd1a62b6
description: Passt die Helligkeit einer Bitmapgrafik an. Verringern Sie die Helligkeit einer Grafik durch Eingabe eines Werts zwischen 0 % und 49 %, oder steigern Sie die Helligkeit durch Eingabe eines Werts zwischen 51 % und 100 %. Der Standardwert lautet 50 %.
ms.openlocfilehash: 688a6cacfa9100ad116b9bf06926194c24712219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796540"
---
# <a name="brightness-cell-image-properties-section"></a><span data-ttu-id="20827-105">Brightness Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="20827-105">Brightness Cell (Image Properties Section)</span></span>

<span data-ttu-id="20827-p102">Passt die Helligkeit einer Bitmapgrafik an. Verringern Sie die Helligkeit einer Grafik durch Eingabe eines Werts zwischen 0 % und 49 %, oder steigern Sie die Helligkeit durch Eingabe eines Werts zwischen 51 % und 100 %. Der Standardwert lautet 50 %.</span><span class="sxs-lookup"><span data-stu-id="20827-p102">Adjusts the brightness of a bitmap image. Decrease brightness of an image by entering a value between 0% and 49%, or increase brightness by entering a value between 51% and 100%. The default value is 50%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20827-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20827-109">Remarks</span></span>

<span data-ttu-id="20827-110">Wenn Sie einen Verweis auf die Zelle Brightness aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="20827-110">To get a reference to the Brightness cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20827-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="20827-111">Cell name:</span></span>  <br/> | <span data-ttu-id="20827-112">Brightness</span><span class="sxs-lookup"><span data-stu-id="20827-112">Brightness</span></span>  <br/> |
   
<span data-ttu-id="20827-113">Wenn Sie einen Verweis auf die Zelle Brightness aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="20827-113">To get a reference to the Brightness cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20827-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="20827-114">Section index:</span></span>  <br/> |<span data-ttu-id="20827-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="20827-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="20827-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="20827-116">Row index:</span></span>  <br/> |<span data-ttu-id="20827-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="20827-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="20827-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="20827-118">Cell index:</span></span>  <br/> |<span data-ttu-id="20827-119">**visImageBrightness**</span><span class="sxs-lookup"><span data-stu-id="20827-119">**visImageBrightness**</span></span> <br/> |
   

