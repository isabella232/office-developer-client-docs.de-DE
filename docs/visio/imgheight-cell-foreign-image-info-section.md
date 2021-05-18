---
title: Zelle "ImgHeight" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Definiert die Höhe des Bilds des Objekts innerhalb seines Rahmens. Die Standardformel lautet:'
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411197"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="fec1b-104">Zelle "ImgHeight" (Abschnitt "Foreign Image Info")</span><span class="sxs-lookup"><span data-stu-id="fec1b-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="fec1b-p102">Definiert die Höhe des Bilds des Objekts innerhalb seines Rahmens. Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="fec1b-p102">Determines the height of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="fec1b-107">= Höhe \* 1</span><span class="sxs-lookup"><span data-stu-id="fec1b-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fec1b-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fec1b-108">Remarks</span></span>

<span data-ttu-id="fec1b-109">Um einen Verweis auf die Zelle ImgHeight anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="fec1b-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fec1b-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="fec1b-110">Cell name:</span></span>  <br/> | <span data-ttu-id="fec1b-111">ImgHeight</span><span class="sxs-lookup"><span data-stu-id="fec1b-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="fec1b-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ImgHeight-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="fec1b-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fec1b-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="fec1b-113">Section index:</span></span>  <br/> |<span data-ttu-id="fec1b-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fec1b-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fec1b-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="fec1b-115">Row index:</span></span>  <br/> |<span data-ttu-id="fec1b-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="fec1b-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="fec1b-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="fec1b-117">Cell index:</span></span>  <br/> |<span data-ttu-id="fec1b-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="fec1b-118">**visFrgnImgHeight**</span></span> <br/> |
   

