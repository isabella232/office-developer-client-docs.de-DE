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
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="6cd6d-104">Zelle "ImgHeight" (Abschnitt "Foreign Image Info")</span><span class="sxs-lookup"><span data-stu-id="6cd6d-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="6cd6d-105">Definiert die Höhe des Bilds des Objekts innerhalb seines Rahmens.</span><span class="sxs-lookup"><span data-stu-id="6cd6d-105">Determines the height of the object's image within its border.</span></span> <span data-ttu-id="6cd6d-106">Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="6cd6d-106">The default formula is:</span></span>
  
<span data-ttu-id="6cd6d-107">= Höhe \* 1</span><span class="sxs-lookup"><span data-stu-id="6cd6d-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6cd6d-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6cd6d-108">Remarks</span></span>

<span data-ttu-id="6cd6d-109">Wenn Sie einen Verweis auf die Zelle Zelle ImgHeight aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6cd6d-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6cd6d-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6cd6d-110">Cell name:</span></span>  <br/> | <span data-ttu-id="6cd6d-111">Zelle ImgHeight</span><span class="sxs-lookup"><span data-stu-id="6cd6d-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="6cd6d-112">Wenn Sie einen Verweis auf die Zelle Zelle ImgHeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6cd6d-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6cd6d-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6cd6d-113">Section index:</span></span>  <br/> |<span data-ttu-id="6cd6d-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6cd6d-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6cd6d-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6cd6d-115">Row index:</span></span>  <br/> |<span data-ttu-id="6cd6d-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="6cd6d-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="6cd6d-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6cd6d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="6cd6d-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="6cd6d-118">**visFrgnImgHeight**</span></span> <br/> |
   

