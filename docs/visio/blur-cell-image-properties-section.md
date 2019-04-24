---
title: Zelle "Blur" (Abschnitt "Image Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm115
localization_priority: Normal
ms.assetid: 8b077cdb-6036-4f77-dc20-a476bb75b0f7
description: Eine Bitmapgrafik wird verwischt oder weichgezeichnet. Der Standardwert ist 0 %.
ms.openlocfilehash: 599810d126c853e37552045d0ef83cb580606ae2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348979"
---
# <a name="blur-cell-image-properties-section"></a><span data-ttu-id="f1881-104">Zelle "Blur" (Abschnitt "Image Properties")</span><span class="sxs-lookup"><span data-stu-id="f1881-104">Blur Cell (Image Properties Section)</span></span>

<span data-ttu-id="f1881-105">Eine Bitmapgrafik wird verwischt oder weichgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f1881-105">Blurs or softens a bitmap image.</span></span> <span data-ttu-id="f1881-106">Der Standardwert ist 0 %.</span><span class="sxs-lookup"><span data-stu-id="f1881-106">The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1881-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1881-107">Remarks</span></span>

<span data-ttu-id="f1881-108">Wenn Sie einen Verweis auf die Zelle "Blur" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f1881-108">To get a reference to the Blur cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f1881-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f1881-109">Cell name:</span></span>  <br/> | <span data-ttu-id="f1881-110">Weichzeichnen</span><span class="sxs-lookup"><span data-stu-id="f1881-110">Blur</span></span>  <br/> |
   
<span data-ttu-id="f1881-111">Wenn Sie einen Verweis auf die Zelle Unschärfe aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f1881-111">To get a reference to the Blur cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f1881-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f1881-112">Section index:</span></span>  <br/> |<span data-ttu-id="f1881-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f1881-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f1881-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f1881-114">Row index:</span></span>  <br/> |<span data-ttu-id="f1881-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="f1881-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="f1881-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f1881-116">Cell index:</span></span>  <br/> |<span data-ttu-id="f1881-117">**visImageBlur**</span><span class="sxs-lookup"><span data-stu-id="f1881-117">**visImageBlur**</span></span> <br/> |
   

