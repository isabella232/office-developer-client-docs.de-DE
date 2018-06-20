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
ms.openlocfilehash: 14a50f2015b2b24d7e41f5d11018a749d089fc37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796539"
---
# <a name="blur-cell-image-properties-section"></a><span data-ttu-id="0ff16-104">Blur Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="0ff16-104">Blur Cell (Image Properties Section)</span></span>

<span data-ttu-id="0ff16-p102">Eine Bitmapgrafik wird verwischt oder weichgezeichnet. Der Standardwert ist 0 %.</span><span class="sxs-lookup"><span data-stu-id="0ff16-p102">Blurs or softens a bitmap image. The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ff16-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0ff16-107">Remarks</span></span>

<span data-ttu-id="0ff16-108">Wenn Sie einen Verweis auf die Zelle Blur nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0ff16-108">To get a reference to the Blur cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0ff16-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0ff16-109">Cell name:</span></span>  <br/> | <span data-ttu-id="0ff16-110">Blur</span><span class="sxs-lookup"><span data-stu-id="0ff16-110">Blur</span></span>  <br/> |
   
<span data-ttu-id="0ff16-111">Wenn Sie einen Verweis auf die Zelle Blur aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0ff16-111">To get a reference to the Blur cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0ff16-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0ff16-112">Section index:</span></span>  <br/> |<span data-ttu-id="0ff16-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0ff16-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0ff16-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0ff16-114">Row index:</span></span>  <br/> |<span data-ttu-id="0ff16-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="0ff16-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="0ff16-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0ff16-116">Cell index:</span></span>  <br/> |<span data-ttu-id="0ff16-117">**visImageBlur**</span><span class="sxs-lookup"><span data-stu-id="0ff16-117">**visImageBlur**</span></span> <br/> |
   

